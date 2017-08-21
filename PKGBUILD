# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=sddm-s6serv
pkgver=0.1
pkgrel=3
pkgdesc="sddm service for s6"
arch=(x86_64)
license=('beerware')
depends=('sddm' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('sddm.daemon.finish.s6'
		'sddm.daemon.run.s6'
		'sddm.log.run.s6'
		'sddm.logd'
		'LICENSE')
md5sums=('2fbe9ef766564ddc18e76009aaaebbcb'
         'e9222e0a3f62e1fca2173e22d756650f'
         'bda55107725c72744a7a9c27d2287ad3'
         'ce3c2ef12063fa79f77ca9fd87b4a7b8'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/sddm.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/classic/sddm/finish"
	install -Dm 0755 "$srcdir/sddm.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/sddm/run"
	
	# log
	install -Dm 0755 "$srcdir/sddm.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/sddm/log/run"
	install -Dm 0644 "$srcdir/sddm.logd" "$pkgdir/etc/s6-serv/log.d/serv/sddm"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/sddm-s6serv/LICENSE"
}

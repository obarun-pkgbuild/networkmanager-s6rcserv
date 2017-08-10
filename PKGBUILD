# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=networkmanager-s6rcserv
pkgver=0.1
pkgrel=2
pkgdesc="networkmanager service for s6"
arch=(x86_64)
license=('beerware')
depends=('networkmanager' 's6' 's6-rc' 's6-boot')
conflicts=()
install=networkmanager-s6rcserv.install
source=('networkmanager.daemon.dependencies.s6'
		'networkmanager.daemon.pipeline-name.s6'
		'networkmanager.daemon.producer-for.s6'
		'networkmanager.daemon.run.s6'		
		'networkmanager.daemon.type.s6'	
		
		'networkmanager.log.consumer-for.s6'
		'networkmanager.log.dependencies.s6'
		'networkmanager.log.run.s6'
		'networkmanager.log.type.s6'
		
		'bundle.networkmanager.contents.s6'
		'bundle.networkmanager.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '99682fb61db23bc105306c3de36ae258'
         '1281e49b660daa6914459e390ba9f43a'
         'ec463a5215a9135565812950c731c7c5'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'ebc36c10b17cee2076605122e1e48080'
         '68b329da9893e34099c7d8ad5cb9c940'
         'f02ec24406aa73784f190b4f3294a644'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'fba65a644f6ac6a5267f8818f4866ada'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-networkmanager need a maj at networkmanager e.g user-Base
	install -Dm 0644 "$srcdir/bundle.networkmanager.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Networkmanager/contents"
	install -Dm 0644 "$srcdir/bundle.networkmanager.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Networkmanager/type"
	
	# daemon
	install -Dm 0644 "$srcdir/networkmanager.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-daemon/dependencies"
	install -Dm 0644 "$srcdir/networkmanager.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/networkmanager.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-daemon/producer-for"
	install -Dm 0644 "$srcdir/networkmanager.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-daemon/run"
	install -Dm 0644 "$srcdir/networkmanager.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-daemon/type"
	
	# log
	install -Dm 0644 "$srcdir/networkmanager.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/consumer-for"
	install -Dm 0644 "$srcdir/networkmanager.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/dependencies"
	install -Dm 0644 "$srcdir/networkmanager.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/run"
	install -Dm 0644 "$srcdir/networkmanager.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/networkmanager-s6rcserv/LICENSE"
}

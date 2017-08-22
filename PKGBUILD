# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=networkmanager-s6rcserv
pkgver=0.1
pkgrel=3
pkgdesc="networkmanager service for"
arch=(x86_64)
license=('beerware')
depends=('networkmanager' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('networkmanager.longrun.dependencies'
		'networkmanager.longrun.pipeline-name'
		'networkmanager.longrun.producer-for'
		'networkmanager.longrun.run'		
		'networkmanager.longrun.type'	
		
		'networkmanager.log.consumer-for'
		'networkmanager.log.dependencies'
		'networkmanager.log.run'
		'networkmanager.log.type'
		
		'bundle.networkmanager.contents'
		'bundle.networkmanager.type'
		'networkmanager.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '99682fb61db23bc105306c3de36ae258'
         '1281e49b660daa6914459e390ba9f43a'
         'ec463a5215a9135565812950c731c7c5'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'c5a2551e9ed77ac4e579c7366cd19946'
         '68b329da9893e34099c7d8ad5cb9c940'
         'f02ec24406aa73784f190b4f3294a644'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'f2949dc6318b701b9c648f6a3938db34'
         '71abe97e2554d37f1d12c5bf4945297f'
         '4600f52ba053f24adfae1a2468b0c60e'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-networkmanager need a maj at networkmanager e.g user-Base
	install -Dm 0644 "$srcdir/bundle.networkmanager.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Networkmanager/contents"
	install -Dm 0644 "$srcdir/bundle.networkmanager.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Networkmanager/type"
	
	# longrun
	install -Dm 0644 "$srcdir/networkmanager.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/networkmanager-longrun/dependencies"
	install -Dm 0644 "$srcdir/networkmanager.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/networkmanager-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/networkmanager.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/networkmanager-longrun/producer-for"
	install -Dm 0644 "$srcdir/networkmanager.longrun.run" "$pkgdir/etc/s6-serv/available/rc/networkmanager-longrun/run"
	install -Dm 0644 "$srcdir/networkmanager.longrun.type" "$pkgdir/etc/s6-serv/available/rc/networkmanager-longrun/type"
	
	# log
	install -Dm 0644 "$srcdir/networkmanager.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/consumer-for"
	install -Dm 0644 "$srcdir/networkmanager.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/dependencies"
	install -Dm 0644 "$srcdir/networkmanager.log.run" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/run"
	install -Dm 0644 "$srcdir/networkmanager.log.type" "$pkgdir/etc/s6-serv/available/rc/networkmanager-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/networkmanager.logd" "$pkgdir/etc/s6-serv/log.d/networkmanager-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/networkmanager-s6rcserv/LICENSE"
}

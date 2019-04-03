## 스카우터 2.6.0 버전

스카우터는 자바프로그래밍 모니터링 프로그램이며
특히나 스프링에 최적화 되어있다.

에이전트는 자바버전에 맞게 고른뒤
실행할 서버프로그램을 실행할때 옵션을 줘서 같이 실행하게 하면 된다
(http://192.168.0.138/pyh/tomcat8.5/blob/master/tomcat8.5_linux/bin/catalina.sh 참고)

에이전트중에 host는 별개로 실행해줘야된다.

수집된 데이터는 연결된 socuter 서버에 통해 저장된다
그후 서버에 클라이언트를 붙여서 모니터링을 할수 있다.

## 주요옵션설명

에이전트의 ./conf/scouter.conf 에 보면 

net_collector_ip=서버IP
net_collector_udp_port=서버port
net_collector_tcp_port=서버port

hook_service_patterns=모니터링 원하는 클래스 및 메소드(ex : com.winitech.aaa.cron.job.*.start)
profile_spring_controller_method_parameter_enabled=true 스프링 컨트롤러 단에서 발생되는 파라메터 및 리턴값 출력허락

서버의 ./conf/scouter.conf 에 보면

net_tcp_listen_port=TCP서버 포트를 결정
net_udp_listen_port=UPD서버 포트를 결정
mgr_purge_disk_usage_pct=30 디스크 용량을 결정

클라이언트는 admin//admin으로 기본접속가능


@brief socket�����������׽���
@param int family:ָ��Э����
	AF_INET		IPv4
	AF_INET6	IPv6
	AF_LOCAL	Unix��Э��
	AF_ROUTE	·���׽���
	AF_KEY		��Կ�׽���
@param int type:ָ���׽�������
	SOCK_STREAM		�ֽ����׽���
	SOCK_DGRAM		���ݰ��׽���
	SOCK_SEQPACKET	��������׽���
	SOCK_RAW		ԭʼ�׽���
@param int protocol:����Ϊ0��ĳ��Э�����ͳ�ֵ
	IPPROTO_CP		TCP����Э��
	IPPROTO_UDP		UDP����Э��
	IPPROTO_SCTP	SCTP����Э��
@return �ɹ�ʱ����һ���Ǹ����׽�����������������-1
�ο���
				AF_INET		AF_INET6	AF_ROUTE	AF_ROUTE	AF_KEY
SOCK_STREAM		TCP|SCTP	TCP|SCTP	��
SOCK_DGRAM		UDP			UDP			��
SOCK_SEQPACKET	SCTP		SCTP		��
SOCK_RAW		IPV4		IPv6					��			��


@brief connect������TCP�ͻ���ʹ�øú���������TCP������
@param int sockfd:���з�����ip�˿ڵ��׽���������
@param const
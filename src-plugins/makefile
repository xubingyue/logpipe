# ���ļ���makeobj.sh�Զ�����
############################################################
# ��Ŀ�� : 
# ģ���� : 
# ��  ע : 
############################################################

###### Դ�ļ�������
#@ c_FILE
c_FILE		=	\
			logpipe-input-file.c \
			logpipe-output-file.c \
			logpipe-input-tcp.c \
			logpipe-output-tcp.c \

###### Ŀ���ļ�����װĿ¼������
include makeinstall
LIB		=	\
			logpipe-input-file.so \
			logpipe-output-file.so \
			logpipe-input-tcp.so \
			logpipe-output-tcp.so \

LIBINST		=	$(_LIBINST)

###### ����ѡ��
CFLAGS		=	$(_CFLAGS) \
			-std=gnu99 \
			-I$(HOME)/include/logpipe \

###### ����ѡ��
LFLAGS		=	$(_LFLAGS) \
			-L$(HOME)/lib \
			-llogpipe_api \

###### ����궨����
CLEAN_ADDITION	=

###### ����mktplģ���
#@ make_all
#@ make_clean
#@ make_install
#@ make_install_LIBINST
#@ make_install_DFTHDERINST
#@ make_uninstall
#@ make_uninstall_LIBINST
#@ make_uninstall_DFTHDERINST
include $(MKTPLDIR)/makeobj_$(MKTPLOS).inc

###### Ŀ���ļ�������ϵ
logpipe-input-file.so		:	logpipe-input-file.o
	$(CC) -o $@ logpipe-input-file.o $(SOFLAGS) $(LFLAGS)

logpipe-output-file.so		:	logpipe-output-file.o
	$(CC) -o $@ logpipe-output-file.o $(SOFLAGS) $(LFLAGS)

logpipe-input-tcp.so		:	logpipe-input-tcp.o
	$(CC) -o $@ logpipe-input-tcp.o $(SOFLAGS) $(LFLAGS)

logpipe-output-tcp.so		:	logpipe-output-tcp.o
	$(CC) -o $@ logpipe-output-tcp.o $(SOFLAGS) $(LFLAGS)

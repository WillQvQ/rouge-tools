FROM ubuntu
ADD ./packages/* /root/
RUN apt-get update && apt-get install -y libwww-perl libdb-dev gcc libexpat1-dev make \
    && cd /root/XML-Parser-2.44 && perl Makefile.PL && make install \
    && cd /root/XML-RegExp-0.04 && perl Makefile.PL && make && make install \
    && cd /root/XML-DOM-1.46 && perl Makefile.PL && make && make install \
    && cd /root/DB_File-1.835 && perl Makefile.PL && make && make install \
    && apt-get remove -y gcc libexpat1-dev make && rm -rf /var/lib/apt/lists/* \
    && cd /root && rm -rf XML-Parser-2.44 XML-RegExp-0.04 XML-DOM-1.46 DB_File-1.835
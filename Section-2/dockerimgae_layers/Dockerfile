FROM ubuntu

# Combine multiple commands into 1 layer for better performance

RUN dd if=/dev/zero of=/root/file1.txt bs=1M count=100 && rm -f /root/file1.txt
RUN dd if=/dev/zero of=/root/file2.txt bs=1M count=100 && rm -f /root/file2.txt


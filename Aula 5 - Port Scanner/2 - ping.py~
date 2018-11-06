from scapy.all import *
conf.verb = 0

IPs = []

for ip in range(1, 255): #1
    IPs.append("192.168.0." + str(ip) )

pacote = IP(dst=IPs)/ICMP() #2
ans, unans = sr(pacote, inter=0.1, timeout=1) #3

print "Hosts ativos"

for pacoteRecebido in ans:
    print pacoteRecebido[1][IP].src #4

'''Para determinar os hosts inativos:
print "Hosts inativos"
for pacoteNaoRecebido in unans:
    print pacoteNaoRecebido.dst
'''
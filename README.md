# BM-SC-Playbook1
BM-SC access disections 

The [BM-SC](https://www.etsi.org/deliver/etsi_ts/123200_123299/123246/14.01.00_60/ts_123246v140100p.pdf) provides functions for [MBMS](https://www.etsi.org/deliver/etsi_ts/123200_123299/123246/14.01.00_60/ts_123246v140100p.pdf) user service provisioning and delivery.

![MBMS Broadcast Mode](https://user-images.githubusercontent.com/47313728/91259815-15467780-e724-11ea-865c-49985ab868fb.PNG)

MBMS Broadcast Mode

For MBMS delivery, [GCS AS](https://www.etsi.org/deliver/etsi_ts/123400_123499/123468/12.02.00_60/ts_123468v120200p.pdf) follow [MB2-C procedures](https://www.etsi.org/deliver/etsi_ts/123400_123499/123468/12.02.00_60/ts_123468v120200p.pdf) to request the BM-SC to activate, deactivate, modify an MBMS bearer, allocate/deallocate TMGI and forwarding of data to be delivered via an MBMS bearer to the BM-SC via the MB2-U reference point

BM-SC from a vendor register live MB2-C/access Procedures daily bases. The [YAML](https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html) [Playbook](https://docs.ansible.com/ansible/latest/user_guide/playbooks_intro.html), access.yml, logon to the said BM-SC utilizing the credetials and host information from inventory. It then grep the he TMGI values from the access log, 

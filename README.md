# BM-SC-Playbook1
BM-SC access disections 

The [BM-SC](https://www.etsi.org/deliver/etsi_ts/123200_123299/123246/14.01.00_60/ts_123246v140100p.pdf) provides functions for [MBMS](https://www.etsi.org/deliver/etsi_ts/123200_123299/123246/14.01.00_60/ts_123246v140100p.pdf) user service provisioning and delivery.

![MBMS Broadcast Mode](https://user-images.githubusercontent.com/47313728/91259815-15467780-e724-11ea-865c-49985ab868fb.PNG)

MBMS Broadcast Mode

For MBMS delivery, [GCS AS](https://www.etsi.org/deliver/etsi_ts/123400_123499/123468/12.02.00_60/ts_123468v120200p.pdf) follow [MB2-C procedures](https://www.etsi.org/deliver/etsi_ts/123400_123499/123468/12.02.00_60/ts_123468v120200p.pdf) to request the BM-SC to activate, deactivate, modify an MBMS bearer, allocate/deallocate [TMGI](https://www.etsi.org/deliver/etsi_ts/124000_124099/124008/13.07.00_60/ts_124008v130700p.pdf) and forwarding of data to be delivered via an MBMS bearer to the BM-SC via the MB2-U reference point

BM-SC, from a vendor, does register live MB2-C/access Procedures daily bases. The [YAML](https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html) [Playbook](https://docs.ansible.com/ansible/latest/user_guide/playbooks_intro.html), BM-SC.yml, logon to the said BM-SC utilizing the credetials and host information from inventory. It then grep the TMGI values from [GCS-Action](https://www.etsi.org/deliver/etsi_ts/129400_129499/129468/13.00.00_60/ts_129468v130000p.pdf) (GAR/GAA) messages in the access log, trim the values to match with the TMGI values in other messages and store them in a list making sure all values are unique.

The Playbook then perform another grep on TMGI values to segregate messages based on each TMGI value. Each group is stamped with TMGI Title and all are save in a file for Telecom Service Engineer to analyze.

Here is one sample



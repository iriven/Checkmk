# Checkmk Distributed Monitoring Tools
Ansible playbooks and roles for a checkmk distributed monitoring  plateform management



---
# -------------------------------------
# GLOBAL PARAMETERS
# -------------------------------------
vaultPasswdFile: '/.cmkvault.cfg'
vaultPasswd: 'xxxxxxxxxx'
# -------------------------------------
# ASSETS DATABASE API PARAMETERS
# -------------------------------------
assetDatabase:
  apiserver: 'assets.db.tld'
  apikey:  'xxxxxxxxxxxxxxxxxxxxxxxxxxxxx'
  protocol: 'https'

# -------------------------------------
# CHECKMK PARAMETERS
# -------------------------------------
checkmkParams:
  default:
    sitepath:  '/opt/omd/sites'
    admuser:   'cmkadmin'
    admpasswd: 'XXXXXXXX'
    sitename:  'mainsite'
    apiuser:   'automation'
    apikey:    'yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy'
    apiversion: '1.0'
    protocol:  'http'
    zoneparams:
      - region: 'us'
        server: 'amer.master.tld'
      - region: 'as'
        server: 'asia.master.tld'
      - region: 'eu'
        server: 'euro.master.tld'

  environment:
    - name:      'dev'
      sitepath:  '/opt/omd/sites'
      admuser:   'cmkadmin'
      admpasswd: 'XXXXXXXX'
      sitename:  'mainsite'
      apiuser:   'automation'
      apikey:    'yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy'
      apiversion: '1.0'
      protocol:  'http'
      zoneparams:
        - region: 'us'
          server: 'amer.master.tld'
        - region: 'as'
          server: 'asia.master.tld'
        - region: 'eu'
          server: 'euro.master.tld'
    - name:      'stg'
      # sitepath:  '/opt/omd/sites'
      # admuser:   'cmkadmin'
      # admpasswd: ''
      # sitename:  ''
      # apiuser:   'automation'
      # apikey:    ''
      # apiversion: '1.0'
      # protocol:  'https'
    - name:      'prd'
      # sitepath:  '/opt/omd/sites'
      # admuser:   'cmkadmin'
      # admpasswd: ''
      # sitename:  ''
      # apiuser:   'automation'
      # apikey:    ''
      # apiversion: '1.0'
      # protocol:  'https'

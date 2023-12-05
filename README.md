# Instructions for converting languages

Includes 2 languages: Chinese and Cambodian

## Installation Instructions

Bitbucket clone path, including language-related files

```sh
https://bitbucket.org/dotbvn/dotbedu_lang/src/main/
```

## Conversion instructions

### There are two typical language files to convert in the entire folder, including other files with prefixes like zh_CN. and kh_CA.

#### Chinese language
```sh
zh_CN.lang.php
```
#### Cambodian language
```sh
kh_CA.lang.php
```

### Note regarding: app_list_strings

For example:

> Note: when not converted

```sh
$app_list_strings['audit_status_list'] = array(
    'success'   => 'Success',
    'in_progress'  => 'In Progress',
    'not_found' => 'Not found',
);
$app_list_strings['c_uploadimage_status_dom']['Active'] = 'Active';
```

Convert to:

> Note: keep the name of app_list_strings(audit_status_list) and its key

```sh
$app_list_strings['audit_status_list'] = array(
    'success'   => 'ជោគជ័យ',
    'in_progress'  => 'ដំណើរការ',
    'not_found' => 'រក​មិន​ឃើញ',
);
$app_list_strings['c_uploadimage_status_dom']['Active'] = 'សកម្ម';
```

### Note regarding: mod_strings

For example:

> Note: when not converted

```sh
$mod_strings = array(
    'LBL_DRI_WORKFLOWS' => 'Customer Journeys',
    'LBL_DRI_WORKFLOW_TEMPLATE' => 'Customer Journey Template',
);
$mod_strings['LBL_DRI_WORKFLOWS'] = 'Customer Journeys';
```

Convert to:

> Note: keep the original name mod_strings(LBL_...)

```sh
$mod_strings = array(
    'LBL_DRI_WORKFLOWS' => 'ដំណើររបស់អតិថិជន',
    'LBL_DRI_WORKFLOW_TEMPLATE' => 'គំរូការធ្វើដំណើររបស់អតិថិជន',
);
$mod_strings['LBL_DRI_WORKFLOWS'] = 'ដំណើររបស់អតិថិជន';
```

### Note regarding: .html .tpl

For example:

> Note: when not converted

```sh
Subject: {CALL_SUBJECT}
Status: {CALL_STATUS}
Start Date: {CALL_STARTDATE}
```

Convert to: 

> Note: keep the name in brackets for example {CALL_SUBJECT}

```sh
ប្រធានបទ: {CALL_SUBJECT}
ស្ថានភាព: {CALL_STATUS}
ថ្ងៃ​ចាប់ផ្តើម: {CALL_STARTDATE}
```
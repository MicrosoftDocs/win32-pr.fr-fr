---
title: Structure RECORD_HEADER
description: En-tête d’enregistrement utilisé par \_ l' \_ entrée du journal des modifications et les \_ structures d’en-tête du journal des modifications \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Restauration du système de la structure RECORD_HEADER
- PRECORD_HEADER de la restauration du système du pointeur de structure
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466358"
---
# <a name="record_header-structure"></a>\_Structure d’en-tête d’enregistrement

\[Ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]

En-tête d’enregistrement utilisé par l' [**\_ \_ entrée du journal des modifications**](change-log-entry.md) et les structures d' [**\_ \_ en-tête du journal des modifications**](change-log-header.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwRecordSize**
</dt> <dd>

Taille totale de l’enregistrement, y compris l’en-tête, en octets.

</dd> <dt>

**dwRecordType**
</dt> <dd>

Type d’enregistrement. Ce membre peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <dt>**RecordTypeLogHeader**</dt> <dt>0</dt> </dl>     | L’enregistrement est l’en-tête du journal des modifications.<br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <dt>**RecordTypeLogEntry**</dt> <dt>1</dt> </dl>         | L’enregistrement est l’en-tête d’une entrée de journal des modifications.<br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <dt>**RecordTypeVolumePath**</dt> <dt>2</dt> </dl> | Les données sont le chemin d’accès du volume pour l’entrée du journal des modifications.<br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <dt>**RecordTypeFirstPath**</dt> <dt>3</dt> </dl>     | Les données sont le chemin de fichier de l’entrée du journal des modifications.<br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <dt>**RecordTypeSecondPath**</dt> <dt>4</dt> </dl> | Les données sont utilisées lors de l’attribution d’un nouveau nom aux entrées du journal des modifications. ce chemin d’accès est l’emplacement où le fichier renommé est stocké.<br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <dt>**RecordTypeTempPath**</dt> <dt>5</dt> </dl>         | Les données sont le nom du fichier de sauvegarde utilisé pour restaurer l’entrée du journal des modifications. Les fichiers de sauvegarde se trouvent dans le dossier RP *n* . Le nom de fichier a le format suivant : a *xxxxxxx*. *ext*, où *xxxxxxx* est un nombre à sept chiffres et *ext* est l’extension de nom de fichier.<br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <dt>**RecordTypeAclInline**</dt> <dt>6</dt> </dl>     | Les données sont une liste de contrôle d’accès. Le format de données est une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . <br/> Cette valeur ne peut pas être supérieure à 8 192 octets. Pour spécifier une valeur supérieure à 8 192 octets, utilisez le membre **RecordTypeAclFile** .<br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <dt>**RecordTypeAclFile**</dt> <dt>7</dt> </dl>             | Les données sont le nom du fichier ACL utilisé pour stocker la liste de contrôle d’accès. Les fichiers ACL se trouvent dans le dossier RP *n* . Le nom de fichier est au format suivant : S *xxxxxxx*. ACL, où *xxxxxxx* est un nombre à sept chiffres.<br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <dt>**RecordTypeDebugInfo**</dt> <dt>8</dt> </dl>     | Les données sont des informations de débogage pour l’entrée du journal des modifications. Le format de données est une structure d' **\_ \_ \_ informations de débogage du journal SR** . Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <dt>**RecordTypeShortName**</dt> <dt>9</dt> </dl>     | Les données sont le nom abrégé du fichier de sauvegarde.<br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La structure des **\_ \_ \_ informations de débogage du journal SR** est définie comme suit.

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                       |



 


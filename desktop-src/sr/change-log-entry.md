---
title: Structure CHANGE_LOG_ENTRY
description: Entrée du journal des modifications.
ms.assetid: adbdc6e6-895e-486d-a194-c74d2cbd0052
keywords:
- Restauration du système de la structure CHANGE_LOG_ENTRY
- PCHANGE_LOG_ENTRY de la restauration du système du pointeur de structure
topic_type:
- apiref
api_name:
- CHANGE_LOG_ENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee4eca1bad0859159821d7717ba6c23c352e03b33a1fcab81721e08dba465c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452930"
---
# <a name="change_log_entry-structure"></a>Structure de l’entrée du journal des modifications \_ \_

\[ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]

Entrée du journal des modifications.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _CHANGE_LOG_ENTRY {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwEntryType;
  DWORD         dwEntryFlags;
  DWORD         dwAttributes;
  INT64         i64SequenceNum;
  WCHAR         szProcName[16];
} CHANGE_LOG_ENTRY, *PCHANGE_LOG_ENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**RecordHeader**
</dt> <dd>

Structure [**d' \_ en-tête d’enregistrement**](record-header.md) . Le membre **dwRecordType** doit être défini sur **RecordTypeLogEntry** (1).

</dd> <dt>

**dwMagicNum**
</dt> <dd>

Ce membre doit être défini sur 0xabcdef12.

</dd> <dt>

**dwEntryType**
</dt> <dd>

Ce membre peut prendre l’une des valeurs suivantes :

<dl><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0x2_"></span><span id="change_log_entrytypes_aclchange__0x2_"></span><span id="CHANGE_LOG_ENTRYTYPES_ACLCHANGE__0X2_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ ACLCHANGE * * (0X2) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0x4_"></span><span id="change_log_entrytypes_attrchange__0x4_"></span><span id="CHANGE_LOG_ENTRYTYPES_ATTRCHANGE__0X4_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ ATTRCHANGE * * (0x4) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0x80_"></span><span id="change_log_entrytypes_dircreate__0x80_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRCREATE__0X80_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ DIRCREATE * * (0x80) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0x100_"></span><span id="change_log_entrytypes_dirrename__0x100_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRRENAME__0X100_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ DIRRENAME * * (0x100) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0x200_"></span><span id="change_log_entrytypes_dirdelete__0x200_"></span><span id="CHANGE_LOG_ENTRYTYPES_DIRDELETE__0X200_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ DIRDELETE * * (0x200) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0x20_"></span><span id="change_log_entrytypes_filecreate__0x20_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILECREATE__0X20_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ FILECREATE * * (0x20) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0x10_"></span><span id="change_log_entrytypes_filedelete__0x10_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILEDELETE__0X10_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ FILEDELETE * * (0x10) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0x40_"></span><span id="change_log_entrytypes_filerename__0x40_"></span><span id="CHANGE_LOG_ENTRYTYPES_FILERENAME__0X40_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ FILERENAME * * (0x40) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0x100000_"></span><span id="change_log_entrytypes_inprecreate__0x100000_"></span><span id="CHANGE_LOG_ENTRYTYPES_INPRECREATE__0X100000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ INPRECREATE * * (3 x) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0x20000_"></span><span id="change_log_entrytypes_isdir__0x20000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISDIR__0X20000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ ISDIR * * (0x20000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0x40000_"></span><span id="change_log_entrytypes_isnotdir__0x40000_"></span><span id="CHANGE_LOG_ENTRYTYPES_ISNOTDIR__0X40000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ ISNOTDIR * * (0x40000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0x400_"></span><span id="change_log_entrytypes_mountcreate__0x400_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTCREATE__0X400_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ MOUNTCREATE * * (0x400) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0x800_"></span><span id="change_log_entrytypes_mountdelete__0x800_"></span><span id="CHANGE_LOG_ENTRYTYPES_MOUNTDELETE__0X800_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ MOUNTDELETE * * (0x800) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0x10000_"></span><span id="change_log_entrytypes_nooptimize__0x10000_"></span><span id="CHANGE_LOG_ENTRYTYPES_NOOPTIMIZE__0X10000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ nooptimise * * (0x10000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0x200000_"></span><span id="change_log_entrytypes_openbyid__0x200000_"></span><span id="CHANGE_LOG_ENTRYTYPES_OPENBYID__0X200000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ OPENBYID * * (0x200000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0x80000_"></span><span id="change_log_entrytypes_simulatedelete__0x80000_"></span><span id="CHANGE_LOG_ENTRYTYPES_SIMULATEDELETE__0X80000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ SIMULATEDELETE * * (0x80000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0x1_"></span><span id="change_log_entrytypes_streamchange__0x1_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCHANGE__0X1_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ STREAMCHANGE * * (0x1) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0x2000_"></span><span id="change_log_entrytypes_streamcreate__0x2000_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMCREATE__0X2000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ STREAMCREATE * * (0x2000) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0x8_"></span><span id="change_log_entrytypes_streamoverwrite__0x8_"></span><span id="CHANGE_LOG_ENTRYTYPES_STREAMOVERWRITE__0X8_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ STREAMOVERWRITE * * (0x8) * *
</dt><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0x1000_"></span><span id="change_log_entrytypes_volumeerror__0x1000_"></span><span id="CHANGE_LOG_ENTRYTYPES_VOLUMEERROR__0X1000_"></span><dt>

Journal des modifications \_ \_ ENTRYTYPES \_ VOLUMEERROR * * (0x1000) * *
</dt> </dl> </dd> <dt>

**dwEntryFlags**
</dt> <dd>

Ce membre peut prendre l’une des valeurs suivantes :

<dl><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0x4_"></span><span id="change_log_entryflags_aclinfo__0x4_"></span><span id="CHANGE_LOG_ENTRYFLAGS_ACLINFO__0X4_"></span><dt>

**Journal des modifications \_ \_ ENTRYFLAGS \_ ACLINFO (0x4)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0x8_"></span><span id="change_log_entryflags_debuginfo__0x8_"></span><span id="CHANGE_LOG_ENTRYFLAGS_DEBUGINFO__0X8_"></span><dt>

**Journal des modifications \_ \_ ENTRYFLAGS \_ DebugInfo (0x8)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0x2_"></span><span id="change_log_entryflags_secondpath__0x2_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SECONDPATH__0X2_"></span><dt>

**Journal des modifications \_ \_ ENTRYFLAGS \_ SECONDPATH (0X2)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0x10_"></span><span id="change_log_entryflags_shortname__0x10_"></span><span id="CHANGE_LOG_ENTRYFLAGS_SHORTNAME__0X10_"></span><dt>

**MODIFIER le \_ journal \_ ENTRYFLAGS \_ ShortName (0x10)**
</dt><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0x1_"></span><span id="change_log_entryflags_temppath__0x1_"></span><span id="CHANGE_LOG_ENTRYFLAGS_TEMPPATH__0X1_"></span><dt>

**Journal des modifications \_ \_ ENTRYFLAGS \_ TempPath (0x1)**
</dt> </dl> </dd> <dt>

**dwAttributes**
</dt> <dd>

Attributs de fichier du fichier journal de modification. Si aucun attribut n’est spécifié, cette valeur doit être définie sur 0xFFFFFFFF.

</dd> <dt>

**i64SequenceNum**
</dt> <dd>

Numéro de séquence assigné à l’entrée du journal des modifications.

</dd> <dt>

**szProcName**
</dt> <dd>

Nom du processus qui effectue la modification.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est suivie d’un nombre variable d’enregistrements de données de longueur variable, ainsi que d’une valeur **DWORD** qui doit être identique à la valeur du membre **dwRecordSize** de **RecordHeader**.

Les enregistrements de données de longueur variable se composent d’une structure d' [**\_ en-tête d’enregistrement**](record-header.md) et de données qui peuvent être utilisées pour restaurer l’entrée du journal des modifications. Le format des données dépend de la valeur du membre **dwRecordType** de la structure d' **\_ en-tête d’enregistrement** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                            |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                       |



 

 






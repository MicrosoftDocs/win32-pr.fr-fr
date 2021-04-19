---
description: Spécifie un objet à signer.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Structure SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520522"
---
# <a name="signer_subject_info-structure"></a>Structure des informations de l’objet du signataire \_ \_

La structure d' **\_ \_ informations** sur l’objet du signataire spécifie un objet à signer.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**pdwIndex**
</dt> <dd>

Ce membre est réservé. Elle doit être définie sur zéro.

</dd> <dt>

**dwSubjectChoice**
</dt> <dd>

Spécifie si l’objet est un fichier ou un [*objet BLOB*](../secgloss/b-gly.md). Ce membre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                         | Signification                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**Signataire \_ OBJET \_ BLOB**</dt> <dt>2 (0X2)</dt> </dl> | L’objet est un objet BLOB.<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**Signataire \_ \_Fichier objet**</dt> <dt>1 (0x1)</dt> </dl> | L’objet est un fichier.<br/> |



 

</dd> <dt>

**pSignerFileInfo**
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de fichier du signataire**](signer-file-info.md) qui spécifie le fichier à signer.

</dd> <dt>

**pSignerBlobInfo**
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations d’objet blob de signataire**](signer-blob-info.md) qui spécifie l’objet blob à signer.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 

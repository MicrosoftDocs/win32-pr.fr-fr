---
description: Spécifie un objet BLOB à signer.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Structure SIGNER_BLOB_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530291"
---
# <a name="signer_blob_info-structure"></a>Structure des \_ informations de l’objet blob de signataire \_

\[La structure des informations de l' **\_ objet \_ BLOB du signataire** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

La structure d’informations de l' **\_ objet BLOB \_ du signataire** spécifie un [*objet BLOB*](../secgloss/b-gly.md) à signer.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**pGuidSubject**
</dt> <dd>

Pointeur vers un **GUID** qui spécifie le package d’interface de sujet (SIP) à charger.

</dd> <dt>

**cbBlob**
</dt> <dd>

Taille, en octets, de l’objet BLOB à signer.

</dd> <dt>

**pbBlob**
</dt> <dd>

Pointeur vers l’objet BLOB à signer.

</dd> <dt>

**pwszDisplayName**
</dt> <dd>

Nom complet de l’objet BLOB. Ce membre peut avoir la valeur **null**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**informations d' \_ objet du signataire \_**](signer-subject-info.md)
</dt> </dl>

 

 

---
title: Structure WINBIO_BIR_DATA ( \_ types WINBIO. h)
description: Spécifie la taille, en octets, et le décalage d’un bloc d’informations biométriques.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BIR_DATA
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384596"
---
# <a name="winbio_bir_data-structure"></a>\_Structure de \_ données WINBIO Bir

La structure de **\_ \_ données WINBIO Bir** spécifie la taille, en octets, et le décalage d’un bloc d’informations biométriques. Cette structure est utilisée par la [**structure \_ Bir WINBIO**](winbio-bir.md) pour spécifier où se trouvent les différentes parties d’un enregistrement d’informations biométriques.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**Taille**
</dt> <dd>

Taille, en octets, des informations biométriques.

</dd> <dt>

**Offset**
</dt> <dd>

Décalage, en octets, entre le début de la structure [**\_ Bir WINBIO**](winbio-bir.md) et les informations biométriques.

</dd> </dl>

## <a name="remarks"></a>Notes

L’utilisation de décalages plutôt que de pointeurs permet de faciliter la sérialisation du BIR et de la traduction moins compliquée entre les environnements 32 et 64 bits ou entre l’utilisateur et le mode noyau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md)
</dt> </dl>

 

 






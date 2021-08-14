---
title: Structure WINBIO_VERSION ( \_ types WINBIO. h)
description: Contient le numéro de version du logiciel d’un composant du fournisseur de services biométriques.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- API de Windows Biometric Framework de structure de WINBIO_VERSION
- API du pointeur de structure PWINBIO_VERSION Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de81dd3da7f37e473a65caaf3e4cd52c8fd2f6732dced45f43245cb4e4c5c905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909114"
---
# <a name="winbio_version-structure"></a>Structure de la version de WINBIO \_

La structure de **\_ version WINBIO** contient le numéro de version du logiciel d’un composant du fournisseur de services biométriques.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>Membres

<dl> <dt>

**MajorVersion**
</dt> <dd>

**Valeur DWORD** qui contient le numéro de version principale.

</dd> <dt>

**MinorVersion**
</dt> <dd>

**Valeur DWORD** qui contient le numéro de version mineure.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**\_schéma BSP \_ WINBIO**](winbio-bsp-schema.md)
</dt> <dt>

[**\_schéma d’unité WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 






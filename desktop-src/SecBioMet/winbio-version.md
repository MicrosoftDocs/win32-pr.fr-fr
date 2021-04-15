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
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466914"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**\_schéma BSP \_ WINBIO**](winbio-bsp-schema.md)
</dt> <dt>

[**\_schéma d’unité WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 






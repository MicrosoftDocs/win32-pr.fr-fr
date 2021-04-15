---
title: Structure WINBIO_BSP_SCHEMA ( \_ types WINBIO. h)
description: Décrit les fonctionnalités d’un fournisseur de services biométriques.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BSP_SCHEMA
- API du pointeur de structure PWINBIO_BSP_SCHEMA Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465414"
---
# <a name="winbio_bsp_schema-structure"></a>\_Structure de \_ schéma BSP WINBIO

La structure de **\_ \_ schéma BSP WINBIO** décrit les fonctionnalités d’un fournisseur de services biométriques. Cette structure est utilisée par la fonction [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>Membres

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Type de mesure biométrique utilisé par cet appareil. Actuellement, il doit s’agir d’une **\_ \_ empreinte digitale de type WINBIO**.

</dd> <dt>

**BspId**
</dt> <dd>

Valeur qui identifie de façon unique ce composant du fournisseur de services biométriques.

</dd> <dt>

**Description**
</dt> <dd>

Chaîne Unicode terminée par le caractère **null** qui contient une description du fournisseur de services biométriques.

</dd> <dt>

**Fournisseur**
</dt> <dd>

Chaîne Unicode terminée par le caractère **null** qui contient le nom du fournisseur qui fournit le fournisseur de services biométriques.

</dd> <dt>

**Version**
</dt> <dd>

Une structure de [**\_ version WINBIO**](winbio-version.md) contient la version logicielle du composant du fournisseur de services biométriques.

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

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 






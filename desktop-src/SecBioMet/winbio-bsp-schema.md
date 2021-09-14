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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095986"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 






---
description: L' \_ énumération de l’indicateur de stockage de clé CAPICOM définit des indicateurs de stockage de \_ \_ clé.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: Énumération CAPICOM_KEY_STORAGE_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121093"
---
# <a name="capicom_key_storage_flag-enumeration"></a>\_Énumération de l' \_ indicateur de stockage de clé CAPICOM \_

L’énumération de l' **\_ indicateur de \_ stockage \_ de clé CAPICOM** définit des indicateurs de stockage de clé.

## <a name="members"></a>Membres



| Membre                                     | Description                           | Valeur |
|--------------------------------------------|---------------------------------------|-------|
| **\_ \_ \_ valeur par défaut du stockage de la clé CAPICOM**         | Stockage de clé par défaut.<br/>       | 0     |
| **\_espace de stockage de clé CAPICOM \_ \_ exportable**      | La clé peut être exportée.<br/>     | 1     |
| **\_clé CAPICOM \_ \_ protégée par l’utilisateur \_** | La clé est protégée par l’utilisateur.<br/> | 2     |



## <a name="remarks"></a>Notes

Cette énumération est utilisée par la méthode suivante :

-   [**Certificate. Load**](certificate-load.md)
-   [**Store. Load**](store-load.md)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 





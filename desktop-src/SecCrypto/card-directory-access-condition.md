---
description: Spécifie les autorisations de contrôle d’accès pour un répertoire sur une carte à puce.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Énumération CARD_DIRECTORY_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 8038179c7337edaff0138fc46c34191f99821250808c4ace16dc76cdfafd3b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878959"
---
# <a name="card_directory_access_condition-enumeration"></a>\_ \_ Énumération des conditions d’accès au répertoire des cartes \_

L’énumération des **\_ conditions d' \_ accès \_ au répertoire** de la carte spécifie les autorisations de contrôle d’accès pour un répertoire sur une [*carte à puce*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Cette valeur n’est pas valide.

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**
</dt> <dd>

Certains utilisateurs peuvent lire, écrire et supprimer le répertoire.

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**
</dt> <dd>

Les administrateurs peuvent lire, écrire et supprimer le répertoire.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows xp, Windows xp, \[ applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows server 2003, Windows server 2003 \[ desktop apps uniquement\]<br/>            |
| En-tête<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur de services de chiffrement de la carte à puce de base Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**CardCreateDirectory**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**CardDeleteDirectory**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 

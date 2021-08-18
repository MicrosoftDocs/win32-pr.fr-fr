---
description: Spécifie les autorisations de contrôle d’accès pour un fichier sur une carte à puce.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Énumération CARD_FILE_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: e9a38e7d67e413352de693f52b07ba11bf34858854fa708b41a735152ad3ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771985"
---
# <a name="card_file_access_condition-enumeration"></a>\_ \_ Énumération des conditions d’accès au fichier de carte \_

L’énumération des conditions d’accès au fichier de carte spécifie les autorisations de contrôle d’accès pour un fichier sur une [*carte à puce*](../secgloss/s-gly.md). **\_ \_ \_**

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Cette valeur n’est pas valide.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**
</dt> <dd>

Tout le monde peut lire le fichier. Des utilisateurs spécifiques peuvent écrire dans le fichier.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

Seuls les utilisateurs spécifiques peuvent lire ou écrire dans le fichier.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

Tout le monde peut lire le fichier. Les administrateurs peuvent écrire dans le fichier.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

Les autorisations d’accès au fichier sont inconnues.

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

[**\_informations sur le fichier de carte \_**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 

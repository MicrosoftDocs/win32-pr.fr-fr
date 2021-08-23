---
description: Obtient le nom du conteneur de compte de l’utilisateur.
title: DIDiskQuotaUser. AccountContainerName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: a7a439fe36262e7f73fd7b839fd60af5b1b0a9b05f77769ab1d6a8c5ee9d06fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094230"
---
# <a name="didiskquotauseraccountcontainername-property"></a>DIDiskQuotaUser. AccountContainerName, propriété

Obtient le nom du conteneur de compte de l’utilisateur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de chaîne qui est définie sur le nom du conteneur de compte de l’utilisateur.

## <a name="remarks"></a>Remarques

Pour les comptes sans informations sur les services d’annuaire, cette propriété contient le nom de domaine. Pour les comptes avec les informations des services d’annuaire, cette propriété contient un nom canonique avec le nom de l’objet de fin supprimé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 





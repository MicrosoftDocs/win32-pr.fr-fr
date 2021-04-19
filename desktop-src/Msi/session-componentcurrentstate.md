---
description: La propriété ComponentCurrentState de l’objet session est une propriété en lecture seule qui retourne l’état installé actuel du composant désigné. Pour les valeurs d’État, consultez la propriété ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Session. ComponentCurrentState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537542"
---
# <a name="sessioncomponentcurrentstate-property"></a>Session. ComponentCurrentState, propriété

La propriété **ComponentCurrentState** de l’objet [**session**](session-object.md) est une propriété en lecture seule qui retourne l’état installé actuel du composant désigné. Pour les valeurs d’État, consultez la propriété [**ComponentRequestState**](session-componentrequeststate.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Valeur de la propriété

Nom de chaîne requis du composant demandé, clé primaire dans la table des composants.

## <a name="remarks"></a>Notes

Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**session**](session-object.md)
</dt> <dt>

[**Propriété ComponentRequestState**](session-componentrequeststate.md)
</dt> </dl>

 

 





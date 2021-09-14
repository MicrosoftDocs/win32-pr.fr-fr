---
description: Indique si le \_ \_ bloc try d’un gestionnaire de terminaisons se termine normalement. La fonction ne peut être appelée qu’à partir du \_ \_ bloc finally d’un gestionnaire de terminaisons.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114626"
---
# <a name="abnormaltermination-macro"></a>AbnormalTermination macro)

Indique si le bloc **\_ \_ try** d’un gestionnaire de terminaisons se termine normalement. La fonction ne peut être appelée qu’à partir du bloc **\_ \_ finally** d’un gestionnaire de terminaisons.

> [!Note]  
> Le compilateur d’optimisation Microsoft C/C++ interprète cette fonction comme un mot clé, et son utilisation en dehors de la syntaxe de gestion des exceptions appropriée génère une erreur du compilateur.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>Paramètres

Cette macro n’a pas de paramètres.

## <a name="return-value"></a>Valeur de retour

Si le bloc **\_ \_ try** s’est arrêté anormalement, la valeur de retour est différente de zéro.

Si le bloc **\_ \_ try** s’est arrêté normalement, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Le bloc **\_ \_ try** se termine normalement uniquement si l’exécution laisse le bloc séquentiellement après l’exécution de la dernière instruction dans le bloc. Les instructions (telles que **Return**, **goto**, **continue** ou **break**) qui forcent l’exécution à quitter le bloc **\_ \_ try** entraînent un arrêt anormal du bloc. C’est le cas même si une telle instruction est la dernière instruction du bloc **\_ \_ try** .

Un arrêt anormal d’un bloc **\_ \_ try** amène le système à parcourir tous les frames de pile pour déterminer si des gestionnaires de terminaison doivent être appelés. Cela peut entraîner l’exécution de centaines d’instructions. il est donc important d’éviter l’arrêt anormal d’un bloc **\_ \_ try** en raison d’une instruction **Return**, **goto**, **continue** ou **break** . Notez que ces instructions ne génèrent pas d’exception, même si l’arrêt est anormal.

Pour éviter un arrêt anormal, l’exécution doit se poursuivre jusqu’à la fin du bloc. Vous pouvez également exécuter l’instruction **\_ \_ Leave** . L’instruction **\_ \_ Leave** autorise l’arrêt immédiat du bloc **\_ \_ try** sans entraîner un arrêt anormal et une baisse des performances. Consultez la documentation de votre compilateur pour déterminer si l’instruction **\_ \_ Leave** est prise en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de gestion structurée des exceptions](structured-exception-handling-functions.md)
</dt> <dt>

[Vue d’ensemble de la gestion structurée des exceptions](structured-exception-handling.md)
</dt> </dl>

 

 





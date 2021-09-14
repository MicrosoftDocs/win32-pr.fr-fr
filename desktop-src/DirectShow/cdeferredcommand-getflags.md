---
description: La méthode GetFlags récupère les indicateurs de contexte associés à la commande différée.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: CDeferredCommand. GetFlags, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999297"
---
# <a name="cdeferredcommandgetflags-method"></a>CDeferredCommand. GetFlags, méthode

La `GetFlags` méthode récupère les indicateurs de contexte associés à la commande différée.

## <a name="syntax"></a>Syntaxe


```C++
short GetFlags();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l'une des valeurs suivantes :



| Code de retour                                                                                             | Description                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISPATCH ( \_ méthode)**</dt> </dl>         | Exécutez le membre en tant que méthode. Si une propriété porte le même nom, vous pouvez définir à la fois cet indicateur et l' \_ indicateur PROPERTYGET (Dispatch.<br/>                                               |
| <dl> <dt>**DISTRIBUER \_ PropertyGet (**</dt> </dl>    | Le membre est récupéré en tant que propriété ou membre de données.<br/>                                                                                                         |
| <dl> <dt>**DISTRIBUER \_ PROPERTYPUT**</dt> </dl>    | Le membre est modifié en tant que propriété ou membre de données.<br/>                                                                                                           |
| <dl> <dt>**DISTRIBUER \_ PROPERTYPUTREF**</dt> </dl> | Le membre est modifié via une assignation de référence, plutôt que comme une assignation de valeur. Cet indicateur est valide uniquement lorsque la propriété accepte une référence à un objet.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 





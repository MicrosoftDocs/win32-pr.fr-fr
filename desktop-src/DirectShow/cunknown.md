---
description: La classe CUnknown implémente l’interface IUnknown. la plupart des objets COM (component Object Model) dans DirectShow dérivent de CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: CUnknown, classe (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b6089f7f1c108a9b99ad4f1b16f4638b84d8d687a3590353c32841ccfff499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075993"
---
# <a name="cunknown-class"></a>CUnknown, classe

![hiérarchie de la classe CUnknown](images/cbase01.png)

La classe **CUnknown** implémente l’interface **IUnknown** . la plupart des objets COM (component Object Model) dans DirectShow dérivent de **CUnknown**.

Si vous implémentez un objet COM, vous souhaiterez peut-être le dériver de **CUnknown**. La dérivation à partir de **CUnknown** fournit une implémentation thread-safe, ce qui vous évite de rencontrer les problèmes d’implémentation de **IUnknown**.

Pour obtenir une présentation détaillée de l’utilisation de cette classe de base, consultez [How to implement IUnknown](how-to-implement-iunknown.md). Voici un bref résumé :

-   Incluez la macro [**Declare \_ IUnknown**](declare-iunknown.md) dans la section public de votre définition de classe. Cette macro déclare les trois méthodes de l’interface **IUnknown** .
-   Substituez la méthode [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) pour prendre en charge les interfaces autres que **IUnknown**. Dans cette méthode, appelez la fonction [**GetInterface**](getinterface.md) pour récupérer les pointeurs d’interface.
-   Dans votre constructeur de classe, appelez la méthode de constructeur **CUnknown** .



| Variables membres protégées                                                  | Description                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**m \_ cref**](cunknown-m-cref.md)                                          | Nombre de références.                                                   |
| M&#233;thodes publiques                                                              | Description                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | Méthode de constructeur.                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | Méthode de destructeur. Virtuels.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Obtient un pointeur vers le contrôle **IUnknown**.                    |
| Méthodes INonDelegatingUnknown                                               | Description                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | Incrémente le décompte de références.                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | Récupère un pointeur d’interface et incrémente le décompte de références. |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | Décrémente le décompte de références.                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Classes de base](directshow-base-classes.md)
</dt> </dl>

 

 





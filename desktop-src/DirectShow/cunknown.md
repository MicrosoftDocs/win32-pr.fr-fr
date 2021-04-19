---
description: La classe CUnknown implémente l’interface IUnknown. La plupart des objets COM (Component Object Model) dans DirectShow dérivent de CUnknown.
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
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541444"
---
# <a name="cunknown-class"></a>CUnknown, classe

![hiérarchie de la classe CUnknown](images/cbase01.png)

La classe **CUnknown** implémente l’interface **IUnknown** . La plupart des objets COM (Component Object Model) dans DirectShow dérivent de **CUnknown**.

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
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de base DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 





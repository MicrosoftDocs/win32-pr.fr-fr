---
title: Règles d’implémentation de QueryInterface
description: Règles d’implémentation de QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0d0df2d0382c670ed6f4a323f55dcdd1b187430282abe6699da186e574e390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047867"
---
# <a name="rules-for-implementing-queryinterface"></a>Règles d’implémentation de QueryInterface

Trois règles principales régissent l’implémentation de la méthode [**IUnknown :: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un objet com :

-   Les objets doivent avoir une identité.
-   L’ensemble d’interfaces sur une instance d’objet doit être statique.
-   Il doit être possible d’interroger avec succès toute interface sur un objet à partir d’une autre interface.

## <a name="objects-must-have-identity"></a>Les objets doivent avoir une identité

Pour toute instance d’objet donnée, un appel à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) avec IID \_ IUnknown doit toujours retourner la même valeur de pointeur physique. Cela vous permet d’appeler **QueryInterface** sur deux interfaces quelconques et de comparer les résultats pour déterminer s’ils pointent vers la même instance d’un objet.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>L’ensemble d’interfaces sur une instance d’objet doit être statique

L’ensemble d’interfaces accessible sur un objet via [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) doit être statique et non dynamique. En particulier, si **QueryInterface** retourne \_ la valeur OK pour un IID donné une seule fois, il ne doit jamais retourner e \_ nointerface lors des appels suivants sur le même objet. Si **QueryInterface** retourne e \_ nointerface pour un IID donné, les appels suivants pour le même IID sur le même objet ne doivent jamais retourner la valeur \_ OK.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Il doit être possible d’interroger avec succès toute interface sur un objet à partir d’une autre interface

Autrement dit, en fonction du code suivant :

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

les règles suivantes s’appliquent :

-   Si vous avez un pointeur vers une interface sur un objet, un appel semblable au suivant à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour cette même interface doit être concluant :

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Si un appel à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour un deuxième pointeur d’interface se déroule correctement, un appel à **QueryInterface** à partir de ce pointeur pour la première interface doit également être effectué. Si la commande pB a été obtenue avec succès, les conditions suivantes doivent également réussir :

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Toute interface doit être en mesure d’interroger une autre interface sur un objet. Si la valeur pB a été obtenue avec succès et que vous interrogez avec succès une troisième interface (IC) à l’aide de ce pointeur, vous devez également être en mesure d’interroger avec succès à l’aide du premier pointeur, pA. Dans ce cas, la séquence suivante doit être effectuée :

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Les implémentations d’interface doivent conserver un compteur de références de pointeur en suspens à toutes les interfaces sur un objet donné. Vous devez utiliser un **entier non signé** pour le compteur.

Si un client a besoin de savoir que les ressources ont été libérées, il doit utiliser une méthode dans une interface sur l’objet avec une sémantique de niveau supérieur avant d’appeler [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation et implémentation de IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 
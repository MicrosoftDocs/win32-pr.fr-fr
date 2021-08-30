---
description: 'La classe CTransInPlaceFilter est conçue pour les filtres de transformation sur place, qui sont des filtres qui modifient les données d’entrée au lieu de copier les données dans les mémoires tampons. Pour utiliser cette classe, dérivez une nouvelle classe de CTransInPlaceFilter et implémentez les méthodes suivantes :'
ms.assetid: 3d6d5436-f280-4e36-96e4-40161e8115c2
title: CTransInPlaceFilter, classe (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 575a4433318a2c956f4585270b0ff329f40cdff37f6b9f6553b895b58c6a3e34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086972"
---
# <a name="ctransinplacefilter-class"></a>CTransInPlaceFilter, classe

![hiérarchie de la classe ctransinplacefilter](images/tsip03.png)

La `CTransInPlaceFilter` classe est conçue pour les filtres de transformation sur place, qui sont des filtres qui modifient les données d’entrée au lieu de copier les données dans les mémoires tampons. Pour utiliser cette classe, dérivez une nouvelle classe de `CTransInPlaceFilter` et implémentez les méthodes suivantes :

-   [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md)
-   [**CTransInPlaceFilter :: Transform**](ctransinplacefilter-transform.md)

Cette classe utilise la classe [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) pour sa broche d’entrée et la classe [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pour sa broche de sortie. En règle générale, vous n’avez pas besoin de remplacer ces classes pin. Le filtre crée les deux codes confidentiels dans la méthode [**CTransInPlaceFilter :: GetPin**](ctransinplacefilter-getpin.md) . Si vous remplacez les classes de code confidentiel, vous devez remplacer **GetPin** pour créer vos codes confidentiels personnalisés.

Cette classe est conçue afin que le type d’entrée corresponde toujours au type de sortie. Dans la mesure du possible, le filtre utilise un allocateur unique pour les deux connexions de pin.

## <a name="preferred-media-types"></a>Types de médias préférés

Si la broche de sortie est déjà connectée, la broche d’entrée offre les types préférés du filtre en aval. (En fait, il retourne simplement l’objet énumérateur du filtre en aval.) Dans le cas contraire, il n’a aucun type préféré. La broche de sortie a le même comportement, mais dans l’ordre inverse : si la broche d’entrée est déjà connectée, la broche de sortie offre les types préférés du filtre en amont. Dans le cas contraire, il n’a aucun type préféré

## <a name="pin-connections"></a>Épingler les connexions

Lorsqu’un code confidentiel se connecte, le filtre reconnecte généralement l’autre code confidentiel, pour s’assurer que les deux codes confidentiels utilisent le même type de média et le même allocateur. (Le mécanisme de reconnexion des codes confidentiels est décrit dans [reconnexion des codes confidentiels](reconnecting-pins.md).) Deux scénarios sont possibles : soit la broche d’entrée se connecte en premier, soit la broche de sortie se connecte en premier.

Supposons que la broche d’entrée se connecte en premier. Les étapes suivantes se produisent :

1.  La broche d’entrée appelle la méthode [**CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type de média.
2.  Le filtre amont sélectionne un allocateur. À ce stade, la broche d’entrée n’a pas de spécifications d’allocateur et accepte tout Allocator pour la connexion. Si le filtre amont demande un allocateur, le code pin en crée un nouveau. Pour les raisons décrites brièvement, cet allocateur ne sera pas utilisé dans la connexion finale. Elle est fournie uniquement pour vous aider à terminer cette étape du processus de connexion.

Plus tard, lorsque la broche de sortie se connecte :

1.  La broche de sortie appelle la méthode [**CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type de média. Elle appelle également [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur le filtre amont. Cela permet de s’assurer que la broche d’entrée peut modifier son type de média pour qu’elle corresponde.
2.  La broche de sortie appelle la méthode [**CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type de média. Elle appelle également [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur le filtre amont. Cela permet de s’assurer que la broche d’entrée peut modifier son type de média pour qu’elle corresponde.
3.  La broche de sortie appelle la méthode [**CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type de média. Elle appelle également [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur le filtre amont. Cela permet de s’assurer que la broche d’entrée peut modifier son type de média pour qu’elle corresponde.
4.  Cette fois-ci, la méthode [**GetAllocator**](ctransinplaceinputpin-getallocator.md) de la broche d’entrée retourne l’allocateur en aval et [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) retourne les exigences d’allocateur du filtre en aval. La broche d’entrée accepte l’allocation que le filtre en amont choisit.
5.  Cette fois-ci, la méthode [**GetAllocator**](ctransinplaceinputpin-getallocator.md) de la broche d’entrée retourne l’allocateur en aval et [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) retourne les exigences d’allocateur du filtre en aval. La broche d’entrée accepte l’allocation que le filtre en amont choisit.

Examinons maintenant le scénario opposé, où la broche de sortie est le premier code pin à connecter.

1.  La broche de sortie appelle la méthode [**CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type de média.
2.  Il sélectionne un allocateur, préférant utiliser l’allocateur du filtre en aval.

Ensuite, lorsque la broche d’entrée se connecte :

1.  La broche d’entrée vérifie le type de média en appelant [**CheckInputType**](ctransformfilter-checkinputtype.md) sur le filtre et en appelant [**QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche de sortie du filtre en aval.
2.  Si le type d’entrée ne correspond pas au type de sortie, le filtre reconnecte la broche de sortie.
3.  Le filtre amont sélectionne un allocateur. La méthode [**GetAllocator**](ctransinplaceinputpin-getallocator.md) de la broche d’entrée retourne l’allocateur en aval, et la broche d’entrée accepte l’allocation que le filtre en amont sélectionne.
4.  Le filtre utilise le même allocateur pour la connexion en aval, en remplaçant éventuellement l’allocateur en aval d’origine.

Cette séquence d’événements change légèrement si l’un des allocateurs impliqués est en lecture seule, car l’allocateur en aval doit être accessible en écriture. Dans ce cas, le filtre peut utiliser deux allocations distinctes.

Pour plus d’informations sur l’utilisation de cette classe, consultez [écriture de filtres de transformation](writing-transform-filters.md).



| Variables membres protégées                                                        | Description                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**m \_ bModifiesData**](ctransinplacefilter-m-bmodifiesdata.md)                   | Indique si le filtre modifie les exemples de données.                           |
| Méthodes protégées                                                                 | Description                                                                      |
| [**Copier**](ctransinplacefilter-copy.md)                                          | Copie un échantillon de média.                                                           |
| [**InputPin**](ctransinplacefilter-inputpin.md)                                  | Récupère un pointeur vers la broche d’entrée du filtre.                                   |
| [**OutputPin**](ctransinplacefilter-outputpin.md)                                | Récupère un pointeur vers la broche de sortie du filtre.                                  |
| [**TypesMatch**](ctransinplacefilter-typesmatch.md)                              | Détermine si le type de média d’entrée correspond au type de média de sortie.           |
| [**UsingDifferentAllocators**](ctransinplacefilter--usingdifferentallocators.md) | Détermine si les broches d’entrée et de sortie utilisent des allocateurs différents.     |
| M&#233;thodes publiques                                                                    | Description                                                                      |
| [**CTransInPlaceFilter**](ctransinplacefilter-ctransinplacefilter.md)            | Méthode de constructeur.                                                              |
| [**GetPin**](ctransinplacefilter-getpin.md)                                      | Récupère un code confidentiel.                                                                 |
| [**GetMediaType**](ctransinplacefilter-getmediatype.md)                          | Récupère un type de média par défaut pour la broche de sortie.                             |
| [**DecideBufferSize**](ctransinplacefilter-decidebuffersize.md)                  | Définit les exigences de mémoire tampon de la broche de sortie.                                       |
| [**CheckTransform**](ctransinplacefilter-checktransform.md)                      | Vérifie si un type de média d’entrée est compatible avec un type de média de sortie.      |
| [**CompleteConnect**](ctransinplacefilter-completeconnect.md)                    | Termine une connexion de code confidentiel.                                                      |
| [**Çoive**](ctransinplacefilter-receive.md)                                    | Reçoit un exemple de support, le traite et le remet au filtre en aval. |
| Méthodes virtuelles pures                                                              | Description                                                                      |
| [**Transform**](ctransinplacefilter-transform.md)                                | Transforme un échantillon en place.                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 





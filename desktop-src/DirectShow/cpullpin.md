---
description: La classe CPullPin fournit la prise en charge des codes confidentiels d’entrée qui extraient les données via l’interface IAsyncReader.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: CPullPin, classe (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d70217fa60afdae3f588f98ecbe61a728ace6ec0b0d78859f55cd241cbc00e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330843"
---
# <a name="cpullpin-class"></a>CPullPin, classe

![hiérarchie de la classe cpullpin](images/pulpin01.png)

La `CPullPin` classe fournit la prise en charge des codes confidentiels d’entrée qui extraient les données via l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Utilisez cette classe si vous implémentez un filtre qui utilise le modèle d’extraction pour demander des données à partir du filtre en amont. pour plus d’informations, consultez Flow de données dans le filtre Graph et le modèle d’extraction.

Cette classe ne dérive pas de **CBasePin** ou implémente l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) , et certains noms de méthode sont en conflit avec **IPIN**. il est donc préférable de l’utiliser en tant qu’objet d’assistance dans votre code confidentiel. Pour utiliser cette classe, procédez comme suit :

1.  Dérivez une classe d’assistance de `CPullPin` et dérivez une classe de code confidentiel d’entrée à partir de **CBasePin**. Déclarez une instance de l' `CPullPin` objet en tant que variable membre de la classe pin.
2.  Substituez la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) pour appeler [**CPullPin :: connecter**](cpullpin-connect.md). Cette méthode interroge l’autre code confidentiel pour **IAsyncReader**.
3.  Substituez la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) pour appeler [**CPullPin ::D éconnecter**](cpullpin-disconnect.md).
4.  Substituez la méthode [**CBasePin :: active**](cbasepin-active.md) pour appeler [**CPullPin :: active**](cpullpin-active.md). Cette méthode démarre un thread de travail qui extrait des exemples du filtre en amont. Lorsque les codes confidentiels se connectent, vous pouvez spécifier si vous souhaitez que le thread de travail effectue des requêtes de lecture asynchrones ou synchrones.
5.  Substituez la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) pour appeler [**CPullPin :: inactive**](cpullpin-inactive.md). Cette méthode arrête le thread de travail.
6.  Implémentez la méthode [**CPullPin :: Receive**](cpullpin-receive.md) virtuelle pure pour traiter les échantillons entrants et les remettre en aval.
7.  Pour définir les positions arrêter et démarrer, ou pour rechercher le flux, appelez la méthode [**CPullPin :: Seek**](cpullpin-seek.md) . Cette méthode suspend le thread de travail et vide le graphique de filtre.
8.  Implémentez les méthodes Virtual [**CPullPin :: EndOfStream**](cpullpin-endofstream.md), [**CPullPin :: BeginFlush**](cpullpin-beginflush.md)et [**CPullPin :: EndFlush**](cpullpin-endflush.md) pures, comme décrit dans les notes pour ces méthodes.
9.  Implémentez la méthode pure virtual [**CPullPin :: OnError**](cpullpin-onerror.md) pour gérer les erreurs de diffusion en continu.



| Variables membres publiques                             | Description                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ pAlloc**](cpullpin-m-palloc.md)              | Pointeur vers l’interface **IMemAllocator** de l’allocateur de mémoire.                   |
| M&#233;thodes publiques                                      | Description                                                                           |
| [**Actif**](cpullpin-active.md)                   | Crée un thread de travail qui extrait des données de la broche de sortie.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Tronque une valeur à une limite d’alignement spécifiée.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Arrondit une valeur à une limite d’alignement spécifiée.                                  |
| [**Connecter**](cpullpin-connect.md)                 | Termine une connexion à la broche de sortie.                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | Méthode de constructeur.                                                                   |
| [**~ CPullPin**](cpullpin--cpullpin.md)             | Méthode de destructeur. Virtuels.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Négocie un allocateur avec la broche de sortie. Virtuels.                                 |
| [**Déconnecter**](cpullpin-disconnect.md)           | Présente la connexion avec la broche de sortie.                                             |
| [**Macauley**](cpullpin-duration.md)               | Récupère la durée du flux.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Retourne un pointeur vers l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) de la broche de sortie. |
| [**Inactive**](cpullpin-inactive.md)               | Arrête le thread de travail qui extrait les données de la broche de sortie.                     |
| [**Seek**](cpullpin-seek.md)                       | Définit les positions de début et de fin du flux.                                      |
| Méthodes virtuelles pures                                | Description                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | Informe le filtre propriétaire de la vidange des filtres en aval.                            |
| [**EndFlush**](cpullpin-endflush.md)               | Informe le filtre propriétaire pour terminer une opération de vidage.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Appelé après que l’objet a effectué le dernier échantillon.                                     |
| [**OnError**](cpullpin-onerror.md)                 | Appelée si une erreur se produit pendant la diffusion en continu.                                           |
| [**Çoive**](cpullpin-receive.md)                 | Appelé lorsque l’objet reçoit un échantillon de média à partir de la broche de sortie.                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 





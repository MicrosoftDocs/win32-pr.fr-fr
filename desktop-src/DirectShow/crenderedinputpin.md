---
description: La classe CRenderedInputPin est une classe de base pour l’implémentation d’une broche d’entrée sur un convertisseur.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: CRenderedInputPin, classe (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 139b0ebd887dc81efd19953d48f3caa8fd6377acde8723de23178ee7a0278c8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585293"
---
# <a name="crenderedinputpin-class"></a>CRenderedInputPin, classe

![hiérarchie de la classe crenderedinputpin](images/rbase04.png)

La classe **CRenderedInputPin** est une classe de base pour l’implémentation d’une broche d’entrée sur un convertisseur. Cette classe est conçue pour les filtres de convertisseur qui ne dérivent pas de la classe [**CBaseRenderer**](cbaserenderer.md) . (Les filtres qui dérivent de **CBaseRenderer** doivent utiliser la classe [**CRendererInputPin**](crendererinputpin.md) pour la broche d’entrée.)

Pour utiliser cette classe, vous devez effectuer au moins ce qui suit :

-   Déclarez une nouvelle classe pin qui hérite de **CRenderedInputPin**.
-   Dans votre classe pin, déclarez un objet de section critique pour conserver le verrou de streaming. Vous pouvez utiliser la classe [**CCritSec**](ccritsec.md) à cet effet. Pour plus d’informations, consultez [threads et sections critiques](threads-and-critical-sections.md).
-   Remplacez [**CRenderedInputPin :: EndOfStream**](crenderedinputpin-endofstream.md) pour conserver le verrou de streaming.
-   Implémentez les méthodes [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md)et [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) .
-   Dans votre filtre, implémentez [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) pour retourner une instance de votre classe pin.

Vous pouvez utiliser cette classe dans un convertisseur qui a plusieurs broches d’entrée. Cette classe hérite de la classe [**CBaseInputPin**](cbaseinputpin.md) .



| Variables membres protégées                                            | Description                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**m \_ bAtEndOfStream**](crenderedinputpin-m-batendofstream.md)       | Indique si la fin du flux a été atteinte.                                                         |
| [**m \_ bCompleteNotified**](crenderedinputpin-m-bcompletenotified.md) | indique si le code pin a envoyé un événement d' [**\_ achèvement ce**](ec-complete.md) à la Graph du gestionnaire de filtres. |
| M&#233;thodes publiques                                                        | Description                                                                                                  |
| [**Actif**](crenderedinputpin-active.md)                            | Notifie le code confidentiel que le filtre est maintenant actif.                                                              |
| [**CRenderedInputPin**](crenderedinputpin-crenderedinputpin.md)      | Méthode de constructeur.                                                                                          |
| [**Exécuter**](crenderedinputpin-run.md)                                  | Notifie le code confidentiel que le filtre est en cours d’exécution.                                                             |
| Méthodes IPin                                                          | Description                                                                                                  |
| [**EndFlush**](crenderedinputpin-endflush.md)                        | Termine une opération de vidage.                                                                                      |
| [**EndOfStream**](crenderedinputpin-endofstream.md)                  | Indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue tant que le filtre n’a pas reçu une nouvelle commande Run.            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amextra. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 





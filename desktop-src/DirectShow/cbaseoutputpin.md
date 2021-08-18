---
description: La classe CBaseOutputPin est une classe de base abstraite qui implémente une broche de sortie.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: CBaseOutputPin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67a4051f904b27b75273d553e1d0604b068b3910fbfb322b5a2df716c996a1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872583"
---
# <a name="cbaseoutputpin-class"></a>CBaseOutputPin, classe

![hiérarchie de la classe cbaseoutputpin](images/filter06.png)

La `CBaseOutputPin` classe est une classe de base abstraite qui implémente une broche de sortie.

Cette classe dérive de [**CBasePin**](cbasepin.md). Il diffère de **CBasePin** en respectant les points suivants :

-   Il se connecte uniquement aux broches d’entrée qui prennent en charge l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Il prend en charge le transport de mémoire locale par le biais de l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .
-   Elle rejette les notifications de fin de flux, de vidage et de segmentation. (Ils ne doivent pas être envoyés à une broche de sortie.)
-   Il fournit des méthodes pour fournir des exemples en aval.

Lorsque le code confidentiel se connecte, il demande un allocateur de mémoire à partir de la broche d’entrée. En échec, elle crée un nouvel objet allocateur. La broche de sortie est chargée de définir les propriétés de l’allocateur. Pour ce faire, il utilise la méthode virtuelle pure [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md). Substituez cette méthode dans votre classe dérivée. Si la broche d’entrée a des exigences de mémoire tampon, elles sont passées à la méthode **DecideBufferSize** .

Appelez la méthode [**CBaseOutputPin :: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) pour obtenir un exemple de support vide. Appelez la méthode [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md) pour remettre des exemples en aval.

Votre classe dérivée doit substituer la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure pour valider le type de média lors des connexions de code confidentiel.



| Variables membres protégées                                      | Description                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseoutputpin-m-pallocator.md)            | Pointeur vers l’allocateur de mémoire.                                           |
| [**m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md)              | Pointeur vers la broche d’entrée connectée à ce code confidentiel.                            |
| M&#233;thodes publiques                                                  | Description                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | Méthode de constructeur.                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | Termine une connexion à une broche d’entrée. Virtuels.                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | Sélectionne un allocateur de mémoire. Virtuels.                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Récupère un exemple de média qui contient une mémoire tampon vide. Virtuels.           |
| [**Remettre**](cbaseoutputpin-deliver.md)                       | Remet un échantillon de média à la broche d’entrée connectée. Virtuels.               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | Crée un allocateur de mémoire. Virtuels.                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | Détermine si une connexion de code confidentiel est appropriée.                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | Libère le code confidentiel d’une connexion.                                        |
| [**Actif**](cbaseoutputpin-active.md)                         | Notifie le code confidentiel que le filtre est maintenant actif.                            |
| [**Inactive**](cbaseoutputpin-inactive.md)                     | Notifie le code confidentiel que le filtre n’est plus actif.                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | Fournit une notification de fin de flux à la broche d’entrée connectée. Virtuels. |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | Demande la broche d’entrée connectée pour commencer une opération de vidage. Virtuels.      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | Demande la broche d’entrée connectée pour terminer une opération de vidage. Virtuels.        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | Remet une notification de nouveau segment à la broche d’entrée connectée. Virtuels.   |
| Méthodes virtuelles pures                                            | Description                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | Définit les exigences de la mémoire tampon.                                              |
| Méthodes IPin                                                    | Description                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | Commence une opération de vidage.                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | Termine une opération de vidage.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Notifie le code confidentiel qu’aucune donnée supplémentaire n’est attendue.                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 





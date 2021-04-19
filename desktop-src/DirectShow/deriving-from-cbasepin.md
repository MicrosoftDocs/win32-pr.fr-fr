---
description: Dérivation à partir de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Dérivation à partir de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515764"
---
# <a name="deriving-from-cbasepin"></a>Dérivation à partir de CBasePin

Pour implémenter un code confidentiel à l’aide de [**CBasePin**](cbasepin.md), vous devez dériver une nouvelle classe de la classe de base et substituer plusieurs de ses méthodes. Vous devez substituer les méthodes suivantes :

-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Vous devrez probablement remplacer ces méthodes supplémentaires :

-   [**CBasePin :: actif**](cbasepin-active.md)
-   [**CBasePin::BreakConnect**](cbasepin-breakconnect.md)
-   [**CBasePin::CheckConnect**](cbasepin-checkconnect.md)
-   [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md)
-   [**CBasePin :: EndOfStream**](cbasepin-endofstream.md)
-   [**CBasePin :: inactif**](cbasepin-inactive.md)
-   [**CBasePin :: Notify**](cbasepin-notify.md)
-   [**CBasePin :: Run**](cbasepin-run.md)

Enfin, vous devez implémenter les méthodes [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) et [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

Certaines de ces méthodes sont implémentées dans les classes de base qui dérivent de **CBasePin**, telles que [**CBaseInputPin**](cbaseinputpin.md) et [**CBaseOutputPin**](cbaseoutputpin.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 




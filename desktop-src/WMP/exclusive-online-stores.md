---
title: Magasins en ligne exclusifs
description: Magasins en ligne exclusifs
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player Online stores, exclusif
- magasins en ligne, exclusifs
- tapez 1 magasins en ligne, exclusif
- tapez 2 magasins en ligne, exclusif
- magasins en ligne exclusifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511058"
---
# <a name="exclusive-online-stores"></a>Magasins en ligne exclusifs

Avec le lecteur Windows Media 11, une application qui incorpore le contrôle du lecteur à distance peut spécifier un magasin en ligne exclusif. Dans ce cas, le sélecteur de service dans le lecteur Windows Media est désactivé et seule la Banque en ligne spécifiée est disponible pour l’utilisateur. En outre, le lecteur Windows Media adopte la couleur spécifiée par l’élément **Color** du document serviceInfo de la boutique en ligne exclusive.

Pour spécifier un magasin en ligne exclusif, une application doit ajouter ExclusiveService :*keyName* à la fin de la chaîne qu’elle retourne à partir de [IWMPRemoteMediaServices :: GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Par exemple, supposons que Proseware est le nom de clé donné à un magasin en ligne particulier. Si **GetServiceType** retourne la chaîne « Remote ExclusiveService : Proseware », le Proseware sera le seul magasin en ligne disponible dans le contrôle de lecteur incorporé à distance.

Une application peut limiter le lecteur Windows Media à une boutique en ligne exclusive uniquement si le lecteur Windows Media n’est pas déjà en cours d’exécution lorsque l’application est lancée. Il incombe à l’application d’informer l’utilisateur qu’il doit fermer le lecteur Windows Media avant d’exécuter l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





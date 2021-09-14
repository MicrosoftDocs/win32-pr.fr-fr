---
title: Magasins en ligne exclusifs
description: Magasins en ligne exclusifs
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Lecteur Windows Media les magasins en ligne, exclusif
- magasins en ligne, exclusifs
- tapez 1 magasins en ligne, exclusif
- tapez 2 magasins en ligne, exclusif
- magasins en ligne exclusifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217108"
---
# <a name="exclusive-online-stores"></a>Magasins en ligne exclusifs

avec Lecteur Windows Media 11, une application qui incorpore le contrôle du lecteur à distance peut spécifier un magasin en ligne exclusif. dans ce cas, le sélecteur de service dans Lecteur Windows Media est désactivé, et seule la banque en ligne spécifiée est disponible pour l’utilisateur. de plus, Lecteur Windows Media adopte la couleur spécifiée par l’élément **color** du document ServiceInfo de la boutique en ligne exclusive.

Pour spécifier un magasin en ligne exclusif, une application doit ajouter ExclusiveService :*keyName* à la fin de la chaîne qu’elle retourne à partir de [IWMPRemoteMediaServices :: GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype). Par exemple, supposons que Proseware est le nom de clé donné à un magasin en ligne particulier. Si **GetServiceType** retourne la chaîne « Remote ExclusiveService : Proseware », le Proseware sera le seul magasin en ligne disponible dans le contrôle de lecteur incorporé à distance.

une application peut limiter Lecteur Windows Media à un magasin en ligne exclusif si Lecteur Windows Media n’est pas déjà en cours d’exécution lors du lancement de l’application. il incombe à l’application d’informer l’utilisateur qu’il doit fermer Lecteur Windows Media avant d’exécuter l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





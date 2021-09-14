---
title: Pages de découverte
description: Pages de découverte
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Lecteur Windows Media des magasins en ligne, des pages de découverte
- magasins en ligne, pages de découverte
- tapez 1 magasins en ligne, pages de découverte
- bibliothèque de Lecteur Windows Media, pages de découverte
- bibliothèque, pages de découverte
- pages de découverte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349b0e7238aa6d59b56f9035a3c02a5b3ff7b7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008458"
---
# <a name="discovery-pages"></a>Pages de découverte

si le magasin en ligne actif est un magasin de type 1, Lecteur Windows Media affiche le contenu du magasin dans son interface utilisateur. Le contrôle Tree-View de la bibliothèque a un nœud pour le magasin en ligne. quand l’utilisateur clique sur ce nœud ou sur l’un de ses sous-nœuds, Lecteur Windows Media affiche le contenu du magasin en ligne dans le volet d’informations.

lorsque l’utilisateur interagit avec le contenu de la boutique en ligne dans le contrôle arborescence ou dans le volet d’informations, Lecteur Windows Media affiche les pages web, appelées *pages de découverte*, fournies par le magasin en ligne. Les pages de découverte fournissent des informations supplémentaires sur la musique au fur et à mesure que l’utilisateur parcourt le catalogue du magasin en ligne. les pages de découverte communiquent avec Lecteur Windows Media via les propriétés, les méthodes et les événements de l' [objet externe](external-object-for-type-1-online-stores.md).

chaque fois que Lecteur Windows Media modifie son affichage du contenu du magasin en ligne, il appelle [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate), implémenté par le plug-in du magasin en ligne, pour obtenir l’URL de la page de découverte à afficher avec la nouvelle vue.

la vue du contenu du magasin en ligne dans Lecteur Windows Media est caractérisée par cinq éléments d’information : tâche, type d’emplacement, id d’emplacement, type d’élément sélectionné et ID d’élément sélectionné. Lecteur Windows Media fournit ces cinq éléments à la **méthode GetTemplate** dans les paramètres *task*, *location*, *pContext*, *clickLocation* et *pClickContext* . Lecteur Windows Media rend ces cinq éléments disponibles pour les pages de découverte dans les propriétés *task*, *libraryLocationType*, *libraryLocationID*, *selectedItemType* et *selectedItemID* de l’objet **External** . pour plus d’informations sur la façon dont Lecteur Windows Media spécifie son affichage du contenu du magasin en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).

en plus de permettre à une page de découverte de communiquer avec Lecteur Windows Media, l’objet **externe** permet à une page de découverte de communiquer avec le plug-in du magasin en ligne. lorsque cela se produit, Lecteur Windows Media agit comme un pont entre la page de découverte et le plug-in. Par exemple, la page découverte peut appeler [External. SendMessage](external-sendmessage.md) pour envoyer un message personnalisé au plug-in. Lecteur Windows Media reçoit cet appel de méthode et appelle à son tour [IWMPContentPartner :: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) pour transmettre le message au plug-in. Lorsque le plug-in a terminé le traitement du message, il appelle [IWMPContentPartnerCallback :: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete). Lecteur Windows Media notifie ensuite la page de découverte en déclenchant l’événement [External. OnSendMessageComplete](external-onsendmessagecomplete-event.md) .

L’objet **externe** permet également à une page de découverte de communiquer avec une autre page de découverte. Lorsque le script d’une page de découverte appelle [External. changeView](external-changeview.md), le script peut fournir une chaîne dans le paramètre *ViewParams* . Lecteur Windows Media n’interprète pas la chaîne *ViewParams* , mais rend la chaîne disponible à la page de découverte suivante dans la propriété [External. viewParameters](external-viewparameters.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Emplacement et élément sélectionné**](location-and-selected-item.md)
</dt> </dl>

 

 





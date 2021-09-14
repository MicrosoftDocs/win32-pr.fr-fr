---
title: Achat de contenu multimédia
description: Achat de contenu multimédia
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Lecteur Windows Media des magasins en ligne, achat de contenu multimédia
- magasins en ligne, achat de contenu multimédia
- tapez 1 magasins en ligne, achat de contenu multimédia
- magasins en ligne Lecteur Windows Media, achats de contenu multimédia
- magasins en ligne, achats de contenu multimédia
- tapez 1 magasins en ligne, achats de contenu multimédia
- contenu multimédia, achat
- achat de contenu multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013233"
---
# <a name="purchasing-media-content"></a>Achat de contenu multimédia

lorsque Lecteur Windows Media affiche du contenu musical dans l’arborescence de la bibliothèque, l’interface utilisateur comprend les éléments sur lesquels l’utilisateur peut cliquer pour acheter le contenu. Par exemple, l’utilisateur peut cliquer sur un bouton pour acheter une chanson individuelle ou acheter un album entier.

si le magasin en ligne actif est un magasin de Type 1, Lecteur Windows Media a accès aux tarifs suivi, album et liste dans le catalogue du magasin en ligne. Ces prix dans le catalogue sont des chaînes qui ont un format compris uniquement par le magasin en ligne. Lecteur Windows Media n’interprète pas les chaînes de prix ; elle les affiche simplement dans des éléments d’interface utilisateur tels que des boutons Acheter.

lorsque Lecteur Windows Media configure un achat pour un ensemble d’éléments multimédias, il transmet les id et les prix des éléments multimédias au plug-in du partenaire de contenu en appelant [IWMPContentPartner :: CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent). À ce stade, le plug-in peut inspecter les prix fournis par le joueur. Il s’agit des prix que l’utilisateur s’attend à payer ; autrement dit, les prix que le joueur affichait à l’utilisateur. En fonction des ID de support et des prix fournis par le joueur, le plug-in calcule un prix total, qu’il renvoie au joueur dans le paramètre *bstrTotalPrice* . Les prix que le joueur transmet à **CanBuySilent** fournissent le plug-in avec les informations, mais ils n’obligent pas le plug-in à retourner un prix total donné. Le plug-in peut calculer le prix total tel qu’il convient.

En plus de calculer le prix total d’un achat, **CanBuySilent** détermine si le purchace peut se poursuivre en mode silencieux. autrement dit, sans afficher de boîte de dialogue. si **CanBuySilent** retourne la **valeur True**, Lecteur Windows Media modifie simplement le texte sur le bouton acheter pour inviter l’utilisateur à confirmer l’achat. si **CanBuySilent** retourne la **valeur false**, Lecteur Windows Media affiche une boîte de dialogue qui invite l’utilisateur à confirmer l’achat. La boîte de dialogue fournit à l’utilisateur des informations qui résument le nombre d’albums, le nombre de pistes individuelles et le prix total (tel qu’il est retourné par le plug-in).

Une fois que l’utilisateur a confirmé l’achat, le lecteur appelle [IWMPContentPartner :: Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy). Cet appel de méthode fournit le plug-in avec la même liste de conteneurs de contenu que **CanBuySilent**. lors de l’appel de **Buy**, Lecteur Windows Media fournit également un cookie (simplement une valeur **DWORD** , unique pour la session) que le plug-in peut utiliser pour identifier la transaction. Une fois la transaction terminée, le plug-in doit appeler [IWMPContentPartnerCallback :: BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), en passant la valeur de cookie d’origine pour le paramètre *dwBuyCookie* , afin d’informer le lecteur que la transaction est terminée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 





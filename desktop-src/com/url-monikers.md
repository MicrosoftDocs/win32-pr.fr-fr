---
title: Monikers d’URL
description: L’architecture du moniker OLE fournit un modèle de programmation pratique pour l’utilisation des URL.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2a63f63d14dfe51c0b8c5c3727637e12a51356
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291855"
---
# <a name="url-monikers"></a>Monikers d’URL

L’architecture du moniker OLE fournit un modèle de programmation pratique pour l’utilisation des URL. L’architecture du moniker prend en charge l’analyse de nom extensible et complète par le biais de la fonction [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) et des interfaces [**IParseDisplayName**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) et [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , ainsi que des noms imprimables via la méthode [**IMoniker :: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) . L’interface **IMoniker** est la façon dont vous utilisez les URL que vous rencontrez, et la création de composants qui s’intègrent à l’architecture du moniker est la manière d’étendre les espaces de noms d’URL dans la pratique.

Une classe de moniker fournie par le système, le moniker d’URL, fournit une infrastructure pour la génération et l’utilisation de certaines URL. Étant donné que les URL voient souvent les ressources sur des réseaux à latence élevée, le moniker d’URL prend en charge la liaison asynchrone et synchrone. Le moniker d’URL ne prend pas actuellement en charge le [stockage asynchrone](/windows/desktop/Stg/asynchronous-storage).

Le diagramme suivant montre les composants impliqués dans l’utilisation de monikers d’URL. Tous ces composants doivent être familiers. (Consultez [monikers asynchrones](asynchronous-monikers.md).)

![Diagramme qui montre les composants impliqués dans l’utilisation des monikers U R L.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Comme pour tous les clients moniker, un utilisateur de monikers URL crée et conserve une référence au moniker ainsi qu’au contexte de liaison à utiliser pendant la liaison ([**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Pour prendre en charge la liaison asynchrone, le client peut implémenter un objet bind-statue-callback, qui implémente l’interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) , et l’inscrire auprès du contexte de liaison à l’aide de la fonction [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) . Cet objet recevra l’interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) du transport lors des appels à [**IBindStatusCallback :: OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

Le moniker d’URL identifie le protocole utilisé en analysant le préfixe d’URL, puis récupère l’interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) à partir de la couche de transport. Le client utilise **IBinding** pour prendre en charge la suspension, l’annulation et la hiérarchisation de l’opération de liaison. L’objet de rappel reçoit également la notification de progression via [**IBindStatusCallback :: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), la notification de disponibilité des données via [**IBindStatusCallback :: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))et diverses autres notifications de couche de transport sur l’état de la liaison. Le moniker d’URL ou des couches de transport spécifiques peuvent également demander des informations étendues du client via **IBindStatusCallback :: QueryInterface**, ce qui permet au client de fournir des informations spécifiques au protocole qui affecteront l’opération de liaison.

Pour plus d'informations, voir les rubriques suivantes :

-   [Synchronisation des rappels](callback-synchronization.md)
-   [Négociation de type de média](media-type-negotiation.md)
-   [Fonctions du moniker d’URL](url-moniker-api-functions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers asynchrones](asynchronous-monikers.md)
</dt> <dt>

[À propos des monikers d’URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 
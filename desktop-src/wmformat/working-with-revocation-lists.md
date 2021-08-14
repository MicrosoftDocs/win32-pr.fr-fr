---
title: Utilisation des listes de révocation
description: Utilisation des listes de révocation
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- Windows Media Format SDK, listes de révocation
- ASF (Advanced Systems Format), listes de révocation
- ASF (format des systèmes avancés), listes de révocation
- listes de révocation
- gestion des droits numériques (DRM), listes de révocation
- DRM (gestion des droits numériques), listes de révocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d022b9b55a1a14b147d76d289efeac956bae8f1858d155f138efa579d533fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194878"
---
# <a name="working-with-revocation-lists"></a>Utilisation des listes de révocation

Pour répondre aux violations de sécurité et garantir que les applications de lecteur connues pour être endommagées ou compromises ne peuvent pas lire ou utiliser des fichiers protégés, chaque licence émise contient une liste de révocation. Une liste de révocation contient les certificats d’application de toutes les applications de lecteur connues pour être endommagées ou endommagées. Lors de la réception d’une nouvelle licence, le composant DRM de l’application du lecteur recherche une liste de révocation. Si une version plus récente que celle actuellement présente sur l’ordinateur est trouvée, la liste la plus récente est stockée. La prochaine fois que le consommateur lit un fichier ASF protégé, le composant DRM compare l’application de lecteur à la liste de révocation. Si l’application de lecteur est révoquée, le composant DRM envoie un message d’erreur à l’application.

Les applications de lecteur peuvent recevoir un message d’erreur de révocation dans les scénarios suivants :

-   Le message d’erreur est reçu après que l’application a appelé la méthode [**IWMDRMReader :: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) pour un fichier protégé. L’appel échoue avec le code **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ révoqué, qui est fourni à la fonction de rappel **OnStatus** avec l’état de la licence d' \_ acquisition WMT \_ . Si ce code **HRESULT** est ignoré, des erreurs continuent de se produire.
-   Le message d’erreur est reçu lorsque l’application crée le lecteur compatible DRM et appelle la méthode [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) pour un fichier protégé. L’appel échoue avec le code **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ révoqué, qui est fourni à la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) avec l' \_ état ouvert de WMT. Quand une application de lecteur reçoit ce message d’erreur, l’application doit avertir les utilisateurs finaux et leur permettre de restaurer les fonctionnalités sur leur lecteur. Par exemple, l’application peut ouvrir une URL où les utilisateurs finaux peuvent télécharger une mise à niveau pour l’application compromise.

**Remarque** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Gestion des événements d’acquisition de licence**](handling-license-acquisition-events.md)
</dt> </dl>

 

 





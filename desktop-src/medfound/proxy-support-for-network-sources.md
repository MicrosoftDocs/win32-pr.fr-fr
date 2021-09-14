---
description: Prise en charge du proxy pour les sources réseau
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Prise en charge du proxy pour les sources réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231708"
---
# <a name="proxy-support-for-network-sources"></a>Prise en charge du proxy pour les sources réseau

Un serveur proxy est un serveur intermédiaire entre votre intranet et Internet, qui achemine les demandes de l’application cliente vers le serveur multimédia et récupère les fichiers à partir du serveur multimédia.

Media Foundation crée implicitement un objet *localisateur de proxy* quand une application cliente tente d’accéder à une URL source. L’objet localisateur de proxy expose l’interface [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) . Pendant la résolution de la source, Media Foundation vérifie la Banque de propriétés transmise à la méthode du programme de résolution source.

Si la Banque de propriétés contient la propriété [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) définie sur un objet de fabrique du localisateur de proxy implémenté par l’application, elle appelle la méthode [**IMFNetProxyLocatorFactory :: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) pour créer un localisateur de proxy avec des paramètres de configuration personnalisés.

Si la Banque de propriétés n’est pas définie, Media Foundation crée le localisateur de proxy avec la configuration par défaut. Ces paramètres sont les suivants :

-   Si la stratégie de l’utilisateur est définie, le localisateur de proxy utilise les paramètres spécifiés dans le registre.

-   Pour HTTP, le localisateur de proxy utilise les paramètres du proxy du navigateur.

-   Pour RTSP, le localisateur de proxy est configuré pour ignorer les serveurs proxy lors de la connexion au serveur multimédia.

Cette configuration par défaut peut être modifiée par l’application. Les rubriques suivantes contiennent des informations sur les paramètres de configuration d’un localisateur de proxy :

-   [Paramètres de Configuration du localisateur de Proxy](proxy-locator-configuration-settings.md)

-   [Comment configurer le localisateur de proxy](how-to-configure-the-proxy-locator.md)

Media Foundation Initialise le localisateur de proxy pour l’URL source spécifiée pour le programme de [résolution source](source-resolver.md). Le localisateur de proxy détecte un serveur proxy à utiliser en fonction des paramètres de configuration. Lorsque le localisateur de proxy tente de définir un serveur proxy, il enregistre le résultat de la réussite ou de l’échec dans le registre. Cette valeur est vérifiée lors du prochain processus de détection de proxy. Si un certain serveur proxy est connu pour avoir provoqué des échecs par le passé, le localisateur de proxy l’ignore.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs et propriétés](attributes-and-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




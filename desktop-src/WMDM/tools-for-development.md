---
title: Outils de développement
description: Outils de développement
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Gestionnaire de périphériques Windows Media, outils de développement
- Gestionnaire de périphériques, outils de développement
- Gestionnaire de périphériques Windows Media, certificats
- Gestionnaire de périphériques, certificats
- Gestionnaire de périphériques Windows Media, clés
- Gestionnaire de périphériques, clés
- Windows Media Gestionnaire de périphériques, bibliothèques
- Gestionnaire de périphériques, bibliothèques
- Windows Media Gestionnaire de périphériques, kit de développement logiciel (SDK)
- Gestionnaire de périphériques, kit de développement logiciel (SDK)
- SDK Windows Media Gestionnaire de périphériques
- SDK Gestionnaire de périphériques
- SDK du lecteur Windows Media
- Windows Media Format SDK
- SDK Windows Media Rights Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "106513747"
---
# <a name="tools-for-development"></a>Outils de développement

Cette section décrit les différents certificats et clés, bibliothèques et kits de développement logiciel (SDK) que vous devrez programmer à l’aide du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques.

Certificats et clés

Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques est fourni avec une paire clé/certificat de test (dans le fichier Key. c) qui peut être utilisée par une application ou un fournisseur de services pour utiliser les méthodes Windows Media Gestionnaire de périphériques sur du contenu non protégé. Cette paire clé/certificat permet à l’application ou au fournisseur de services d’utiliser la plupart des fonctionnalités de Gestionnaire de périphériques Windows Media.

Toutefois, pour développer une application ou un fournisseur de services qui peut gérer le contenu DRM protégé, vous devez demander un ou plusieurs certificats (chacun avec une clé) à partir de la page de gestion des [licences Windows Media](https://www.microsoft.com/licensing/default). Des certificats sont requis pour les applications ou objets suivants :

-   Les fournisseurs de services qui gèrent le contenu protégé par DRM requièrent un certificat de fournisseur de services Windows Media Gestionnaire de périphériques (et une clé)
-   Les applications qui transfèrent du contenu protégé par DRM requièrent un certificat de transfert Windows Media Gestionnaire de périphériques (et une clé)
-   Les applications qui lisent du contenu protégé par DRM requièrent un certificat DRM (et une clé).
-   Les composants de contrôle de licence requièrent un certificat de contrôle. Il est fourni par un service de contrôle de licence basé sur le kit de développement logiciel (SDK) Windows Media Rights Manager, qui peut être demandé sur la page Windows Media Licensing.

Bibliothèques et en-têtes

En plus des bibliothèques et des en-têtes mentionnés dans les [fichiers d’en-tête et de bibliothèque requis pour une application](required-library-and-header-files-for-an-application.md) ou les [bibliothèques et en-têtes requis pour un fournisseur de services](required-libraries-and-headers-for-a-service-provider.md), toute application ou plug-in précédemment lié à WMDRMSDK. lib pour appeler les fonctions du SDK Windows Media Format devrait maintenant être lié à WMDRMSDKStub. lib. Ce fichier de bibliothèque est utilisé pour accéder aux fichiers protégés par DRM. Vous pouvez également demander cette bibliothèque à partir de la page de gestion des licences Windows Media.

Kits de développement logiciel associés

Les kits de développement logiciel (SDK) Microsoft suivants fournissent des éléments dont vous pouvez avoir besoin pour concevoir des solutions pour appareils multimédias portables.



| SDK requis                     | Requis pour...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SDK Windows Media Gestionnaire de périphériques | Applications de lecteur multimédia pour ordinateur de bureau qui communiquent avec des appareils mobiles<br/> Applications de bureau qui peuvent échanger des fichiers ou des informations avec des appareils mobiles<br/> Objets COM de contrôle du lecteur Windows Media<br/> |
| SDK du lecteur Windows Media         | Plug-ins du lecteur Windows Media<br/> Objets COM de contrôle du lecteur Windows Media<br/> Apparences du lecteur Windows Media<br/>                                                                                                   |
| Windows Media Format SDK         | Lecteurs audio ou vidéo capables de créer ou de lire des fichiers (en particulier les fichiers ASF)<br/> Applications d’édition audio ou vidéo<br/>                                                                                               |
| SDK Windows Media Rights Manager | Applications ou plug-ins qui mesurent le nombre de jeux sur le bureau ou l’appareil.                                                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](getting-started.md)
</dt> </dl>

 

 






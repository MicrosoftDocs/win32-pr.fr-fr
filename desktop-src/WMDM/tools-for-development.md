---
title: Outils de développement
description: Outils de développement
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Gestionnaire de périphériques de média, outils de développement
- Gestionnaire de périphériques, outils de développement
- Windows Gestionnaire de périphériques de média, certificats
- Gestionnaire de périphériques, certificats
- Windows Gestionnaire de périphériques de média, clés
- Gestionnaire de périphériques, clés
- Windows Gestionnaire de périphériques de média, bibliothèques
- Gestionnaire de périphériques, bibliothèques
- Windows Gestionnaire de périphériques de média, kit de développement logiciel (SDK)
- Gestionnaire de périphériques, kit de développement logiciel (SDK)
- Windows SDK Media Gestionnaire de périphériques
- SDK Gestionnaire de périphériques
- Lecteur Windows Media SDK
- Windows Media Format SDK
- Windows Kit de développement logiciel (SDK) Media Rights Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e517a97246c2bf9b2ac5670a7cf696e714777a2f5926a37e1b2d37ecbe45c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031609"
---
# <a name="tools-for-development"></a>Outils de développement

cette section décrit les différents certificats et clés, bibliothèques et kits de développement logiciel (sdk) que vous devrez programmer à l’aide du kit de développement logiciel (sdk) Windows Media Gestionnaire de périphériques.

Certificats et clés

le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques est fourni avec une paire clé/certificat de test (dans le fichier key. c) qui peut être utilisée par une application ou un fournisseur de services pour utiliser les méthodes Windows Media Gestionnaire de périphériques sur du contenu non protégé. cette paire clé/certificat permet à l’application ou au fournisseur de services d’utiliser la plupart des fonctionnalités de Gestionnaire de périphériques de média Windows.

toutefois, pour développer une application ou un fournisseur de services pouvant gérer le contenu DRM protégé, vous devez demander un ou plusieurs certificats (chacun avec une clé) à partir de la Page de gestion des [licences des médias Windows](https://www.microsoft.com/licensing/default). Des certificats sont requis pour les applications ou objets suivants :

-   les fournisseurs de services qui gèrent le contenu protégé par DRM requièrent un certificat de fournisseur de services Windows Media Gestionnaire de périphériques (et une clé)
-   les Applications qui transfèrent du contenu protégé par DRM requièrent un certificat Windows Media Gestionnaire de périphériques transfer (et une clé)
-   Les applications qui lisent du contenu protégé par DRM requièrent un certificat DRM (et une clé).
-   Les composants de contrôle de licence requièrent un certificat de contrôle. ce service est fourni par un service de contrôle de licence basé sur le kit de développement logiciel (SDK) media Rights Manager Windows, qui peut être demandé sur la Page Windows media Licensing.

Bibliothèques et en-têtes

en plus des bibliothèques et des en-têtes mentionnés dans les [fichiers d’en-tête et de bibliothèque requis pour une application](required-library-and-header-files-for-an-application.md) ou les [bibliothèques et en-têtes requis pour un fournisseur de services](required-libraries-and-headers-for-a-service-provider.md), toute Application ou plug-in précédemment lié à WMDRMSDK. lib pour appeler Windows fonctions du SDK de Format multimédia doit maintenant être lié à WMDRMSDKStub. lib. Ce fichier de bibliothèque est utilisé pour accéder aux fichiers protégés par DRM. vous pouvez également demander cette bibliothèque à partir de la Page de gestion des licences des médias Windows.

Kits de développement logiciel associés

Les kits de développement logiciel (SDK) Microsoft suivants fournissent des éléments dont vous pouvez avoir besoin pour concevoir des solutions pour appareils multimédias portables.



| SDK requis                     | Requis pour...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows SDK Media Gestionnaire de périphériques | Applications de lecteur multimédia pour ordinateur de bureau qui communiquent avec des appareils mobiles<br/> Applications de bureau qui peuvent échanger des fichiers ou des informations avec des appareils mobiles<br/> Lecteur Windows Media les objets COM de contrôle<br/> |
| Lecteur Windows Media SDK         | plug-ins Lecteur Windows Media<br/> Lecteur Windows Media les objets COM de contrôle<br/> apparences de Lecteur Windows Media<br/>                                                                                                   |
| Windows Media Format SDK         | Lecteurs audio ou vidéo capables de créer ou de lire des fichiers (en particulier les fichiers ASF)<br/> Applications d’édition audio ou vidéo<br/>                                                                                               |
| Windows Kit de développement logiciel (SDK) Media Rights Manager | Applications ou plug-ins qui mesurent le nombre de jeux sur le bureau ou l’appareil.                                                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](getting-started.md)
</dt> </dl>

 

 






---
title: Réalisation de l’individualisation DRM
description: Réalisation de l’individualisation DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- SDK Windows Media format, API étendues du client DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Kit de développement logiciel (SDK) Windows Media format, gestion des droits numériques (DRM)
- Windows Media Format SDK, individualisation DRM
- Windows Media Format SDK, individualisation
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- gestion des droits numériques (DRM), individualisation
- DRM (gestion des droits numériques), individualisation
- gestion des droits numériques (DRM), individualisation DRM
- DRM (gestion des droits numériques), individualisation DRM
- API étendues du client DRM, individualisation
- API étendues clientes, individualisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310897"
---
# <a name="performing-drm-individualization"></a>Réalisation de l’individualisation DRM

L’individualisation est le processus qui consiste à mettre à jour le composant DRM sur l’ordinateur client, à le chiffrer et à le rendre unique. Lorsqu’un ordinateur est individualisé, le composant DRM est lié à l’ordinateur et ne peut pas décoder le contenu sur un autre ordinateur. Les API étendues du client Windows Media DRM prennent en charge l’individualisation du composant DRM sur les ordinateurs clients.

L’individualisation est effectuée en appelant la méthode [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) . Vous pouvez appeler **PerformSecurityUpdate** pour qu’il soit personnalisable uniquement si la version sur le serveur est plus récente que celle installée sur l’ordinateur client, ou vous pouvez forcer l’individualisation sans tenir compte des versions de sécurité relatives. L’indicateur de l’individualisation en tant que nécessaire est la \_ sécurité WMDRM \_ perform \_ indiv. L’indicateur de l’individualisation forcée est la \_ sécurité WMDRM \_ perform \_ force \_ indiv.

**PerformSecurityUpdate** est un appel asynchrone. Elle retournera rapidement, puis générera des événements pour fournir des informations d’État sur le processus d’individualisation. La majorité des événements générés sont les événements **MEWMDRMIndividualizationProgress** et chacun d’eux est associé à une interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) . Pour obtenir l’interface d’État, vous devez appeler **IMFMediaEvent :: GetValue** pour récupérer un pointeur **IUnknown** qui se trouve sur le même objet, puis l’interroger pour **IWMDRMIndividualizationStatus**.

Vous pouvez obtenir des données pour une structure d’état de l' [**\_ \_ individualisation WM**](drmwm-individualize-status.md) en appelant [**IWMDRMIndividualizeStatus :: GetStatus**](iwmdrmindividualizationstatus-getstatus.md). Chaque événement généré a son propre objet avec l’État. vous devez donc suivre le processus d’obtention de la valeur de l’événement et de l’interrogation de l’interface d’État à chaque fois.

Selon la taille du téléchargement, il peut y avoir des dizaines ou des centaines d’événements **MEWMDRMIndividualizationProgress** . Lorsque le processus d’individualisation est terminé, un événement **MEWMDRMIndividualizationCompleted** est généré.

Lorsque l’individualisation est terminée, les seuls objets existants qui reflètent le nouvel État individualisé sont ceux qui héritent de [**IWMDRMSecurity**](iwmdrmsecurity.md). Tous les autres objets existants ne seront pas mis à jour. Vous devez libérer et recréer tous les autres objets pour qu’ils reflètent le nouvel État individualisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple d’individualisation DRM**](drm-individualization-example.md)
</dt> <dt>

[**Guide de programmation**](drm-programming-guide.md)
</dt> <dt>

[**Utilisation du modèle d’événement Media Foundation**](using-the-media-foundation-model.md)
</dt> <dt>

[Meilleures pratiques pour l’individualisation DRM Windows Media](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 





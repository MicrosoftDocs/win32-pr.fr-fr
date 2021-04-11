---
title: Flux Web
description: Flux Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media Format SDK, flux Web
- ASF (Advanced Systems Format), flux Web
- ASF (format de systèmes avancés), flux Web
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- Flux Web, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029139"
---
# <a name="web-streams"></a>Flux Web

Un flux Web est semblable à un flux de fichier, car il contient des fichiers de données. Dans un flux Web, ces fichiers sont généralement des pages HTML et des graphiques associés au format GIF ou JPEG.

Les flux Web peuvent être particulièrement utiles pour les fichiers ASF utilisés comme présentations. Avant la prise en charge des flux Web, les présentations auraient des URL dans les flux de script dans un fichier afin qu’une page Web se chargeait à une heure prédéterminée. La difficulté était que la congestion du réseau pouvait entraîner des retards et créer une expérience d’affichage médiocre.

Avec les flux Web, les parties constitutives des pages Web peuvent être incluses dans le fichier ASF sous forme de flux. À mesure que les fichiers sont reçus, ils peuvent être mis en cache afin que, quand la commande pour afficher (ou rendre) une URL soit remise, elle peut être accessible instantanément par un navigateur. Cela permet une lecture fluide et homogène. La commande Render est fournie dans le flux Web lui-même, et non pas comme une commande de script dans un flux distinct.

Il est recommandé que les flux Web créés à l’aide du kit de développement logiciel (SDK) Windows Media Format 9 Series ou version ultérieure reçoivent le numéro de version 1. Cette valeur est spécifiée dans la structure de [**\_ \_ format webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) dans le membre **wVersion** . Le kit de développement logiciel (SDK) lui-même ne fait rien pour appliquer cette version.

> [!Note]  
> Lors de la connexion à des flux de diffusion en direct qui ont des flux Web, il est possible que l’utilisateur puisse recevoir une commande de rendu avant que le fichier spécifié soit réellement dans le cache local. À moins que votre application ne gère cette condition, le navigateur affichera une erreur « page introuvable ».

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Flux arbitraires**](arbitrary-streams.md)
</dt> <dt>

[**Configuration de flux Web**](configuring-web-streams.md)
</dt> </dl>

 

 





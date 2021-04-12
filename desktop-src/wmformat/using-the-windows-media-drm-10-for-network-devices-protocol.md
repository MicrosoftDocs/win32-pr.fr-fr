---
title: Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau
description: Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK, Windows Media DRM 10 pour les périphériques réseau
- Windows Media Format SDK, DRM 10 pour les périphériques réseau
- ASF (Advanced Systems Format), Windows Media DRM 10 pour les périphériques réseau
- ASF (format avancé des systèmes), Windows Media DRM 10 pour les périphériques réseau
- ASF (Advanced Systems Format), DRM 10 pour les périphériques réseau
- ASF (format de systèmes avancés), DRM 10 pour les périphériques réseau
- gestion des droits numériques (DRM), Windows Media DRM 10 pour les périphériques réseau
- DRM (gestion des droits numériques), Windows Media DRM 10 pour les périphériques réseau
- gestion des droits numériques (DRM), DRM 10 pour les périphériques réseau
- DRM (gestion des droits numériques), DRM 10 pour les périphériques réseau
- Windows Media DRM 10 pour les périphériques réseau, protocoles
- DRM 10 pour les périphériques réseau, protocoles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309886"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a>Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau

Le kit de développement logiciel (SDK) du format Windows Media fournit certaines fonctionnalités pour prendre en charge le protocole de périphérique réseau sécurisé, Windows Media DRM 10 pour les périphériques réseau. Ce protocole définit les messages envoyés entre un périphérique de lecture multimédia numérique, tel qu’un lecteur vidéo en haut de la série, et l’ordinateur qui sert les données à l’appareil. Les données multimédia envoyées entre le serveur et l’appareil sont chiffrées pour empêcher l’interception.

La communication entre votre application et les appareils qui prennent en charge Windows Media DRM 10 pour les périphériques réseau peut utiliser les protocoles de mise en réseau que vous préférez. Le kit de développement logiciel (SDK) Windows Media format ne fournit pas d’objets qui effectuent les communications réseau pour vous. Au lieu de cela, les objets de ce SDK traitent les messages de Windows Media DRM 10 pour les périphériques réseau une fois que votre application les a reçus.

Les fonctionnalités qui prennent en charge Windows Media DRM 10 pour les périphériques réseau sont l’inscription des appareils, la détection de proximité et la conversion des fichiers protégés par DRM. Ces fonctionnalités sont décrites dans les sections suivantes.



| Section                                                                                                                                                                          | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Inscription de l’appareil](device-registration.md)                                                                                                                                   | Décrit comment traiter les messages de demande d’inscription à partir d’appareils.                                                                       |
| [Détection de proximité en cours](performing-proximity-detection.md)                                                                                                             | Décrit le processus de détection de proximité.                                                                                                 |
| [Conversion d’un fichier de DRM-Protected en un flux Windows Media DRM 10 pour les périphériques réseau](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | Décrit comment convertir un fichier protégé par DRM en un flux qui peut être envoyé à un appareil qui utilise Windows Media DRM 10 pour les périphériques réseau. |



 

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 





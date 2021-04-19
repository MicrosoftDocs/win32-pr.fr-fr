---
description: Interface de programmation d’applications WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interface de programmation d’applications WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530172"
---
# <a name="wpd-application-programming-interface"></a>Interface de programmation d’applications WPD

Les applications basées sur des appareils mobiles Windows peuvent explorer un appareil, envoyer et recevoir du contenu et même contrôler l’appareil, par exemple, prendre une photo ou envoyer un SMS. Le système est conçu pour être flexible afin que de nombreux types d’appareils puissent être explorés et extensibles afin que les développeurs de pilotes puissent définir des propriétés personnalisées et des commandes pour les appareils personnalisés.

Le tableau suivant décrit les rubriques principales de cette documentation.



| Rubrique                                                                                                                  | Description                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Exigences générales pour le développement d’applications](general-requirements-for-application-development.md)               | Configurations matérielle et logicielle requises pour développer des pilotes et des applications à l’aide d’appareils mobiles Windows.     |
| [Configuration requise pour les applications Windows Media DRM-Enabled](requirements-for-windows-media-drm-enabled-applications.md) | Propriétés requises pour activer les transferts de contenu protégés par DRM Windows Media.                      |
| [Exemples](sample.md)                                                                                                  | Description de deux applications de bureau en ligne de commande fournies avec ce kit de développement logiciel (SDK). |
| [Vue d’ensemble de l’application](application-overview.md)                                                                       | Concepts clés utilisés dans les appareils mobiles Windows.                                                             |
| [Guide de programmation](programming-guide.md)                                                                             | Tâches clés qu’une application exécutera, avec des instructions pas à pas et des extraits de code.              |
| [Guide de référence de programmation](programming-reference.md)                                                                     | Guide de référence des interfaces et des types de données définis par les appareils mobiles Windows.                      |



 

Les applications basées sur Windows Media Gestionnaire de périphériques ou l’acquisition d’images Windows peuvent accéder aux appareils mobiles Windows par le biais d’une couche de compatibilité.

Microsoft fournit plusieurs pilotes pour les protocoles et les périphériques standard, y compris les périphériques MTP (Media Transport Protocol) et les périphériques de classe de stockage de masse (MSC). Si vous êtes familiarisé avec l’infrastructure de pilote User-Mode, vous pouvez développer vos propres pilotes pour des appareils personnalisés.

 

 




---
title: Utilisation d’IMAPi
description: Les rubriques suivantes illustrent l’utilisation de l’API de mastérisation d’image.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf19d619f6ed5ab9a2d6b0deb1ca6a42b71a0b0941a96f54cccfa87c14b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092429"
---
# <a name="using-imapi"></a>Utilisation d’IMAPi

Les rubriques suivantes illustrent l’utilisation de l’API de mastérisation d’image.

## <a name="usage-scenarios"></a>Scénarios d’utilisation

La documentation suivante fournit des conseils détaillés pour les scénarios IMAPi courants.



| Scénario                                                                                                         | Description                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vérification de la prise en charge du lecteur](checking-drive-support.md)                                                             | Illustre la détection de la prise en charge d’un lecteur multimédia.<br/>                                                                                                   |
| [Vérification de la prise en charge des supports](checking-media-support.md)                                                             | Illustre la détection de la prise en charge des médias.<br/>                                                                                                           |
| [Gravure d’une image de disque](burning-a-disc.md)                                                                       | Illustre la maîtrise (gravure d’un disque) à l’aide d’IMAPi.<br/>                                                                                                       |
| [Ajout d’une image de démarrage](adding-a-boot-image.md)                                                                   | S’appuie sur l’exemple [gravure d’une image de disque](burning-a-disc.md) en ajoutant du code pour inclure une image de démarrage dans la section de démarrage du disque.<br/>               |
| [Création d’un disque multisession](creating-a-multisession-disc.md)                                                 | Illustre la création d’un disque multisession à l’aide d’IMAPi.<br/>                                                                                              |
| [Surveillance de la progression avec des événements](monitoring-progress-with-events.md)                                           | Illustre l’utilisation d’interfaces spécifiques pour permettre l’implémentation d’un gestionnaire d’événements afin que les informations de progression puissent être reçues. <br/>        |
| [Empêcher la déconnexion ou la suspension pendant une gravure](preventing-logoff-or-suspend-during-a-burn.md)                     | Contient des informations détaillant les considérations relatives au développement d’applications en ce qui concerne les scénarios impliquant l’utilisateur « Logoff » et « suspend » dans Windows.<br/> |
| [Fournir des autorisations utilisateur pour les appareils de gravure de médias](providing-user-permissions-for-media-burning-devices.md) | détaille le processus nécessaire pour s’assurer qu’un utilisateur dispose des autorisations adéquates pour utiliser les appareils de gravure de contenu multimédia sur Windows XP et Windows Server 2003.<br/>             |



 

## <a name="application-compatibility"></a>Compatibilité des applications

La documentation suivante contient des informations importantes à prendre en compte lors du développement d’une application qui utilise IMAPi.



| Instructions                                                   | Description                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Présentation de la multisession IMAPi](imapi-multisession-layout.md) | Détaille la disposition du disque que IMAPi utilise pour implémenter la multisession. Ces informations sont utilisées pour garantir l’interopérabilité entre IMAPi et d’autres logiciels de gravure, ainsi que pour autoriser la création d’images de disque multisession compatibles IMAPi.<br/> |



 

 

 






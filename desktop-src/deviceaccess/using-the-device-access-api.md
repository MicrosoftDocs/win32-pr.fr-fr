---
title: Comment utiliser l’API d’accès à l’appareil
description: Cette rubrique contient des tâches et des considérations relatives à la conception pour l’utilisation de l’API d’accès aux appareils.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 29c4812c559b691a896fb5bb9da39064bf3c8614
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383195"
---
# <a name="how-to-use-the-device-access-api"></a>Comment utiliser l’API d’accès à l’appareil

Cette rubrique contient des tâches et des considérations relatives à la conception pour l’utilisation de l’API d’accès aux appareils.

## <a name="steps"></a>Étapes

| Rubrique | Description |
|---|---|
| [Considérations relatives à la conception des appareils personnalisés](design.md)<br/> | Cette rubrique décrit les considérations de conception qui peuvent vous aider à déterminer si votre appareil a besoin d’un pilote personnalisé.<br/> |
| [Implémenter l’objet d’accès de l’appareil](create-the-device-access-object.md)<br/> | Cette rubrique explique comment instancier l’objet d’accès de l’appareil et l’utiliser pour accéder à un appareil. <br/>  |
| [Déclaration de la fonctionnalité de l’appareil](declaring-the-device-capability.md)<br/> | Cette rubrique explique comment déclarer le GUID des fonctionnalités de l’appareil.<br/> |
| [Inscrire l’interface de l’appareil comme restreint aux applications privilégiées](register-the-device-interface-class-as-privileged.md)<br/> | Cette rubrique montre comment ajouter la propriété **Restricted** qui indique que seules les applications privilégiées peuvent accéder à une classe d’interface d’appareil.<br/> |
| [Créer une extension de Windows Runtime](create-a-windows-runtime-extension.md)<br/> | Vous pouvez créer un composant Windows Runtime pour inclure dans un wrapper le composant qui accède à votre pilote. Vous pouvez ensuite écrire une application d’appareil Windows Store pour votre appareil en C# ou JavaScript.<br/> |

## <a name="additional-resources"></a>Ressources supplémentaires

- L' [exemple d’accès au pilote personnalisé](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) montre comment utiliser les API d’accès de l’appareil pour accéder à un pilote personnalisé à partir d’une application d’appareil du Windows Store.
- Les [applications d’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) fournissent des ressources pour en savoir plus sur la conception et le développement d’applications d’appareils Windows Store pour des appareils spécialisés.
- Le [Centre](/windows-hardware/drivers/) de développement matériel fournit des ressources générales pour les tâches de développement d’applications pour appareils Windows Store qui sont communes à tous les types d’appareils.

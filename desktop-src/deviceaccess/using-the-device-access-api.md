---
title: Comment utiliser l’API d’accès à l’appareil
description: Cette rubrique contient des tâches et des considérations relatives à la conception pour l’utilisation de l’API d’accès aux appareils.
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: bd1ddf9d2716cd01ab2db8acb08d2793a6831ffa6f20aa2c75378f72932d992b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635299"
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
| [créer une Extension de Windows Runtime](create-a-windows-runtime-extension.md)<br/> | vous pouvez créer un composant Windows Runtime pour inclure dans un wrapper le composant qui accède à votre pilote. vous pouvez ensuite écrire une application d’appareil Windows Store pour votre appareil en C# ou JavaScript.<br/> |

## <a name="additional-resources"></a>Ressources supplémentaires

- l' [exemple d’accès au pilote personnalisé](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) montre comment utiliser les api d’accès de l’appareil pour accéder à un pilote personnalisé à partir d’une application de l’appareil Windows Store.
- [applications pour appareils UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) fournit des ressources pour en savoir plus sur la conception et le développement d’applications d’appareil Windows Store pour des appareils spécialisés.
- le [Centre de développement matériel](/windows-hardware/drivers/) fournit des ressources générales pour les tâches de développement d’applications de l’appareil Windows Store qui sont communes à tous les types d’appareils.

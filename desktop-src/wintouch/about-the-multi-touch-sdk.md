---
title: À propos de Windows Touch
description: Cette rubrique fournit une brève présentation de Windows Touch.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch, kit de développement logiciel (SDK)
- Windows Touch, SDK
- Windows Touch, à propos de
- Windows Touch, nouvelles fonctionnalités
- Windows Touch, nouveautés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e9a3ebab9a5c85127a1548c07c2ea0fa2cae54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939684"
---
# <a name="about-windows-touch"></a>À propos de Windows Touch

Cette rubrique fournit une brève présentation de Windows Touch.

Les nouveaux éléments de matériel et d’API du système d’exploitation Windows 7 offrent aux applications la possibilité de recevoir des entrées de plusieurs contacts. Cela donne à ces applications la possibilité de détecter et de répondre à plusieurs points tactiles simultanés sur la surface visible de l’application. Les fonctionnalités de cette fonctionnalité dans Windows 7 sont fournies par un nouveau message qui signale et effectue le suivi des touches. Le nouveau message, [**WM \_ Touch**](wm-touchdown.md), signale l’action (haut, descendre, déplacer), la position et un identificateur pour les points tactiles. Les messages tactiles Windows sont générés par Windows et sont remis à Windows qui s’inscrivent à l’entrée tactile Windows.

En plus du nouveau message de saisie tactile, des messages de mouvement ont été ajoutés à la liste existante de messages de fenêtre. La prise en charge de la messagerie pour les gestes est activée par un nouveau message de fenêtre ([**\_ mouvement WM**](wm-gesture.md)) qui est envoyé ou publié dans les fenêtres d’application appropriées lorsque l’entrée utilisateur est reconnue comme un geste. Les fonctions d’API dédiées encapsulent les détails de la création et de la consommation de ce message. Cela est dû au fait que les informations associées au message peuvent changer à l’avenir sans interrompre les applications qui consomment déjà ce message.

En plus des messages de mouvement, des interfaces spécialisées ont été ajoutées au SDK Windows. Ces interfaces activent la prise en charge avancée de l’entrée tactile pour permettre aux développeurs d’applications de créer facilement des interfaces utilisateur naturelles. L’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interprète les messages [**WM \_ Touch**](wm-touchdown.md) pour déclencher des événements qui contiennent des informations de translation, de rotation et de mise à l’échelle sur une collection de points tactiles. L’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) peut être utilisée conjointement avec l’interface **IManipulationProcessor** pour activer l’animation et garantir que les objets restent sur l’écran de l’utilisateur lorsqu’ils sont déplacés.

Les éléments d’API pour Windows Touch ont des similitudes avec le kit de développement logiciel (SDK) Microsoft PixelSense (anciennement connu sous le nom de Microsoft surface SDK), mais les applications ciblant Microsoft PixelSense ne s’exécutent pas sur les ordinateurs tactiles Windows. En outre, les applications ciblant Windows Touch ne s’exécutent pas sur Microsoft PixelSense.

Certaines fonctionnalités de Windows Touch sont intégrées au cœur de Windows 7. Cette fonctionnalité est disponible pour les utilisateurs sans que les développeurs n’aient besoin d’activer explicitement la prise en charge. Toutefois, pour tirer pleinement parti de Windows Touch, les développeurs doivent utiliser l’API tactile Windows. Pour commencer à découvrir comment fonctionne Windows Touch, consultez le [Guide de programmation](programming-guide.md) ou commencez par [choisir la bonne approche pour Windows Touch](choosing-the-right-approach-to-windows-touch.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de l’architecture](architectural-overview.md)
</dt> <dt>

[Choix de la bonne approche pour Windows Touch](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Tactile Windows](windows-touch-portal.md)
</dt> </dl>

 

 





---
title: Conception d’animation
description: Conception d’animation
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939845"
---
# <a name="animation-design"></a>Conception d’animation

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

### <a name="image-design"></a>Conception d’image

Utilisez la palette de Microsoft Office lors de la conception de vos caractères pour réduire les problèmes potentiels de réalisation de la palette. Évitez de sélectionner une couleur de transparence similaire aux couleurs que vous utilisez dans votre document.

### <a name="sounds"></a>Sons

Microsoft agent vous permet de lire des sons dans vos animations. Nous vous recommandons de ne pas inclure de sons pour vos animations **inactives** . Ainsi, il n’y aura pas de délai au milieu de l’animation, si l’agent doit charger la DLL multimédia système.

### <a name="frame-size"></a>Taille de trame

Les compagnons Office standard sont 123 x 93 pixels. Bien que vous puissiez créer des caractères d’autres tailles, ceux-ci seront mis à l’échelle à 123 x 93 dans la Galerie de l’Assistant.

### <a name="frame-transition"></a>Transition de frame

Toutes les animations, à l’exception de **adieu**, **Greetings**, **Show** et **Hide** , doivent commencer et se terminer par l’animation RestPose. Microsoft Office ne lise pas les animations de **retour** explicites, vous ne devez pas les définir. Toutes les animations doivent également avoir une branche de sortie. La création de branche de sortie nous permet de mettre en place et de terminer l’animation en cours avant d’appeler l’animation suivante. Si vous ne fournissez pas de branchement de sortie, la transition entre les animations peut être saccadée.

### <a name="character-properties"></a>Propriétés des caractères

Microsoft agent vous permet de définir les propriétés [**Name**](name-property.md), [**Description**](description-property.md) et [**ExtraData**](extradata-property.md) du caractère. Microsoft Office utilise le champ **ExtraData** pour contenir une ou plusieurs expressions d’introduction et expressions de rappel. Microsoft Office choisit les autres expressions de présentation à placer dans la bulle de reconnaissance vocale dans la Galerie de l’Assistant. Nous utilisons les phrases de rappel lorsque vous recevez un rappel d’Outlook.

Le champ [**ExtraData**](extradata-property.md) est mis en forme comme suit :

IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

Les expressions Intro sont séparées par une paire de caractères tildes (~), suivis de phrases de rappel. Ces expressions de rappel sont également séparées par une paire de caractères tilde. Les deux ensembles d’expressions sont séparés par deux caractères de signe insertion (^^). Il n’existe pas de limite au nombre de chaque type d’expression, sauf qu’il doit y en avoir au moins un.

 

 





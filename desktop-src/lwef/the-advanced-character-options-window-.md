---
title: Fenêtre Options des caractères avancés (fenêtre commandes vocales)
description: En savoir plus sur la fenêtre Options de caractères avancés, qui fournit des options permettant aux utilisateurs d’ajuster leur interaction avec tous les caractères.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404356"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Fenêtre Options des caractères avancés (fenêtre commandes vocales)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La fenêtre Options de caractères avancés fournit des options permettant aux utilisateurs d’ajuster leur interaction avec tous les caractères. Par exemple, les utilisateurs peuvent désactiver l’entrée vocale ou modifier les paramètres d’entrée. Les utilisateurs peuvent également modifier les paramètres de sortie du mot-bulle. Ces paramètres remplacent tous les jeux par une application cliente ou définis dans le cadre de la définition des caractères. Votre application ne peut pas modifier ou désactiver ces options, car elles s’appliquent aux préférences de l’utilisateur général pour le fonctionnement de tous les caractères. Toutefois, le serveur notifie votre application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) lorsque l’utilisateur modifie et applique une option. Vous pouvez également afficher ou fermer la fenêtre à l’aide de la propriété [**visible**](visible-property.md) de la fenêtre et accéder à son emplacement par le biais de ses propriétés [**Top**](top-property.md) et [**Left**](left-property.md) .

Outre la prise en charge de l’animation d’un caractère, Microsoft agent prend en charge la sortie audio pour le caractère. Cela comprend la sortie orale et les effets sonores. Pour une sortie orale, le serveur consigne automatiquement les images de la bouche définies du caractère dans la sortie. Vous pouvez choisir la synthèse TTS (conversion de texte par synthèse vocale), l’audio enregistré ou uniquement la sortie de texte de la bulle.

 

 





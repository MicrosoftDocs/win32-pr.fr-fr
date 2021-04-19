---
description: Description des techniques sous-standard pour l’exposition de contrôles personnalisés.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Techniques substandardistes pour l’exposition de contrôles personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541898"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Techniques substandardistes pour l’exposition de contrôles personnalisés

Si une application ne prend pas en charge Microsoft Active Accessibility, elle peut ne pas être entièrement accessible. Les techniques suivantes rendent les contrôles partiellement compatibles :

-   Retourne une chaîne descriptive lorsque le contrôle est interrogé à l’aide du \_ message WM GETTEXT. Par exemple, vous pouvez autoriser un équivalent personnalisé d’un contrôle bouton intitulé « imprimer » pour retourner la chaîne « bouton imprimer ». Cela identifie le type de contrôle et l’étiquette. La même chaîne est appropriée pour un bouton avec une étiquette autre que du texte, tel qu’un graphique d’imprimante. De même, autoriser un contrôle personnalisé qui se comporte comme une case à cocher pour retourner la chaîne de légende « impression activée, activée ».
-   Prenez en charge le \_ message WM GETDLGCODE, en identifiant l’entrée au clavier prise en charge. Par exemple, autorisez un équivalent personnalisé d’un contrôle d’édition à gérer WM \_ GETDLGCODE en retournant DLGC \_ HASSETSEL s’il gère les messages pour définir la sélection, DLGC \_ WANTARROWS s’il utilise des touches de direction et DLGC \_ WANTCHARS pour indiquer qu’il utilise l’entrée de caractères.
    > [!Note]  
    > Seuls les contrôles qui ont leurs propres handles de fenêtre peuvent répondre aux \_ messages WM GETTEXT et WM \_ GETDLGCODE.

     

Pour éviter les problèmes de compatibilité avec les aides à l’accessibilité, vous devez suivre Active Accessibility instructions avec soin lors de la conception de contrôles personnalisés. Pour plus d’informations sur la façon d’éviter des problèmes de compatibilité avec les aides à l’accessibilité, consultez la section [accessibilité](../accessibility/accessibility.md) .

 

 

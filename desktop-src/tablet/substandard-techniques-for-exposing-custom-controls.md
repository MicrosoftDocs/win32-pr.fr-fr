---
description: Description des techniques sous-standard pour l’exposition de contrôles personnalisés.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Techniques substandardistes pour l’exposition de contrôles personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121856bf5303b011b785a26bc47013e0df93463d7f278d6e4586991a47d8e020
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934309"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Techniques substandardistes pour l’exposition de contrôles personnalisés

Si une application ne prend pas en charge Microsoft Active Accessibility, elle peut ne pas être entièrement accessible. Les techniques suivantes rendent les contrôles partiellement compatibles :

-   Retourne une chaîne descriptive lorsque le contrôle est interrogé à l’aide du \_ message WM GETTEXT. Par exemple, vous pouvez autoriser un équivalent personnalisé d’un contrôle bouton intitulé « imprimer » pour retourner la chaîne « bouton imprimer ». Cela identifie le type de contrôle et l’étiquette. La même chaîne est appropriée pour un bouton avec une étiquette autre que du texte, tel qu’un graphique d’imprimante. De même, autoriser un contrôle personnalisé qui se comporte comme une case à cocher pour retourner la chaîne de légende « impression activée, activée ».
-   Prenez en charge le \_ message WM GETDLGCODE, en identifiant l’entrée au clavier prise en charge. Par exemple, autorisez un équivalent personnalisé d’un contrôle d’édition à gérer WM \_ GETDLGCODE en retournant DLGC \_ HASSETSEL s’il gère les messages pour définir la sélection, DLGC \_ WANTARROWS s’il utilise des touches de direction et DLGC \_ WANTCHARS pour indiquer qu’il utilise l’entrée de caractères.
    > [!Note]  
    > Seuls les contrôles qui ont leurs propres handles de fenêtre peuvent répondre aux \_ messages WM GETTEXT et WM \_ GETDLGCODE.

     

Pour éviter les problèmes de compatibilité avec les aides à l’accessibilité, vous devez suivre Active Accessibility instructions avec soin lors de la conception de contrôles personnalisés. Pour plus d’informations sur la façon d’éviter des problèmes de compatibilité avec les aides à l’accessibilité, consultez la section [accessibilité](../accessibility/accessibility.md) .

 

 

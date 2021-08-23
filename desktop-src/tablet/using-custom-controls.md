---
description: Description de l’utilisation des contrôles client pour le Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Utilisation de contrôles personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70699a141f0319f917953e25363db0e0cd38eb21ecc06345c581b55526ad6bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551879"
---
# <a name="using-custom-controls"></a>Utilisation de contrôles personnalisés

Vous pouvez personnaliser les contrôles standard en utilisant le dessin owner-drawn pour modifier l’apparence du contrôle et l’établissement d’une superclasse ou d’une sous-classe pour modifier le comportement du contrôle. Dans chaque cas, le code système sous-jacent pour le type de contrôle standard gère les fonctions de contrôle de base. La plupart de ces contrôles peuvent être accessibles si vous les utilisez correctement.

Un contrôle owner-drawn basé sur un contrôle standard apparaît comme le contrôle standard pour les aides à l’accessibilité et prend en charge Microsoft Active Accessibility ; Toutefois, il a une apparence personnalisée. Certaines applications utilisent des contrôles personnalisés pour modifier l’apparence d’un contrôle, mais les contrôles owner-drawn sont une solution plus accessible. Pour plus d’informations sur la façon de définir des menus owner-drawn et d’exposer des contrôles owner-drawn, consultez [accessibilité](../accessibility/accessibility.md).

L’établissement d’une superclasse ou d’une sous-classe est une technique permettant de personnaliser le comportement des contrôles existants. Selon le nouveau comportement du contrôle, il peut être nécessaire de compléter les informations d’accessibilité qu’il expose. Par exemple, une application peut utiliser un contrôle owner-drawn pour afficher un X dans une case à cocher sélectionnée au lieu d’une coche, ou pour étiqueter un bouton de commande avec une image au lieu d’un mot.

Quand vous utilisez des contrôles owner-drawn qui sont soit une superclasse, soit une sous-classe :

-   Fournissez des étiquettes pour tous les contrôles, même lorsque les étiquettes ne sont pas visibles à l’écran. Si vous personnalisez un contrôle afin que la légende standard ne soit pas visible (par exemple, un bouton avec un visage graphique) et que vous laissez la légende sous la forme d’une chaîne vide, l’aide à l’accessibilité n’est pas en mesure d’obtenir la légende et de l’utiliser pour identifier le contrôle.
-   Assurez-vous que [**WM \_ GETTEXT**](../winmsg/wm-gettext.md) est pris en charge.
-   Assurez-vous que tous les messages spécifiques à la classe sont pris en charge. Il est particulièrement important de prendre en charge les messages d’extraction de texte tels que [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) et [**lb \_ GETTEXT**](../controls/lb-gettext.md). Définissez les bits de style appropriés, tels que **CBS \_ HASSTRINGS** et **lbs \_ HASSTRINGS**, pour indiquer que le contrôle prend en charge ces messages.

 

 

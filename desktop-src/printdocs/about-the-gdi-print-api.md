---
description: L’une des fonctionnalités principales des fonctions de l’API d’impression GDI est la prise en charge de l’indépendance des appareils.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: À propos de l’API d’impression GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3aa7ea0ecfdd96237fb330868ddf2d9619aa24ee0d2f27a940c789a581a6c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951009"
---
# <a name="about-the-gdi-print-api"></a>À propos de l’API d’impression GDI

L’une des fonctionnalités principales des fonctions de l’API d’impression GDI est la prise en charge de l’indépendance des appareils. Au lieu d’émettre des commandes spécifiques à l’appareil pour dessiner la sortie sur une imprimante ou un traceur particulier, une application appelle des fonctions de haut niveau à partir de l’interface GDI (Graphics Device Interface). Par exemple, pour imprimer une image bitmap, une application peut appeler la fonction [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) , en fournissant les coordonnées de la bitmap, ainsi que les handles qui identifient les contextes de périphérique (DC) source et de destination. L’appel à **BitBlt** est ensuite converti en commandes d’appareils brutes par un pilote d’imprimante. Un pilote de périphérique est une bibliothèque de liens dynamiques (DLL) qui prend en charge l’interface de pilote de périphérique (DDI). Un pilote de périphérique génère des commandes d’appareil brutes lors du traitement des appels aux fonctions DDI effectuées par le moteur graphique. Les commandes sont traitées par l’imprimante lorsqu’elle imprime l’image. La syntaxe, le nombre et le type de ces commandes varient d’un appareil à l’appareil.

Cette vue d’ensemble fournit des informations sur les rubriques suivantes.

<dl>

[Interface d’impression par défaut](default-printing-interface.md)  
[Contextes de périphérique d’impression](printer-output.md)  
[Échappements de l’imprimante](printer-escapes.md)  
[Affichage et sortie WYSIWYG](wysiwyg-display-and-output.md)  
[DEVMODE par utilisateur](per-user-devmode.md)  
</dl>

 

 

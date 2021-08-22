---
description: L’indépendance des appareils est l’une des principales fonctionnalités de Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: À propos des contextes de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9439e3091b3138917e24ab4a49ff89c21a1e1b53480d4a138bd2bbad3288fcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105874"
---
# <a name="about-device-contexts"></a>À propos des contextes de périphérique

L’indépendance des appareils est l’une des principales fonctionnalités de Microsoft Windows. Les applications peuvent dessiner et imprimer la sortie sur divers appareils. Les logiciels qui prennent en charge cette indépendance des appareils sont contenus dans deux bibliothèques de liens dynamiques. Le premier, Gdi.dll, est appelé GDI (Graphics Device Interface); le deuxième est appelé pilote de périphérique. Le nom du second dépend de l’appareil sur lequel l’application dessine la sortie. Par exemple, si l’application dessine la sortie dans la zone cliente de sa fenêtre sur un affichage VGA, cette bibliothèque est Vga.dll ; Si l’application imprime la sortie sur une imprimante Epson FX-80, cette bibliothèque est Epson9.dll.

Une application doit indiquer à GDI de charger un pilote de périphérique particulier et, une fois le pilote chargé, de préparer l’appareil pour les opérations de dessin (par exemple, sélectionner une couleur et une largeur de ligne, un modèle de pinceau et une couleur, une police de caractères, une zone de découpage, etc.). Ces tâches sont accomplies en créant et en conservant un contexte de périphérique (DC). Un contrôleur de schéma est une structure qui définit un ensemble d’objets graphiques et leurs attributs associés, ainsi que les modes graphiques qui affectent la sortie. Les objets graphiques incluent un stylet pour dessiner des lignes, un pinceau pour la peinture et le remplissage, une image bitmap pour la copie ou le défilement des parties de l’écran, une palette pour définir l’ensemble des couleurs disponibles, une région pour le découpage et d’autres opérations, ainsi qu’un chemin d’accès pour les opérations de peinture et de dessin. Contrairement à la plupart des structures, une application n’a jamais un accès direct au contrôleur de service. au lieu de cela, il opère indirectement sur la structure en appelant diverses fonctions.

Cette vue d’ensemble fournit des informations sur les rubriques suivantes :

-   [Objets graphiques](graphic-objects.md)
-   [Modes graphiques](graphic-modes.md)
-   [Types de contexte de périphérique](device-context-types.md)
-   [Opérations de contexte de périphérique](device-context-operations.md)
-   [fonctions de contexte de périphérique compatibles ICM](icm-enabled-device-context-functions.md)

Un concept important est la disposition d’un DC ou d’une fenêtre, qui décrit l’ordre dans lequel les objets GDI et le texte sont révélés (de gauche à droite ou de droite à gauche). Pour plus d’informations, consultez « disposition des fenêtres et mise en miroir » dans [**fonctionnalités des fenêtres**](../winmsg/window-features.md) et fonctions [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) et [**setLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) .

 

 

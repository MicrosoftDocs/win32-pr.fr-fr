---
description: Une application peut utiliser le découpage et les tracés pour créer des effets graphiques spéciaux. L’illustration suivante montre une chaîne de texte dessinée avec une grande police Arial.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Tracés de clip et effets graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528390"
---
# <a name="clip-paths-and-graphic-effects"></a>Tracés de clip et effets graphiques

Une application peut utiliser le découpage et les tracés pour créer des effets graphiques spéciaux. L’illustration suivante montre une chaîne de texte dessinée avec une grande police Arial.

![Illustration montrant du texte noir sur un arrière-plan blanc](images/cspth-02.png)

L’illustration suivante montre le résultat obtenu en sélectionnant le texte comme tracé de clip et en dessinant des lignes radiales pour un cercle dont le Centre se trouve au-dessus et à gauche de la chaîne.

![Illustration montrant le même texte, mais remplie de lignes au lieu de noir Uni](images/cspth-03.png)

> [!Note]  
> Avant que GDI (Graphics Device Interface) ajoute un texte créé avec une police bitmap à un tracé, il convertit la police en police vectorielle ou vectorielle.

 

Une application crée un tracé de clip en générant un crochet de chemin d’accès, puis en appelant la fonction [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) . Une fois qu’un tracé de clip est sélectionné dans un DC, la sortie s’affiche uniquement dans les bordures du tracé.

Outre la création d’effets graphiques spéciaux, les tracés de clip sont également utiles dans les applications qui enregistrent des images en tant que sous-fichiers améliorés. En utilisant un tracé de clip, une application peut garantir l’indépendance des appareils, car les unités utilisées pour spécifier un chemin d’accès sont des unités logiques.

 

 




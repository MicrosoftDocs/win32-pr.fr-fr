---
description: Un métafichier amélioré est un tableau d’enregistrements.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Enregistrements de métafichiers améliorés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414332"
---
# <a name="enhanced-metafile-records"></a>Enregistrements de métafichiers améliorés

Un métafichier amélioré est un tableau d’enregistrements. Un enregistrement de métafichier est une structure [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) de longueur variable. Au début de chaque enregistrement de métafichier amélioré se trouve une structure [**le**](/windows/win32/api/wingdi/ns-wingdi-emr) , qui contient deux membres. Le premier membre, iType, identifie le type d’enregistrement qui est, la fonction GDI dont les paramètres sont contenus dans l’enregistrement. Étant donné que les structures sont de longueur variable, l’autre membre, nSize, contient la taille de l’enregistrement. Immédiatement après le membre nSize, les paramètres restants, le cas échéant, de la fonction GDI. Le reste de la structure contient des données supplémentaires qui dépendent du type d’enregistrement.

Le premier enregistrement dans un métafichier amélioré est toujours la structure [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , qui est l’en-tête de métafichier amélioré. L’en-tête spécifie les informations suivantes :

-   Taille du métafichier, en octets
-   Dimensions du cadre d’image, en unités de périphérique
-   Dimensions du cadre d’image, en unités de 01 à millimètres
-   Nombre d’enregistrements dans le métafichier
-   Décalage d’une description de texte facultative
-   Taille de la palette facultative
-   Résolution de l’appareil d’origine, en pixels
-   Résolution de l’appareil d’origine, en millimètres

Une description de texte facultative peut suivre l’enregistrement d’en-tête. La description textuelle décrit l’image et le nom de l’auteur. La palette facultative spécifie les couleurs utilisées pour créer le métafichier amélioré. Les enregistrements restants identifient les fonctions GDI utilisées pour créer l’image. La sortie hexadécimale suivante correspond à un enregistrement généré pour un appel à la fonction [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .


```C++
00000011 0000000C 00000004 
```



La valeur 0x00000011 spécifie le type d’enregistrement (correspond à la \_ constante le SETMAPMODE définie dans le fichier WinGDI. h). La valeur 0x0000000C spécifie la longueur de l’enregistrement, en octets. La valeur 0x00000004 identifie le mode de mappage (correspond à la \_ constante mm LOENGLISH définie dans la fonction [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).

Pour obtenir la liste des types d’enregistrements supplémentaires, consultez [structures de métafichier](metafile-structures.md).

 

 




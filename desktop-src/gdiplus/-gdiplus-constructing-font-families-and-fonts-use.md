---
description: Windows GDI+ regroupe des polices avec la même police, mais des styles différents dans des familles de polices.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Construction des familles de polices et des polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc405883eadd85b5b8018f75da270085197aed4792bf1c6848628cce02f457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015191"
---
# <a name="constructing-font-families-and-fonts"></a>Construction des familles de polices et des polices

Windows GDI+ regroupe des polices avec la même police, mais des styles différents dans des familles de polices. Par exemple, la famille de polices Arial contient les polices suivantes :

-   Arial normal
-   Arial gras
-   Arial italique
-   Arial gras italique

GDI+ utilise quatre styles pour former les familles : normal, gras, italique et gras italique. Les adjectifs tels que *Narrow* et *Rounded* ne sont pas considérés comme des styles ; ils font plutôt partie du nom de famille. Par exemple, Arial Narrow est une famille de polices dont les membres sont les membres suivants :

-   Arial étroit normal
-   Arial étroit gras
-   Arial étroit italique
-   Arial étroit gras italique

avant de pouvoir dessiner du texte avec GDI+, vous devez construire un objet [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) et un objet [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Les objets **FontFamily** spécifient le type de caractères (par exemple, Arial) et l’objet **font** spécifie la taille, le style et les unités.

L’exemple suivant construit une police Arial de style standard d’une taille de 16 pixels :


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



Dans le code précédent, le premier argument passé au constructeur [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) est l’adresse de l’objet [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Le deuxième argument spécifie la taille de la police mesurée en unités identifiées par le quatrième argument. Le troisième argument identifie le style.

[* * * * UnitPixel * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) * * est un membre de l’énumération d' **unité** , et [* * * * FontStyleRegular * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) est un membre de l’énumération **FontStyle** . Les deux énumérations sont déclarées dans Gdiplusenums. h.

 

 




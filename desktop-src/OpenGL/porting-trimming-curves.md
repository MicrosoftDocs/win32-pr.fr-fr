---
title: Portage des courbes de suppression
description: Les courbes de suppression OpenGL sont très similaires aux courbes de rognage de l’IRIS. Le tableau suivant répertorie les fonctions IRIS GL permettant de définir des courbes de rognage et leurs fonctions OpenGL équivalentes.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Portage de l’IRIS dans le grand livre, découpage des courbes
- Portage à partir de IRIS GL, courbes de rognage
- portage vers OpenGL à partir de IRIS GL, courbes de rognage
- Portage OpenGL à partir de IRIS GL, courbes de rognage
- courbes de rognage
- courbes
- Portage de l’IRIS dans le GL, courbes
- Portage à partir de IRIS GL, courbes
- portage vers OpenGL à partir de IRIS GL, courbes
- Portage OpenGL à partir de IRIS GL, courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311706"
---
# <a name="porting-trimming-curves"></a>Portage des courbes de suppression

Les courbes de suppression OpenGL sont très similaires aux courbes de rognage de l’IRIS. Le tableau suivant répertorie les fonctions IRIS GL permettant de définir des courbes de rognage et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL | Fonction OpenGL                        | Signification                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Commence la définition de la courbe de délimitation.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Définit une courbe linéaire par morceaux.    |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Spécifie les attributs de la courbe de rognage. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Termine la définition de la courbe de rognage.      |



 

??

 

 





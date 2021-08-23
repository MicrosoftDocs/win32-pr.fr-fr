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
ms.openlocfilehash: ad544431adaa7f0b049341ec7314e3e53ae60752d633a48c760ca09334f79d33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553859"
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

 

 





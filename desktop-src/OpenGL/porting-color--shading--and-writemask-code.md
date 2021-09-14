---
title: Portage de la couleur, de l’ombrage et du code Writemask
description: Portage de la couleur, de l’ombrage et du code Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Portage du GL IRIS, couleur
- Portage à partir de IRIS GL, couleur
- portage vers OpenGL à partir de IRIS GL, couleur
- Portage OpenGL à partir de IRIS GL, couleur
- Portage de l’IRIS dans le GL, ombrage
- Portage à partir de IRIS GL, ombrage
- portage vers OpenGL à partir de IRIS GL, ombrage
- Portage OpenGL à partir de IRIS GL, ombrage
- Portage du grand livre de l’IRIS, writemask
- Portage à partir de IRIS GL, writemask
- portage vers OpenGL à partir de IRIS GL, writemask
- Portage OpenGL à partir de IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119154"
---
# <a name="porting-color-shading-and-writemask-code"></a>Portage de la couleur, de l’ombrage et du code Writemask

Lorsque vous portez des couleurs, des ombrages et du code writemask à OpenGL, gardez les points suivants à l’esprit :

-   Bien que vous puissiez définir des index de carte de couleurs avec la fonction OpenGL [glIndex](glindex-functions.md) , OpenGL ne dispose pas d’une fonction pour le chargement d’index de carte de couleurs.
-   Les valeurs de couleur sont normalisées en fonction de leur type de données. (Pour plus d’informations sur les valeurs de couleur, consultez [glColor](glcolor-functions.md)).
-   Il n’existe aucun équivalent simple pour **cpack**.
-   Vous devrez peut-être traduire le code qui comprend les fonctions **c** ou **Color** en [**glClearColor**](glclearcolor.md) ou [**glClearIndex**](glclearindex.md) au lieu de **glColor** ou **glIndex**.
-   Le writemask RVBA s’applique à chaque composant, mais pas à chaque bit.
-   IRIS GL fournit des constantes de couleur définies : noir, bleu, rouge, vert, MAGENTA, CYAN, jaune et blanc. OpenGL ne fournit pas ces constantes.

Cette rubrique contient des informations sur les éléments suivants.

-   [Portage des appels de couleur](porting-color-calls.md)
-   [Portage de modèles d’ombrage](porting-shading-models.md)

 

 





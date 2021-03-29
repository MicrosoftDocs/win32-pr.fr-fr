---
description: Un objet GraphicsPath stocke une séquence de lignes et de courbes B&\# 233 ;.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Aplatissement des chemins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987939"
---
# <a name="flattening-paths"></a>Aplatissement des chemins

Un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) stocke une séquence de lignes et de splines de Bézier. Vous pouvez ajouter plusieurs types de courbes (ellipses, arcs, splines cardinales) à un tracé, mais chaque courbe est convertie en spline de Bézier avant d’être stockée dans le tracé. L’aplatissement d’un tracé consiste à convertir chaque spline de Bézier dans le tracé en une séquence de lignes droites.

Pour aplatir un chemin d’accès, appelez la méthode [**GraphicsPath :: Flatten**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) d’un objet [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . La méthode **GraphicsPath :: flattse** reçoit un argument flate qui spécifie la distance maximale entre le chemin aplati et le chemin d’accès d’origine. L’illustration suivante montre un tracé avant et après la mise à plat.

![Illustration montrant une séquence de splines Bézier connectées en bleu et les lignes correspondantes en rouge](images/aboutgdip02-art32a.png)

 

 




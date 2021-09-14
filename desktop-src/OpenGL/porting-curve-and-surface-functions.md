---
title: Portage des fonctions de courbe et de surface
description: Portage des fonctions de courbe et de surface
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Portage de l’IRIS dans le GL, courbes
- Portage à partir de IRIS GL, courbes
- portage vers OpenGL à partir de IRIS GL, courbes
- Portage OpenGL à partir de IRIS GL, courbes
- Portage de l’IRIS dans le GL, carreaux de surface
- Portage à partir de IRIS GL, carreaux de surface
- portage vers OpenGL à partir de IRIS GL, carreaux de surface
- Portage OpenGL à partir de IRIS GL, carreaux de surface
- courbes
- carreaux de surface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119149"
---
# <a name="porting-curve-and-surface-functions"></a>Portage des fonctions de courbe et de surface

OpenGL ne prend pas en charge les équivalents des fonctions IRIS GL pour les courbes et les carreaux de surface. Vous devez réécrire votre code s’il comprend l’un des appels suivants :

-   **defbasis**
-   **curvebasis**, **curveprecision**, **CRV**, **CrVn**, **RCRV**, **rcrvn** et **curveit**
-   **patchbasis**, **patchcurves**, **patchprecision**, **patch** et **rpatch**

Cette rubrique contient des informations sur les éléments suivants.

-   [Portage d’objets NURBS](porting-nurbs-objects.md)
-   [Portage de courbes NURBS](porting-nurbs-curves.md)
-   [Portage des courbes de suppression](porting-trimming-curves.md)
-   [Portage des surfaces NURBS](porting-nurbs-surfaces.md)

 

 





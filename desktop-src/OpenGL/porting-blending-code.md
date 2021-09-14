---
title: Portage du code de fusion
description: Dans IRIS GL, quand vous dessinez sur des mémoires tampons d’arrière-plan et d’arrière-plan, la fusion est effectuée en lisant l’une des mémoires tampons, en fusionnant avec cette couleur, puis en écrivant le résultat dans les deux mémoires tampons. Dans OpenGL, toutefois, chaque tampon est lu successivement, fusionné, puis écrit.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Portage de l’IRIS dans le GL, fusion
- Portage à partir de IRIS GL, fusion
- portage vers OpenGL à partir de IRIS GL, fusion
- Portage OpenGL depuis IRIS GL, fusion
- mélanger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416658"
---
# <a name="porting-blending-code"></a>Portage du code de fusion

Dans IRIS GL, quand vous dessinez sur des mémoires tampons d’arrière-plan et d’arrière-plan, la fusion est effectuée en lisant l’une des mémoires tampons, en fusionnant avec cette couleur, puis en écrivant le résultat dans les deux mémoires tampons. Dans OpenGL, toutefois, chaque tampon est lu successivement, fusionné, puis écrit.

Le tableau suivant répertorie les fonctions de fusion de l’IRIS dans le GL et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL  | Fonction OpenGL                            | Signification                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) ( \_ mélange GL) | Active la fusion.          |
| **blendfunction** | [**glBlendFunc**](glblendfunc.md)         | Spécifie une fonction de fusion. |



 

La fonction OpenGL **glBlendFunc** et la fonction Iris GL **BLENDFUNCTION** sont presque identiques. Le tableau suivant répertorie les facteurs de mélange IRIS GL et leurs équivalents OpenGL.



| IRIS GL          | Technologie                     | Notes             |
|------------------|----------------------------|-------------------|
| BF \_ zéro         | \_zéro GL                   |                   |
| BF \_ 1          | GL \_ 1                    |                   |
| \_As BF           | source de la \_ source GL \_             |                   |
| BF \_ MSA          | GL \_ un \_ moins de \_ src \_ alpha |                   |
| BF \_ da           | de l' \_ heure d’été alpha du GL \_             |                   |
| \_Assistant débogage MANAGÉ BF          | GL \_ 1 \_ moins \_ heure d’été \_ alpha |                   |
| BF \_ SC           | couleur de la source du GL \_ \_             |                   |
| BF \_ msc          | GL \_ un \_ moins \_ \_ couleur SRC | Destination uniquement. |
| \_DC BF           | couleur de l' \_ heure d’été GL \_             | Source uniquement.      |
| Carte \_ fille BF          | \_couleur GL 1 \_ moins \_ DST \_ | Source uniquement.      |
| \_mini-MDA mn min \_ sa \_ | \_ \_ saturation alpha de la source GL \_   |                   |



 

??

 

 





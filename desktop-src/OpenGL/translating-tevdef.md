---
title: Traduction de tevdef
description: L’exemple de code suivant est une définition d’environnement de texture de GL d’IRIS qui spécifie le \_ paramètre d’environnement de texture de DÉCALCOMANIE TV
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Portage de l’IRIS dans le GL, texture
- Portage à partir de IRIS GL, texture
- portage vers OpenGL à partir de IRIS GL, texture
- Portage OpenGL à partir de IRIS GL, texture
- texture
- Portage du grand livre de l’IRIS, tevdef
- Portage à partir de IRIS GL, tevdef
- portage vers OpenGL à partir de IRIS GL, tevdef
- Portage OpenGL à partir de IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940280"
---
# <a name="translating-tevdef"></a>Traduction de tevdef

L’exemple de code suivant est une définition d’environnement de texture de GL d’IRIS qui spécifie le \_ paramètre d’environnement de texture de DÉCALCOMANIE TV :


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



et le même code traduit en OpenGL :


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



Le tableau suivant répertorie les paramètres d’environnement de texture du GL d’IRIS et leurs paramètres OpenGL équivalents.



| Paramètre IRIS GL     | Paramètre OpenGL             |
|-----------------------|------------------------------|
| \_modulation TV          | module comptabilité GL \_                 |
| \_DÉCALCOMANIE TV             | décalque GL \_                    |
| \_fusion TV             | fusion du GL \_                    |
| \_couleur TV             | couleur de la texture du GL \_ \_ env \_      |
| TV \_ alpha             | Aucun équivalent OpenGL direct. |
| \_sélection du composant TV \_ | Aucun équivalent OpenGL direct. |



 

Pour plus d’informations sur les paramètres de l’environnement de texture, consultez [**glTexEnv**](gltexenv-functions.md).

 

 





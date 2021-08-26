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
ms.openlocfilehash: 7feef33c2aa725c6e5bb91782fe43fdc6a84d23db8aa412f02c07b6ec588f719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887879"
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

 

 





---
title: Portage des appels de tampon d’accumulation
description: Vous devez allouer votre mémoire tampon d’accumulation en demandant le format de pixel approprié avec la fonction OpenGL auxInitDisplayMode ou ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Portage des tampons du GL d’IRIS, accumulation
- Portage à partir de IRIS GL, accumulation de mémoires tampons
- portage vers OpenGL depuis IRIS GL, accumulation de mémoires tampons
- Portage OpenGL depuis IRIS GL, accumulation de mémoires tampons
- mémoires tampons d’accumulation OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197426"
---
# <a name="porting-accumulation-buffer-calls"></a>Portage des appels de tampon d’accumulation

Vous devez allouer votre mémoire tampon d’accumulation en demandant le format de pixel approprié avec la fonction OpenGL **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) . Le tableau suivant répertorie les fonctions d’IRIS dans le GL qui affectent la mémoire tampon d’accumulation et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL       | Fonction OpenGL                                       | Signification                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             | **auxInitDisplayMode** ou **ChoosePixelFormat**       | Spécifie le nombre de bitplanes par composant de couleur dans la mémoire tampon d’accumulation. |
| **acbuf**              | [**glAccum**](glaccum.md)                            | Opère sur la mémoire tampon d’accumulation.                                          |
|                        | [**glClearAccum**](glclearaccum.md)                  | Définit des valeurs claires pour la mémoire tampon d’accumulation.                                    |
| **acbuf**(AC \_ Clear) | [**glClear**](glclear.md) ( \_ bit de tampon amort GL \_ \_ ) | Efface la mémoire tampon d’accumulation.                                               |



 

Le tableau suivant répertorie les paramètres **acbuf** de l’iris du GL ainsi que les paramètres [**glAccum**](glaccum.md) OpenGL équivalents.



| Paramètre IRIS GL     | Paramètre OpenGL |
|-----------------------|------------------|
| \_accumulation AC        | \_total amort        |
| \_accumulation d’effacement AC \_ | charge du GL \_         |
| \_retour AC            | \_retour GL       |
| AC \_ mult              | GL \_ mult         |
| \_Ajout AC               | ajout au GL \_          |



 

 

 





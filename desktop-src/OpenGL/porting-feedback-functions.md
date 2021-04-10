---
title: Portage des fonctions de commentaires
description: Avec IRIS GL, la façon dont les commentaires sont traités diffère selon l’ordinateur exécutant IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Portage de l’IRIS dans le GL, commentaires
- Portage à partir de IRIS GL, Feedback
- portage vers OpenGL à partir de IRIS GL, Feedback
- Portage OpenGL depuis IRIS GL, Feedback
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197167"
---
# <a name="porting-feedback-functions"></a>Portage des fonctions de commentaires

Avec IRIS GL, la façon dont les commentaires sont traités diffère selon l’ordinateur exécutant IRIS GL. OpenGL normalise les fonctions de commentaires pour vous permettre de vous reposer sur des commentaires cohérents entre différentes plateformes matérielles. Le tableau suivant répertorie les fonctions d’évaluation du GL de l’IRIS et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL | Fonction OpenGL                                                                                            | Signification                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **Commentaires**     | [**glRenderMode**](glrendermode.md) (commentaires sur le GL \_ )                                                      | Bascule en mode commentaires.                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) ( \_ rendu GL)[**glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | Bascule en mode de rendu.                   |
| **passage**  | [**glPassThrough**](glpassthrough.md)                                                                     | Place un marqueur de jeton dans la mémoire tampon de commentaires. |



 

 

 






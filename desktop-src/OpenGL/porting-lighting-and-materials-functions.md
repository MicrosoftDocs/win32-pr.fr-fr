---
title: Portage des fonctions d’éclairage et de matériaux
description: Les fonctions OpenGL pour l’éclairage et les matériaux diffèrent sensiblement des fonctions de la comptabilité IRIS. Contrairement à IRIS GL, OpenGL offre des fonctions distinctes pour définir les lumières, les modèles de lumière et les matériaux.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Portage du GL IRIS, éclairage
- Portage à partir de IRIS GL, éclairage
- portage vers OpenGL à partir de IRIS GL, éclairage
- Portage OpenGL à partir de IRIS GL, éclairage
- Portage de l’IRIS dans le GL, matériel
- Portage à partir de IRIS GL, matériaux
- portage vers OpenGL à partir de IRIS GL, matériel
- Portage OpenGL à partir de IRIS GL, matériaux
- éclairage
- destinés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c775670b7ae49e41fed35c192385c72e72e880b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840421"
---
# <a name="porting-lighting-and-materials-functions"></a>Portage des fonctions d’éclairage et de matériaux

Les fonctions OpenGL pour l’éclairage et les matériaux diffèrent sensiblement des fonctions de la comptabilité IRIS. Contrairement à IRIS GL, OpenGL offre des fonctions distinctes pour définir les lumières, les modèles de lumière et les matériaux.

Gardez les points suivants à l’esprit lorsque vous portez des fonctions d’éclairage et de matériaux :

-   OpenGL n’a pas de table de définitions stockées. Vous pouvez utiliser des listes d’affichage pour imiter le mécanisme def/bind du GL d’IRIS. Pour plus d’informations sur les defs et les liaisons, consultez [Portage des ensembles de paramètres, des liaisons et des jeux](porting-defs--binds--and-sets.md).
-   Avec OpenGL, l’atténuation est associée à chaque source de lumière, plutôt qu’au modèle d’éclairage global.
-   Les composants diffus et spéculaire sont séparés dans des sources de lumière OpenGL.
-   Les sources de lumière OpenGL ont un composant alpha. Lors du Portage de votre code IRIS GL, définissez ce composant alpha sur 1,0, indiquant une opacité de 100%. Les valeurs alpha sont ensuite déterminées par le composant alpha de vos matériaux uniquement. par conséquent, les objets de votre scène auront le même aspect que dans IRIS GL.

Le tableau suivant répertorie les fonctions d’éclairage et de matériaux de l’IRIS dans le GL et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                 | Fonction OpenGL                               | Signification                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef (dévols**,... **)**    | [glLight](gllight-functions.md)              | Définissez une source de lumière.                                        |
| **Imdef (DEFLMODEL**,... **)**   | [glLightModel](gllightmodel-functions.md)    | Définir un modèle d’éclairage.                                      |
| **Lier**                       | [**glEnable**](glenable.md) (GL \_ clair *i*) | Activer la lumière *i*.                                             |
| **Lier**                       | **glEnable**( \_ éclairage GL)                  | Activer l’éclairage.                                              |
| **Imdef (DEFMATERIAL**,... **)** | [**glMaterial**](glmaterial-functions.md)    | Définir un matériau.                                            |
| **Couleurs**                      | [**glColorMaterial**](glcolormaterial.md)    | Modifiez l’effet des commandes couleur lorsque l’éclairage est actif. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Obtient les paramètres de la documentation.                                      |



 

Le tableau suivant répertorie les différents paramètres de matériel de l’IRIS et leurs paramètres OpenGL équivalents.



| Index Imdef  | paramètre glMaterial                              | Default              | Signification                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| LETTRES        | \_diffusion GL                                       |                      | La quatrième valeur dans le \_ paramètre GL diffus spécifie la valeur alpha.                      |
| AMBIANT      | ambiant du GL \_                                       | (0,2, 0,2, 0,2, 1,0) | Couleur ambiante.                                                                                |
| DIFFUSE      | \_diffusion GL                                       | (0,8, 0,8, 0,8, 1,0) | Couleur diffuse.                                                                                |
| SPÉCULAIRE     | \_spéculaire GL                                      | (0,0, 0,0, 0,0, 1,0) | Couleur émissif.                                                                               |
| ÉCLAT    | SHININESSGL du GL- \_ \_ ambiant \_ et \_ diffuse<br/> | 0.0                  | Exposant spéculaire. Équivaut à appeler **glMaterial** deux fois avec les mêmes valeurs.<br/> |
| COLORINDEXES | \_index de couleurs GL \_                                |                      | Index de couleurs pour l’éclairage ambiant, diffus et spéculaire.                                    |



 

Lorsque le premier paramètre de **Imdef** est DEFMODEL, la traduction OpenGL équivalente est la fonction [**glLightModel**](gllightmodel-functions.md). L’exception est lorsque le paramètre suivant DEFMODEL est atténuation : la fonction OpenGL équivalente est [**glLight**](gllight-functions.md).

Le tableau suivant répertorie les paramètres de modèle d’éclairage équivalents pour IRIS GL et OpenGL.



| Index Imdef | paramètre glLightModel          | Default              | Signification                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| AMBIANT     | ambiant (GL \_ Light \_ Model) \_       | (0,2, 0,2, 0,2, 1,0) | Couleur ambiante de la scène.                          |
| ATTÉNUATION |                                 |                      | Consultez [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | \_ \_ visionneuse locale du modèle de lumière \_ GL \_ | GL- \_ faux            | Visionneuse locale (**true**) ou infinie (**false**). |
| TWOSIDE     | LIGHTMODEL du GL \_ \_ deux \_ côtés       | GL- \_ faux            | Utilisez l’éclairage à deux côtés lorsque la **valeur est true**.            |



 

Lorsque le premier paramètre de **Imdef** est devols, la traduction OpenGL équivalente est la fonction [**glLight**](gllight-functions.md) .

Le tableau suivant répertorie les paramètres d’éclairage équivalents pour IRIS GL et OpenGL.



| Index Imdef           | paramètre glLight                                                                                 | Default                                                                             | Signification                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| AMBIANT               | \_diffusion AMBIENTGLs GL \_<br/> \_spéculaire GL<br/>                                         | (0,0, 0,0, 0,0, 1,0) (1,0, 1,0, 1,0, 1,0)<br/> (1,0, 1,0, 1,0, 1,0)<br/> | Intensité ambiante. Intensité diffuse.<br/> Intensité spéculaire.<br/> |
| LCOLOR                | Aucun équivalent.                                                                                    |                                                                                     |                                                                                |
| POSITION              | \_position GL                                                                                      | (0,0, 0,0, 1,0, 0,0)                                                                | Position de la lumière.                                                             |
| SPOTDIRECTION         | \_sens du spot GL \_                                                                               | (0, 0, 1)                                                                           | Direction de la lumière.                                                        |
| VEDETTE             | découpage de l’emplacement \_ \_ EXPONENTGL GL \_ \_<br/>                                                     | 0180<br/>                                                                     | Distribution d’intensité. Angle d’étalement maximal de la source de lumière.<br/>        |
| DEFMODEL, ATTÉNUATION | \_ \_ \_ atténuation linéaire ATTENUATIONGL constante \_ GL<br/> \_atténuation quadratique du \_ GL<br/> | (1, 0, 0)                                                                           | Facteurs d’atténuation.                                                           |



 

 

 






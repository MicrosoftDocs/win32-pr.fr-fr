---
title: Utilisation des fonctions de requête
description: Utilisation des fonctions de requête
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, fonctions de requête
- fonctions de requête OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013980"
---
# <a name="using-the-query-functions"></a>Utilisation des fonctions de requête

Il existe quatre fonctions de requête pour obtenir des variables d’État simples et une pour déterminer si un état particulier est activé ou désactivé :

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

Les prototypes des fonctions de requête sont les suivants :

**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \** _ _params *);

**void** **glGetIntegerv**(**GLenum** *pname* , **glint \** _ _params *);

**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \** _ _params *);

**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \** _ _params *);

Respectivement, les fonctions de requête obtiennent des variables d’État booléennes, entières, à virgule flottante ou à double précision. Le paramètre *pname* est une constante symbolique indiquant la variable d’État à retourner, et *params* est un pointeur vers un tableau du type indiqué dans lequel placer les données retournées. Les valeurs possibles pour *pname* sont répertoriées dans les [variables d’État OpenGL](opengl-state-variables.md). Une conversion de type est effectuée si nécessaire pour retourner la variable souhaitée en tant que type de données demandé.

Le prototype de [**glIsEnabled**](glisenabled.md) est le suivant :

**GLboolean** **glIsEnabled**(GLenum *Cap* );

Si le mode spécifié par *Cap* est activé, **glIsEnabled** retourne la \_ valeur GL true. Si le mode spécifié par *Cap* est désactivé, **glIsEnabled** retourne GL \_ false. Les valeurs possibles pour *Cap* sont répertoriées dans les [variables d’État OpenGL](opengl-state-variables.md).

D’autres fonctions spécialisées retournent des variables d’État spécifiques. Pour savoir quand utiliser ces fonctions, consultez la page variables d’État OpenGL et le *Manuel de référence OpenGL*. Pour plus d’informations sur la fonctionnalité de gestion des erreurs de OpenGL et la fonction **glGetError** , consultez [gestion des erreurs](error-handling.md).

Les fonctions qui retournent des variables d’État spécifiques sont :

-   [**glGetClipPlane**](glgetclipplane.md)
-   [**glGetError**](glgeterror.md)
-   [**glGetLight**](glgetlight.md)
-   [**glGetMap**](glgetmap.md)
-   [**glGetMaterial**](glgetmaterial.md)
-   [**glGetPixelMap**](glgetpixelmap.md)
-   [**glGetPolygonStipple**](glgetpolygonstipple.md)
-   [**glGetString**](glgetstring.md)
-   [**glGetTexEnv**](glgettexenv.md)
-   [**glGetTexGen**](glgettexgen.md)
-   [**glGetTexImage**](glgetteximage.md)
-   [**glGetTexLevelParameter**](glgettexlevelparameter.md)
-   [**glGetTexParameter**](glgettexparameter.md)

 

 





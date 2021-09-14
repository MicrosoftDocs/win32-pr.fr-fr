---
title: Portage des fonctions d’extraction du GL IRIS
description: 'IRIS GL \ 0034 ; obtient \ 0034 ; les fonctions prennent la forme suivante :'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Optimiser le portage du GL, accéder aux fonctions
- Portage à partir de IRIS GL, fonctions d’extraction
- portage vers OpenGL à partir de IRIS GL, fonctions d’extraction
- Portage OpenGL depuis IRIS GL, fonctions d’extraction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127020971"
---
# <a name="porting-iris-gl-get-functions"></a>Portage des fonctions d’extraction du GL IRIS

Les fonctions « d’extraction » de l’IRIS GL prennent la forme suivante :

``` syntax
int getthing();
```

et

``` syntax
int getthings( int *a, int *b);
```

Votre code IRIS GL comprend probablement des appels de fonction d’extraction qui ressemblent à ceci :

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

Dans OpenGL, vous utilisez l’un des quatre types suivants de fonctions [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) à la place des fonctions équivalentes d’extraction de la comptabilité d’IRIS :

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

Les fonctions ont la syntaxe suivante :

``` syntax
glGet<Datatype>v( value, *data );
```

où la *valeur* est de type **GLenum** et les données sont de type **GLdatatype**. Quand vous appelez **glGet** et qu’il retourne un type différent du type attendu, le type est converti de manière appropriée. Pour obtenir la liste complète des paramètres **glGet** , consultez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 





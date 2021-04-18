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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512058"
---
# <a name="porting-iris-gl-get-functions"></a><span data-ttu-id="aa39b-107">Portage des fonctions d’extraction du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="aa39b-107">Porting IRIS GL Get Functions</span></span>

<span data-ttu-id="aa39b-108">Les fonctions « d’extraction » de l’IRIS GL prennent la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="aa39b-108">IRIS GL "get" functions take the following form:</span></span>

``` syntax
int getthing();
```

<span data-ttu-id="aa39b-109">et</span><span class="sxs-lookup"><span data-stu-id="aa39b-109">and</span></span>

``` syntax
int getthings( int *a, int *b);
```

<span data-ttu-id="aa39b-110">Votre code IRIS GL comprend probablement des appels de fonction d’extraction qui ressemblent à ceci :</span><span class="sxs-lookup"><span data-stu-id="aa39b-110">Your IRIS GL code probably includes get function calls that look something like:</span></span>

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

<span data-ttu-id="aa39b-111">Dans OpenGL, vous utilisez l’un des quatre types suivants de fonctions [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) à la place des fonctions équivalentes d’extraction de la comptabilité d’IRIS :</span><span class="sxs-lookup"><span data-stu-id="aa39b-111">In OpenGL you use one of the following four types of [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) functions in place of equivalent IRIS GL get functions:</span></span>

-   <span data-ttu-id="aa39b-112">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="aa39b-112">**glGetBooleanv**</span></span>
-   <span data-ttu-id="aa39b-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="aa39b-113">**glGetIntegerv**</span></span>
-   <span data-ttu-id="aa39b-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="aa39b-114">**glGetFloatv**</span></span>
-   <span data-ttu-id="aa39b-115">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="aa39b-115">**glGetDoublev**</span></span>

<span data-ttu-id="aa39b-116">Les fonctions ont la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="aa39b-116">The functions have the following syntax:</span></span>

``` syntax
glGet<Datatype>v( value, *data );
```

<span data-ttu-id="aa39b-117">où la *valeur* est de type **GLenum** et les données sont de type **GLdatatype**.</span><span class="sxs-lookup"><span data-stu-id="aa39b-117">where *value* is of type **GLenum** and data is of type **GLdatatype**.</span></span> <span data-ttu-id="aa39b-118">Quand vous appelez **glGet** et qu’il retourne un type différent du type attendu, le type est converti de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="aa39b-118">When you call **glGet** and it returns a type different from the type expected, the type is converted appropriately.</span></span> <span data-ttu-id="aa39b-119">Pour obtenir la liste complète des paramètres **glGet** , consultez [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="aa39b-119">For a complete list of **glGet** parameters, see [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span></span>

 

 





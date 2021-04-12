---
title: gluGetString, fonction (Glu. h)
description: La fonction gluGetString obtient une chaîne qui décrit le numéro de version GLU ou les appels d’extension GLU pris en charge.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- gluGetString fonction OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384460"
---
# <a name="glugetstring-function"></a><span data-ttu-id="69853-104">gluGetString fonction)</span><span class="sxs-lookup"><span data-stu-id="69853-104">gluGetString function</span></span>

<span data-ttu-id="69853-105">La fonction **gluGetString** obtient une chaîne qui décrit le numéro de version Glu ou les appels d’extension Glu pris en charge.</span><span class="sxs-lookup"><span data-stu-id="69853-105">The **gluGetString** function gets a string that describes the GLU version number or supported GLU extension calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="69853-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69853-106">Syntax</span></span>


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="69853-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69853-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69853-108">*name*</span><span class="sxs-lookup"><span data-stu-id="69853-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="69853-109">Le numéro de version de GLU ( \_ version Glu) ou des appels d’extension spécifiques au fournisseur ( \_ Extensions Glu) disponibles.</span><span class="sxs-lookup"><span data-stu-id="69853-109">Either the version number of GLU (GLU\_VERSION) or available vendor-specific extension calls (GLU\_EXTENSIONS).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69853-110">Notes</span><span class="sxs-lookup"><span data-stu-id="69853-110">Remarks</span></span>

<span data-ttu-id="69853-111">La fonction **gluGetString** retourne un pointeur vers une chaîne statique se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="69853-111">The **gluGetString** function returns a pointer to a static, null-terminated string.</span></span> <span data-ttu-id="69853-112">Quand le *nom* est Glu \_ version, la chaîne retournée est une valeur qui représente le numéro de version de Glu.</span><span class="sxs-lookup"><span data-stu-id="69853-112">When *name* is GLU\_VERSION, the returned string is a value that represents the version number of GLU.</span></span> <span data-ttu-id="69853-113">Le format du numéro de version est le suivant :</span><span class="sxs-lookup"><span data-stu-id="69853-113">The format of the version number is as follows:</span></span>

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

<span data-ttu-id="69853-114">Le numéro de version se présente sous la forme « \_ numéro principal. \_ nombre mineur » ou « numéro majeur. numéro de \_ \_ version secondaire \_ ».</span><span class="sxs-lookup"><span data-stu-id="69853-114">The version number has the form "major\_number.minor\_number" or "major\_number.minor\_number.release\_number".</span></span> <span data-ttu-id="69853-115">Les informations spécifiques au fournisseur sont facultatives, et le format et le contenu dépendent de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="69853-115">The vendor-specific information is optional, and the format and contents depend on the implementation.</span></span>

<span data-ttu-id="69853-116">Quand le *nom* est Glu \_ Extensions, la chaîne retournée contient une liste de noms d’extensions Glu prises en charge, séparées par des espaces.</span><span class="sxs-lookup"><span data-stu-id="69853-116">When *name* is GLU\_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces.</span></span> <span data-ttu-id="69853-117">Le format de la liste de noms retournée est le suivant :</span><span class="sxs-lookup"><span data-stu-id="69853-117">The format of the returned list of names is as follows:</span></span>

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

<span data-ttu-id="69853-118">Les noms d’extension ne peuvent pas contenir d’espaces.</span><span class="sxs-lookup"><span data-stu-id="69853-118">The extension names cannot contain any spaces.</span></span>

<span data-ttu-id="69853-119">La fonction **gluGetString** est valide pour GLU version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="69853-119">The **gluGetString** function is valid for GLU version 1.1 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="69853-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69853-120">Requirements</span></span>



| <span data-ttu-id="69853-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69853-121">Requirement</span></span> | <span data-ttu-id="69853-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="69853-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="69853-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69853-123">Minimum supported client</span></span><br/> | <span data-ttu-id="69853-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69853-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="69853-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69853-125">Minimum supported server</span></span><br/> | <span data-ttu-id="69853-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69853-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="69853-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="69853-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="69853-128"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="69853-128"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="69853-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69853-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="69853-130"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69853-130"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="69853-131">DLL</span><span class="sxs-lookup"><span data-stu-id="69853-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69853-132"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69853-132"><dt>Glu32.dll</dt></span></span> </dl> |



 

 






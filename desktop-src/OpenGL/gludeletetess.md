---
title: gluDeleteTess, fonction (Glu. h)
description: La fonction gluDeleteTess détruit un objet pavage.
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- gluDeleteTess fonction OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4625f0a9c2f51e9d7147c9564fcd4fb1fa7117
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740629"
---
# <a name="gludeletetess-function"></a><span data-ttu-id="f5827-104">gluDeleteTess fonction)</span><span class="sxs-lookup"><span data-stu-id="f5827-104">gluDeleteTess function</span></span>

<span data-ttu-id="f5827-105">La fonction **gluDeleteTess** détruit un objet pavage.</span><span class="sxs-lookup"><span data-stu-id="f5827-105">The **gluDeleteTess** function destroys a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5827-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5827-106">Syntax</span></span>


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="f5827-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5827-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5827-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="f5827-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="f5827-109">Objet de pavage à détruire (créé avec [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="f5827-109">The tessellation object to destroy (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5827-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f5827-110">Return value</span></span>

<span data-ttu-id="f5827-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f5827-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5827-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f5827-112">Remarks</span></span>

<span data-ttu-id="f5827-113">La fonction **gluDeleteTess** détruit l’objet de pavage indiqué et libère toute mémoire qu’il utilisait.</span><span class="sxs-lookup"><span data-stu-id="f5827-113">The **gluDeleteTess** function destroys the indicated tessellation object and frees any memory that it used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5827-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5827-114">Requirements</span></span>



| <span data-ttu-id="f5827-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5827-115">Requirement</span></span> | <span data-ttu-id="f5827-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5827-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f5827-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5827-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5827-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5827-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f5827-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5827-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5827-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5827-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f5827-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5827-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5827-122"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5827-122"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f5827-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5827-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5827-124"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5827-124"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5827-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f5827-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5827-126"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5827-126"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5827-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5827-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5827-128">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="f5827-128">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="f5827-129">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="f5827-129">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="f5827-130">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="f5827-130">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 






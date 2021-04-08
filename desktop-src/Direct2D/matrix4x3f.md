---
title: Matrix4x3F, classe (D2d1 \_ Helper. h)
description: La classe Matrix4x3F représente une matrice 4 par 3 et fournit des méthodes pratiques pour la création de matrices.
ms.assetid: 633B1828-0CB5-4CD3-9826-C65083C6C0A9
keywords:
- Classe Matrix4x3F Direct2D
- Classe Matrix4x3F Direct2D, Description
topic_type:
- apiref
api_name:
- Matrix4x3F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81467b51eb22586d537c7ea8032e13a30da19c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844414"
---
# <a name="matrix4x3f-class"></a><span data-ttu-id="3e63a-105">Matrix4x3F, classe</span><span class="sxs-lookup"><span data-stu-id="3e63a-105">Matrix4x3F class</span></span>

<span data-ttu-id="3e63a-106">La classe **Matrix4x3F** représente une matrice 4 par 3 et fournit des méthodes pratiques pour la création de matrices.</span><span class="sxs-lookup"><span data-stu-id="3e63a-106">The **Matrix4x3F** class represents a 4-by-3 matrix and provides convenience methods for creating matrices.</span></span>

## <a name="members"></a><span data-ttu-id="3e63a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3e63a-107">Members</span></span>

<span data-ttu-id="3e63a-108">La classe **Matrix4x3F** hérite de [**d2d1 \_ Matrix \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span><span class="sxs-lookup"><span data-stu-id="3e63a-108">The **Matrix4x3F** class inherits from [**D2D1\_MATRIX\_4X3\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span></span> <span data-ttu-id="3e63a-109">**Matrix4x3F** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3e63a-109">**Matrix4x3F** also has these types of members:</span></span>

-   [<span data-ttu-id="3e63a-110">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="3e63a-110">Constructors</span></span>](#constructors)

### <a name="constructors"></a><span data-ttu-id="3e63a-111">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="3e63a-111">Constructors</span></span>

<span data-ttu-id="3e63a-112">La classe **Matrix4x3F** contient ces constructeurs.</span><span class="sxs-lookup"><span data-stu-id="3e63a-112">The **Matrix4x3F** class has these constructors.</span></span>



| <span data-ttu-id="3e63a-113">Constructeur</span><span class="sxs-lookup"><span data-stu-id="3e63a-113">Constructor</span></span>                                                                                                                                                                                           | <span data-ttu-id="3e63a-114">Description</span><span class="sxs-lookup"><span data-stu-id="3e63a-114">Description</span></span>                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e63a-115">**Matrix4x3F()**</span><span class="sxs-lookup"><span data-stu-id="3e63a-115">**Matrix4x3F()**</span></span>](matrix4x3f-matrix4x3f--.md)                                                                                                                                                       | <span data-ttu-id="3e63a-116">Instancie une nouvelle instance d’une classe **Matrix4x3F** non initialisée.</span><span class="sxs-lookup"><span data-stu-id="3e63a-116">Instantiates a new instance of an uninitialized **Matrix4x3F** class.</span></span><br/>                                                   |
| [<span data-ttu-id="3e63a-117">**Matrix4x3F (FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT) (FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT)**</span><span class="sxs-lookup"><span data-stu-id="3e63a-117">**Matrix4x3F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)**</span></span>](matrix4x3f-matrix4x3f-floats-.md) | <span data-ttu-id="3e63a-118">Instancie une nouvelle instance d’une classe **Matrix4x3F** qui est initialisée avec toutes les valeurs de la matrice à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="3e63a-118">Instantiates a new instance of a **Matrix4x3F** class that is initialized with all of the floating point matrix values.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e63a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e63a-119">Requirements</span></span>



| <span data-ttu-id="3e63a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e63a-120">Requirement</span></span> | <span data-ttu-id="3e63a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e63a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e63a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e63a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3e63a-123">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3e63a-123">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="3e63a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e63a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3e63a-125">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3e63a-125">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="3e63a-126">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e63a-126">Minimum supported phone</span></span><br/>  | <span data-ttu-id="3e63a-127">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="3e63a-127">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="3e63a-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3e63a-128">Namespace</span></span><br/>                | <span data-ttu-id="3e63a-129">D2D1</span><span class="sxs-lookup"><span data-stu-id="3e63a-129">D2D1</span></span><br/>                                                                                                                          |
| <span data-ttu-id="3e63a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e63a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e63a-131"><dt>D2d1 \_ Helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e63a-131"><dt>D2d1\_helper.h</dt></span></span> </dl>                                                |
| <span data-ttu-id="3e63a-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e63a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e63a-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e63a-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="3e63a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3e63a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e63a-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e63a-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



## <a name="see-also"></a><span data-ttu-id="3e63a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e63a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e63a-137">**D2D1 \_ matrice \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="3e63a-137">**D2D1\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)
</dt> </dl>

 

 






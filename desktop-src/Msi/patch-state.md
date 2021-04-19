---
description: La propriété State retourne l’état d’installation de cette instance du correctif.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Propriété patch. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540037"
---
# <a name="patchstate-property"></a><span data-ttu-id="6a55d-103">Propriété patch. State</span><span class="sxs-lookup"><span data-stu-id="6a55d-103">Patch.State property</span></span>

<span data-ttu-id="6a55d-104">La propriété **State** retourne l’état d’installation de cette instance du correctif.</span><span class="sxs-lookup"><span data-stu-id="6a55d-104">The **State** property returns the installation state of this instance of the patch.</span></span>

<span data-ttu-id="6a55d-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a55d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a55d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a55d-106">Syntax</span></span>


```JScript
propVal = Patch.State
```



## <a name="property-value"></a><span data-ttu-id="6a55d-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6a55d-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6a55d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6a55d-108">Remarks</span></span>

<span data-ttu-id="6a55d-109">Cette propriété retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a55d-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="6a55d-110">État de l’installation</span><span class="sxs-lookup"><span data-stu-id="6a55d-110">Installation State</span></span>        | <span data-ttu-id="6a55d-111">Signification</span><span class="sxs-lookup"><span data-stu-id="6a55d-111">Meaning</span></span>                                                      |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6a55d-112">MSIPATCHSTATE \_ appliqué</span><span class="sxs-lookup"><span data-stu-id="6a55d-112">MSIPATCHSTATE\_APPLIED</span></span>    | <span data-ttu-id="6a55d-113">Le correctif est appliqué à cette instance de produit.</span><span class="sxs-lookup"><span data-stu-id="6a55d-113">Patch is applied to this product instance.</span></span>                   |
| <span data-ttu-id="6a55d-114">MSIPATCHSTATE \_ remplacé</span><span class="sxs-lookup"><span data-stu-id="6a55d-114">MSIPATCHSTATE\_SUPERSEDED</span></span> | <span data-ttu-id="6a55d-115">Le correctif est appliqué à cette instance de produit, mais il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="6a55d-115">Patch is applied to this product instance but is superseded.</span></span> |
| <span data-ttu-id="6a55d-116">MSIPATCHSTATE \_ obsolète</span><span class="sxs-lookup"><span data-stu-id="6a55d-116">MSIPATCHSTATE\_OBSOLETED</span></span>  | <span data-ttu-id="6a55d-117">Le correctif est appliqué dans cette instance du produit, mais il est obsolète.</span><span class="sxs-lookup"><span data-stu-id="6a55d-117">Patch is applied in this product instance but obsolete.</span></span>      |



 

<span data-ttu-id="6a55d-118">Cette méthode peut retourner \_ une erreur Unknown \_ patch, si l’objet [**patch**](patch-object.md) est initialisé avec une chaîne vide pour *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="6a55d-118">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a55d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a55d-119">Requirements</span></span>



| <span data-ttu-id="6a55d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a55d-120">Requirement</span></span> | <span data-ttu-id="6a55d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a55d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a55d-122">Version</span><span class="sxs-lookup"><span data-stu-id="6a55d-122">Version</span></span><br/> | <span data-ttu-id="6a55d-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a55d-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a55d-124">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a55d-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a55d-125">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6a55d-125">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="6a55d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6a55d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="6a55d-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a55d-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="6a55d-128">IID</span><span class="sxs-lookup"><span data-stu-id="6a55d-128">IID</span></span><br/>     | <span data-ttu-id="6a55d-129">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6a55d-129">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6a55d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a55d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a55d-131">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="6a55d-131">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="6a55d-132">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="6a55d-132">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="6a55d-133">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="6a55d-133">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





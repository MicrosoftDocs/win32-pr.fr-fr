---
description: La propriété Context retourne le contexte de ce correctif.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Patch. Context, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528621"
---
# <a name="patchcontext-property"></a><span data-ttu-id="a4a7a-103">Patch. Context, propriété</span><span class="sxs-lookup"><span data-stu-id="a4a7a-103">Patch.Context property</span></span>

<span data-ttu-id="a4a7a-104">La propriété **Context** retourne le contexte de ce correctif.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-104">The **Context** property returns the context of this patch.</span></span>

<span data-ttu-id="a4a7a-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a7a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4a7a-106">Syntax</span></span>


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a><span data-ttu-id="a4a7a-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a4a7a-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a7a-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a4a7a-108">Remarks</span></span>

<span data-ttu-id="a4a7a-109">Cette propriété retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="a4a7a-110">Context</span><span class="sxs-lookup"><span data-stu-id="a4a7a-110">Context</span></span>                        | <span data-ttu-id="a4a7a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4a7a-111">Value</span></span> | <span data-ttu-id="a4a7a-112">Signification</span><span class="sxs-lookup"><span data-stu-id="a4a7a-112">Meaning</span></span>                        |
|--------------------------------|-------|--------------------------------|
| <span data-ttu-id="a4a7a-113">MSIINSTALLCONTEXT \_ USERMANAGED</span><span class="sxs-lookup"><span data-stu-id="a4a7a-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="a4a7a-114">1</span><span class="sxs-lookup"><span data-stu-id="a4a7a-114">1</span></span>     | <span data-ttu-id="a4a7a-115">Correctif sous le contexte géré.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-115">Patch under managed context.</span></span>   |
| <span data-ttu-id="a4a7a-116">\_utilisateur MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="a4a7a-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="a4a7a-117">2</span><span class="sxs-lookup"><span data-stu-id="a4a7a-117">2</span></span>     | <span data-ttu-id="a4a7a-118">Correctif sous un contexte non managé.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-118">Patch under unmanaged context.</span></span> |
| <span data-ttu-id="a4a7a-119">\_machine MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="a4a7a-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="a4a7a-120">4</span><span class="sxs-lookup"><span data-stu-id="a4a7a-120">4</span></span>     | <span data-ttu-id="a4a7a-121">Correctif sous le contexte de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-121">Patch under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="a4a7a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4a7a-122">Requirements</span></span>



| <span data-ttu-id="a4a7a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4a7a-123">Requirement</span></span> | <span data-ttu-id="a4a7a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4a7a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a7a-125">Version</span><span class="sxs-lookup"><span data-stu-id="a4a7a-125">Version</span></span><br/> | <span data-ttu-id="a4a7a-126">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a4a7a-127">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a4a7a-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a4a7a-128">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a4a7a-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a4a7a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a7a-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4a7a-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4a7a-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a4a7a-131">IID</span><span class="sxs-lookup"><span data-stu-id="a4a7a-131">IID</span></span><br/>     | <span data-ttu-id="a4a7a-132">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a4a7a-132">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a4a7a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4a7a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a7a-134">**Objet patch**</span><span class="sxs-lookup"><span data-stu-id="a4a7a-134">**Patch Object**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="a4a7a-135">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="a4a7a-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





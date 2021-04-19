---
description: La méthode SetGroupName définit le nom défini par l’application du groupe.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'IAMTimelineGroup :: SetGroupName, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520822"
---
# <a name="iamtimelinegroupsetgroupname-method"></a><span data-ttu-id="b54d1-103">IAMTimelineGroup :: SetGroupName, méthode</span><span class="sxs-lookup"><span data-stu-id="b54d1-103">IAMTimelineGroup::SetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="b54d1-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b54d1-104">\[Deprecated.</span></span> <span data-ttu-id="b54d1-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b54d1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b54d1-106">La `SetGroupName` méthode définit le nom défini par l’application du groupe.</span><span class="sxs-lookup"><span data-stu-id="b54d1-106">The `SetGroupName` method sets the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b54d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b54d1-107">Syntax</span></span>


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="b54d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b54d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b54d1-109">*pGroupName*</span><span class="sxs-lookup"><span data-stu-id="b54d1-109">*pGroupName*</span></span> 
</dt> <dd>

<span data-ttu-id="b54d1-110">**BSTR** qui spécifie le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="b54d1-110">**BSTR** that specifies the name of the group.</span></span> <span data-ttu-id="b54d1-111">La longueur maximale du nom est de 256 caractères, incluant la marque de fin null.</span><span class="sxs-lookup"><span data-stu-id="b54d1-111">The maximum length of the name is 256 characters, incuding the null terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b54d1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b54d1-112">Return value</span></span>

<span data-ttu-id="b54d1-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b54d1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b54d1-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b54d1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b54d1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b54d1-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b54d1-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b54d1-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b54d1-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b54d1-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b54d1-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b54d1-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b54d1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b54d1-119">Requirements</span></span>



| <span data-ttu-id="b54d1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b54d1-120">Requirement</span></span> | <span data-ttu-id="b54d1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b54d1-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b54d1-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b54d1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b54d1-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b54d1-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b54d1-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b54d1-124">Library</span></span><br/> | <dl> <span data-ttu-id="b54d1-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b54d1-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b54d1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b54d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b54d1-127">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="b54d1-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="b54d1-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b54d1-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: La méthode GetGroupName récupère le nom défini par l’application du groupe.
ms.assetid: 402e97d9-abb5-4d8e-8735-1b06d60ab225
title: 'IAMTimelineGroup :: GetGroupName, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 78e3fc736ece3f4a8ebea1c688ce2bc5099f497c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545695"
---
# <a name="iamtimelinegroupgetgroupname-method"></a><span data-ttu-id="d8b9c-103">IAMTimelineGroup :: GetGroupName, méthode</span><span class="sxs-lookup"><span data-stu-id="d8b9c-103">IAMTimelineGroup::GetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="d8b9c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-104">\[Deprecated.</span></span> <span data-ttu-id="d8b9c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8b9c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d8b9c-106">La `GetGroupName` méthode récupère le nom défini par l’application du groupe.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-106">The `GetGroupName` method retrieves the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b9c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b9c-107">Syntax</span></span>


```C++
HRESULT GetGroupName(
  [out, retval] BSTR *pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="d8b9c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8b9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b9c-109">*pGroupName* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d8b9c-109">*pGroupName* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b9c-110">Reçoit le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-110">Receives the name of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b9c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8b9c-111">Return value</span></span>

<span data-ttu-id="d8b9c-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8b9c-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8b9c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b9c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d8b9c-114">Remarks</span></span>

<span data-ttu-id="d8b9c-115">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-115">The method allocates memory for the string.</span></span> <span data-ttu-id="d8b9c-116">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="d8b9c-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d8b9c-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d8b9c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d8b9c-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d8b9c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8b9c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8b9c-120">Requirements</span></span>



| <span data-ttu-id="d8b9c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8b9c-121">Requirement</span></span> | <span data-ttu-id="d8b9c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8b9c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b9c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8b9c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d8b9c-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b9c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d8b9c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8b9c-125">Library</span></span><br/> | <dl> <span data-ttu-id="d8b9c-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8b9c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b9c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b9c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b9c-128">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="d8b9c-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="d8b9c-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="d8b9c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





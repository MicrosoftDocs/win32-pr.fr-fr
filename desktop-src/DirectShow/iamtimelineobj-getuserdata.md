---
description: La méthode GetUserData récupère les données persistantes définies par l’application.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'IAMTimelineObj :: GetUserData, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541306"
---
# <a name="iamtimelineobjgetuserdata-method"></a><span data-ttu-id="876f9-103">IAMTimelineObj :: GetUserData, méthode</span><span class="sxs-lookup"><span data-stu-id="876f9-103">IAMTimelineObj::GetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="876f9-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="876f9-104">\[Deprecated.</span></span> <span data-ttu-id="876f9-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="876f9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="876f9-106">La `GetUserData` méthode récupère les données persistantes définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="876f9-106">The `GetUserData` method retrieves the application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="876f9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="876f9-107">Syntax</span></span>


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="876f9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="876f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="876f9-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="876f9-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="876f9-110">Pointeur vers une mémoire tampon qui reçoit les données.</span><span class="sxs-lookup"><span data-stu-id="876f9-110">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="876f9-111">Pour déterminer la taille de la mémoire tampon à allouer, attribuez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="876f9-111">To determine the size of buffer to allocate, set this parameter to **NULL**.</span></span> <span data-ttu-id="876f9-112">La taille requise est retournée dans *psize*.</span><span class="sxs-lookup"><span data-stu-id="876f9-112">The required size is returned in *pSize*.</span></span>

</dd> <dt>

<span data-ttu-id="876f9-113">*pSize*</span><span class="sxs-lookup"><span data-stu-id="876f9-113">*pSize*</span></span> 
</dt> <dd>

<span data-ttu-id="876f9-114">Reçoit la taille des données, en octets.</span><span class="sxs-lookup"><span data-stu-id="876f9-114">Receives the size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="876f9-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="876f9-115">Return value</span></span>

<span data-ttu-id="876f9-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="876f9-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="876f9-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="876f9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="876f9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="876f9-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="876f9-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="876f9-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="876f9-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="876f9-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="876f9-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="876f9-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="876f9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="876f9-122">Requirements</span></span>



| <span data-ttu-id="876f9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="876f9-123">Requirement</span></span> | <span data-ttu-id="876f9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="876f9-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="876f9-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="876f9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="876f9-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="876f9-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="876f9-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="876f9-127">Library</span></span><br/> | <dl> <span data-ttu-id="876f9-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="876f9-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="876f9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="876f9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876f9-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="876f9-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="876f9-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="876f9-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





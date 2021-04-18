---
description: La méthode SetUserData définit les données persistantes définies par l’application.
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: 'IAMTimelineObj :: SetUserData, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e09aafd614234827a704d8b9997f27981eb7c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526582"
---
# <a name="iamtimelineobjsetuserdata-method"></a><span data-ttu-id="56dcc-103">IAMTimelineObj :: SetUserData, méthode</span><span class="sxs-lookup"><span data-stu-id="56dcc-103">IAMTimelineObj::SetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="56dcc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="56dcc-104">\[Deprecated.</span></span> <span data-ttu-id="56dcc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="56dcc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56dcc-106">La `SetUserData` méthode définit les données persistantes définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="56dcc-106">The `SetUserData` method sets application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="56dcc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56dcc-107">Syntax</span></span>


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a><span data-ttu-id="56dcc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56dcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56dcc-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="56dcc-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="56dcc-110">Pointeur vers une mémoire tampon contenant les données.</span><span class="sxs-lookup"><span data-stu-id="56dcc-110">Pointer to a buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="56dcc-111">*Taille*</span><span class="sxs-lookup"><span data-stu-id="56dcc-111">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="56dcc-112">Taille des données, en octets.</span><span class="sxs-lookup"><span data-stu-id="56dcc-112">Size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56dcc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56dcc-113">Return value</span></span>

<span data-ttu-id="56dcc-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56dcc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56dcc-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56dcc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56dcc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="56dcc-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56dcc-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="56dcc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="56dcc-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="56dcc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="56dcc-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="56dcc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56dcc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56dcc-120">Requirements</span></span>



| <span data-ttu-id="56dcc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56dcc-121">Requirement</span></span> | <span data-ttu-id="56dcc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="56dcc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56dcc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="56dcc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="56dcc-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="56dcc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="56dcc-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56dcc-125">Library</span></span><br/> | <dl> <span data-ttu-id="56dcc-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56dcc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56dcc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56dcc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dcc-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="56dcc-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="56dcc-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="56dcc-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





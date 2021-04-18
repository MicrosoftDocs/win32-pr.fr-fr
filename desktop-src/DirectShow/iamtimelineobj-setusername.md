---
description: La méthode SetUserName définit un nom défini par l’application pour l’objet.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'IAMTimelineObj :: SetUserName, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540586"
---
# <a name="iamtimelineobjsetusername-method"></a><span data-ttu-id="475f6-103">IAMTimelineObj :: SetUserName, méthode</span><span class="sxs-lookup"><span data-stu-id="475f6-103">IAMTimelineObj::SetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="475f6-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="475f6-104">\[Deprecated.</span></span> <span data-ttu-id="475f6-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="475f6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="475f6-106">La `SetUserName` méthode définit un nom défini par l’application pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="475f6-106">The `SetUserName` method sets an application-defined name for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="475f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="475f6-107">Syntax</span></span>


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="475f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="475f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="475f6-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="475f6-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="475f6-110">Chaîne de caractères larges qui contient le nom.</span><span class="sxs-lookup"><span data-stu-id="475f6-110">Wide-character string that contains the name.</span></span> <span data-ttu-id="475f6-111">Les chaînes de plus de 256 caractères peuvent être tronquées.</span><span class="sxs-lookup"><span data-stu-id="475f6-111">Strings longer than 256 characters might be truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="475f6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="475f6-112">Return value</span></span>

<span data-ttu-id="475f6-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="475f6-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="475f6-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="475f6-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="475f6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="475f6-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="475f6-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="475f6-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="475f6-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="475f6-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="475f6-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="475f6-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="475f6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="475f6-119">Requirements</span></span>



| <span data-ttu-id="475f6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="475f6-120">Requirement</span></span> | <span data-ttu-id="475f6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="475f6-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="475f6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="475f6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="475f6-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="475f6-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="475f6-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="475f6-124">Library</span></span><br/> | <dl> <span data-ttu-id="475f6-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="475f6-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="475f6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="475f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475f6-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="475f6-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="475f6-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="475f6-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





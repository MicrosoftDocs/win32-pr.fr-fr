---
description: La méthode GetUserName récupère le nom défini par l’application de l’objet.
ms.assetid: 7d172ec5-9cb7-4418-a628-a109944077a6
title: 'IAMTimelineObj :: GetUserName, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: efca014493cb5631e058927256bd1586aaca7ab7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526584"
---
# <a name="iamtimelineobjgetusername-method"></a><span data-ttu-id="1e893-103">IAMTimelineObj :: GetUserName, méthode</span><span class="sxs-lookup"><span data-stu-id="1e893-103">IAMTimelineObj::GetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="1e893-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="1e893-104">\[Deprecated.</span></span> <span data-ttu-id="1e893-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1e893-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1e893-106">La `GetUserName` méthode récupère le nom défini par l’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1e893-106">The `GetUserName` method retrieves the object's application-defined name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e893-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e893-107">Syntax</span></span>


```C++
HRESULT GetUserName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1e893-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e893-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e893-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1e893-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1e893-110">Reçoit le nom de l’objet en tant que **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="1e893-110">Receives the name of the object as a **BSTR**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e893-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e893-111">Return value</span></span>

<span data-ttu-id="1e893-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e893-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e893-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e893-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e893-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1e893-114">Remarks</span></span>

<span data-ttu-id="1e893-115">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1e893-115">The method allocates memory for the string.</span></span> <span data-ttu-id="1e893-116">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1e893-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="1e893-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="1e893-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1e893-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1e893-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1e893-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1e893-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e893-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e893-120">Requirements</span></span>



| <span data-ttu-id="1e893-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e893-121">Requirement</span></span> | <span data-ttu-id="1e893-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e893-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e893-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e893-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1e893-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e893-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1e893-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e893-125">Library</span></span><br/> | <dl> <span data-ttu-id="1e893-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e893-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e893-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e893-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e893-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="1e893-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="1e893-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="1e893-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





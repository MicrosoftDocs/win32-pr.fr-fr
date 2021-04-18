---
description: La méthode GetVendorString récupère le nom du fournisseur. Pour les objets de moteur de rendu fournis par DirectShow, la chaîne du fournisseur est &\# 0034 ; Microsoft Corporation&\# 0034 ;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'IRenderEngine :: GetVendorString, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540585"
---
# <a name="irenderenginegetvendorstring-method"></a><span data-ttu-id="463e7-104">IRenderEngine :: GetVendorString, méthode</span><span class="sxs-lookup"><span data-stu-id="463e7-104">IRenderEngine::GetVendorString method</span></span>

> [!Note]  
> <span data-ttu-id="463e7-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="463e7-105">\[Deprecated.</span></span> <span data-ttu-id="463e7-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="463e7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="463e7-107">La `GetVendorString` méthode récupère le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="463e7-107">The `GetVendorString` method retrieves the name of the vendor.</span></span> <span data-ttu-id="463e7-108">Pour les objets de moteur de rendu fournis par DirectShow, la chaîne du fournisseur est « Microsoft Corporation ».</span><span class="sxs-lookup"><span data-stu-id="463e7-108">For the render engine objects that are provided by DirectShow, the vendor string is "Microsoft Corporation".</span></span>

## <a name="syntax"></a><span data-ttu-id="463e7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="463e7-109">Syntax</span></span>


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a><span data-ttu-id="463e7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="463e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="463e7-111">*pVendorID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="463e7-111">*pVendorID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="463e7-112">Reçoit un **BSTR** contenant la chaîne du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="463e7-112">Receives a **BSTR** containing the vendor string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="463e7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="463e7-113">Return value</span></span>

<span data-ttu-id="463e7-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="463e7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="463e7-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="463e7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="463e7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="463e7-116">Remarks</span></span>

<span data-ttu-id="463e7-117">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="463e7-117">The method allocates memory for the string.</span></span> <span data-ttu-id="463e7-118">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="463e7-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="463e7-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="463e7-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="463e7-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="463e7-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="463e7-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="463e7-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="463e7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="463e7-122">Requirements</span></span>



| <span data-ttu-id="463e7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="463e7-123">Requirement</span></span> | <span data-ttu-id="463e7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="463e7-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="463e7-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="463e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="463e7-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="463e7-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="463e7-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="463e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="463e7-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="463e7-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463e7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="463e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463e7-130">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="463e7-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="463e7-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="463e7-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





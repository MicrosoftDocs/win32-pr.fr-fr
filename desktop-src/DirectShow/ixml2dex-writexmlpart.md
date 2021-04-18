---
description: Non implémenté.
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: 'IXml2Dex :: WriteXMLPart, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8f194fe409d8ea94f786fe3802b2c758a1a00520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516156"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="40460-103">IXml2Dex :: WriteXMLPart, méthode</span><span class="sxs-lookup"><span data-stu-id="40460-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="40460-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="40460-104">\[Deprecated.</span></span> <span data-ttu-id="40460-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="40460-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="40460-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="40460-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="40460-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40460-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="40460-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40460-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40460-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="40460-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="40460-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="40460-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="40460-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="40460-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="40460-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="40460-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="40460-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="40460-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="40460-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="40460-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="40460-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="40460-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="40460-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="40460-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40460-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40460-117">Return value</span></span>

<span data-ttu-id="40460-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="40460-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40460-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="40460-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="40460-120">Notes</span><span class="sxs-lookup"><span data-stu-id="40460-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="40460-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="40460-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="40460-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="40460-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="40460-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="40460-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="40460-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40460-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40460-125">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="40460-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 




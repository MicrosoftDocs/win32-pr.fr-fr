---
description: La méthode WriteXML traduit une chronologie en une chaîne XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'IXml2Dex :: WriteXML, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545905"
---
# <a name="ixml2dexwritexml-method"></a><span data-ttu-id="482db-103">IXml2Dex :: WriteXML, méthode</span><span class="sxs-lookup"><span data-stu-id="482db-103">IXml2Dex::WriteXML method</span></span>

> [!Note]  
> <span data-ttu-id="482db-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="482db-104">\[Deprecated.</span></span> <span data-ttu-id="482db-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="482db-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="482db-106">La `WriteXML` méthode traduit une chronologie en une chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="482db-106">The `WriteXML` method translates a timeline to an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="482db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="482db-107">Syntax</span></span>


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a><span data-ttu-id="482db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="482db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="482db-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="482db-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="482db-110">Pointeur vers l’interface **IUnknown** de l’objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="482db-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="482db-111">*pbstrXML*</span><span class="sxs-lookup"><span data-stu-id="482db-111">*pbstrXML*</span></span> 
</dt> <dd>

<span data-ttu-id="482db-112">Pointeur vers une variable de type BSTR qui reçoit la chaîne XML décrivant la chronologie.</span><span class="sxs-lookup"><span data-stu-id="482db-112">Pointer to a variable of type BSTR that receives the XML string describing the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="482db-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="482db-113">Return value</span></span>

<span data-ttu-id="482db-114">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="482db-114">Returns S\_OK if successful.</span></span> <span data-ttu-id="482db-115">Si la mémoire est insuffisante pour la conversion, retourne E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="482db-115">If there is insufficient memory for the conversion, returns E\_OUTOFMEMORY.</span></span> <span data-ttu-id="482db-116">Sinon, retourne un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="482db-116">Otherwise, returns another error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="482db-117">Notes</span><span class="sxs-lookup"><span data-stu-id="482db-117">Remarks</span></span>

<span data-ttu-id="482db-118">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="482db-118">The method allocates memory for the string.</span></span> <span data-ttu-id="482db-119">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="482db-119">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="482db-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="482db-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="482db-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="482db-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="482db-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="482db-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="482db-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="482db-123">Requirements</span></span>



| <span data-ttu-id="482db-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="482db-124">Requirement</span></span> | <span data-ttu-id="482db-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="482db-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="482db-126">Version</span><span class="sxs-lookup"><span data-stu-id="482db-126">Version</span></span><br/> | <span data-ttu-id="482db-127">Internet Explorer 4,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="482db-127">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="482db-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="482db-128">Header</span></span><br/>  | <dl> <span data-ttu-id="482db-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="482db-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="482db-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="482db-130">Library</span></span><br/> | <dl> <span data-ttu-id="482db-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="482db-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="482db-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="482db-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482db-133">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="482db-133">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="482db-134">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="482db-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





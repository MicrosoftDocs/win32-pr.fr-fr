---
description: La méthode WriteXMLFile convertit une chronologie en XML et écrit les données XML dans un fichier.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'IXml2Dex :: WriteXMLFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533219"
---
# <a name="ixml2dexwritexmlfile-method"></a><span data-ttu-id="267fe-103">IXml2Dex :: WriteXMLFile, méthode</span><span class="sxs-lookup"><span data-stu-id="267fe-103">IXml2Dex::WriteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="267fe-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="267fe-104">\[Deprecated.</span></span> <span data-ttu-id="267fe-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="267fe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="267fe-106">La `WriteXMLFile` méthode convertit une chronologie en XML et écrit les données XML dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="267fe-106">The `WriteXMLFile` method translates a timeline to XML and writes the XML data to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="267fe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="267fe-107">Syntax</span></span>


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="267fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="267fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="267fe-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="267fe-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="267fe-110">Pointeur vers l’interface **IUnknown** de l’objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="267fe-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="267fe-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="267fe-112">Chaîne qui spécifie le nom du fichier à écrire.</span><span class="sxs-lookup"><span data-stu-id="267fe-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="267fe-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="267fe-113">Return value</span></span>

<span data-ttu-id="267fe-114">Retourne une valeur **HRESULT** qui dépend de l’implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="267fe-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="267fe-115">Le **HRESULT** peut inclure l’une des constantes standard suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="267fe-115">The **HRESULT** can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="267fe-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="267fe-116">Return code</span></span>                                                                                   | <span data-ttu-id="267fe-117">Description</span><span class="sxs-lookup"><span data-stu-id="267fe-117">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="267fe-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="267fe-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="267fe-119">L’argument n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="267fe-119">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="267fe-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="267fe-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="267fe-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="267fe-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="267fe-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="267fe-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="267fe-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="267fe-123">Success.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="267fe-124">Notes</span><span class="sxs-lookup"><span data-stu-id="267fe-124">Remarks</span></span>

<span data-ttu-id="267fe-125">Cette méthode génère un fichier XML qui représente tous les composants de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="267fe-125">This method generates an XML file that represents all the components in the timeline.</span></span>

> [!Note]  
> <span data-ttu-id="267fe-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="267fe-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="267fe-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="267fe-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="267fe-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="267fe-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="267fe-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="267fe-129">Requirements</span></span>



| <span data-ttu-id="267fe-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="267fe-130">Requirement</span></span> | <span data-ttu-id="267fe-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="267fe-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="267fe-132">Version</span><span class="sxs-lookup"><span data-stu-id="267fe-132">Version</span></span><br/> | <span data-ttu-id="267fe-133">Internet Explorer 4,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="267fe-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="267fe-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="267fe-134">Header</span></span><br/>  | <dl> <span data-ttu-id="267fe-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="267fe-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="267fe-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="267fe-136">Library</span></span><br/> | <dl> <span data-ttu-id="267fe-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="267fe-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="267fe-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="267fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267fe-139">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="267fe-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="267fe-140">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="267fe-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





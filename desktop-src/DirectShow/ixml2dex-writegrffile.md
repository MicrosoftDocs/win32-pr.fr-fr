---
description: La méthode WriteGrfFile écrit un graphique de filtre dans un fichier au format. GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'IXml2Dex :: WriteGrfFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538112"
---
# <a name="ixml2dexwritegrffile-method"></a><span data-ttu-id="8362a-103">IXml2Dex :: WriteGrfFile, méthode</span><span class="sxs-lookup"><span data-stu-id="8362a-103">IXml2Dex::WriteGrfFile method</span></span>

> [!Note]  
> <span data-ttu-id="8362a-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8362a-104">\[Deprecated.</span></span> <span data-ttu-id="8362a-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8362a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8362a-106">La `WriteGrfFile` méthode écrit un graphique de filtre dans un fichier au format. GRF.</span><span class="sxs-lookup"><span data-stu-id="8362a-106">The `WriteGrfFile` method writes a filter graph to a file in .grf format.</span></span>

## <a name="syntax"></a><span data-ttu-id="8362a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8362a-107">Syntax</span></span>


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="8362a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8362a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8362a-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="8362a-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="8362a-110">Pointeur vers l’interface **IUnknown** du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="8362a-110">Pointer to the filter graph's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="8362a-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="8362a-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="8362a-112">Chaîne qui spécifie le nom du fichier à écrire.</span><span class="sxs-lookup"><span data-stu-id="8362a-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8362a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8362a-113">Return value</span></span>

<span data-ttu-id="8362a-114">Retourne une valeur **HRESULT** qui dépend de l’implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="8362a-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="8362a-115">HRESULT peut inclure l’une des constantes standard suivantes, ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="8362a-115">HRESULT can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="8362a-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8362a-116">Return code</span></span>                                                                                  | <span data-ttu-id="8362a-117">Description</span><span class="sxs-lookup"><span data-stu-id="8362a-117">Description</span></span>                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="8362a-118"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8362a-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="8362a-119">Échec.</span><span class="sxs-lookup"><span data-stu-id="8362a-119">Failure.</span></span><br/>             |
| <dl> <span data-ttu-id="8362a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8362a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8362a-121">L’argument n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8362a-121">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="8362a-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8362a-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8362a-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="8362a-123">Success.</span></span><br/>             |



 

<span data-ttu-id="8362a-124">Cette méthode peut également retourner des codes d’erreur générés par des appels internes aux méthodes **IStorage :: CreateStream,** et **IPersist :: Save** .</span><span class="sxs-lookup"><span data-stu-id="8362a-124">This method can also return error codes generated by internal calls to the **IStorage::CreateStream** and **IPersist::Save** methods.</span></span> <span data-ttu-id="8362a-125">Pour plus d’informations, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="8362a-125">For more information, see the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8362a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="8362a-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8362a-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8362a-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8362a-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8362a-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8362a-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8362a-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8362a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8362a-130">Requirements</span></span>



| <span data-ttu-id="8362a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8362a-131">Requirement</span></span> | <span data-ttu-id="8362a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8362a-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8362a-133">Version</span><span class="sxs-lookup"><span data-stu-id="8362a-133">Version</span></span><br/> | <span data-ttu-id="8362a-134">Internet Explorer 4,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8362a-134">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="8362a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="8362a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8362a-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8362a-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8362a-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8362a-137">Library</span></span><br/> | <dl> <span data-ttu-id="8362a-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8362a-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8362a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8362a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8362a-140">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="8362a-140">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="8362a-141">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="8362a-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





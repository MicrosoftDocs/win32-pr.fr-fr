---
description: La méthode AddFoundLocation ajoute un répertoire au cache de répertoire.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'IMediaLocator :: AddFoundLocation, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76d878e5b013b8c6a061d777d4ec837bca85f8e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525155"
---
# <a name="imedialocatoraddfoundlocation-method"></a><span data-ttu-id="dbb9d-103">IMediaLocator :: AddFoundLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="dbb9d-103">IMediaLocator::AddFoundLocation method</span></span>

> [!Note]  
> <span data-ttu-id="dbb9d-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-104">\[Deprecated.</span></span> <span data-ttu-id="dbb9d-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dbb9d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dbb9d-106">La `AddFoundLocation` méthode ajoute un répertoire au cache de répertoire.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-106">The `AddFoundLocation` method adds a directory to the directory cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb9d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbb9d-107">Syntax</span></span>


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a><span data-ttu-id="dbb9d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbb9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbb9d-109">*DirectoryName*</span><span class="sxs-lookup"><span data-stu-id="dbb9d-109">*DirectoryName*</span></span> 
</dt> <dd>

<span data-ttu-id="dbb9d-110">Chemin d’accès au répertoire à ajouter au cache.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-110">Directory path to add to the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbb9d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbb9d-111">Return value</span></span>

<span data-ttu-id="dbb9d-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbb9d-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbb9d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbb9d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dbb9d-114">Remarks</span></span>

<span data-ttu-id="dbb9d-115">Le localisateur de média conserve un cache de chemins d’accès aux répertoires dans lesquels il a trouvé des fichiers dans les recherches précédentes.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-115">The media locator keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="dbb9d-116">Lorsqu’il localise correctement un fichier, il ajoute le répertoire au cache.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-116">When it successfully locates a file, it adds the directory to the cache.</span></span>

> [!Note]  
> <span data-ttu-id="dbb9d-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dbb9d-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dbb9d-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dbb9d-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dbb9d-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dbb9d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbb9d-120">Requirements</span></span>



| <span data-ttu-id="dbb9d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbb9d-121">Requirement</span></span> | <span data-ttu-id="dbb9d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbb9d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb9d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbb9d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="dbb9d-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbb9d-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dbb9d-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dbb9d-125">Library</span></span><br/> | <dl> <span data-ttu-id="dbb9d-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbb9d-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb9d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb9d-128">**Interface IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="dbb9d-128">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="dbb9d-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="dbb9d-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





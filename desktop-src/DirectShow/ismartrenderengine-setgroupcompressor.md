---
description: Spécifie un filtre de compression à utiliser lors du rendu du groupe spécifié.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'ISmartRenderEngine :: SetGroupCompressor, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545686"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a><span data-ttu-id="b48c1-103">ISmartRenderEngine :: SetGroupCompressor, méthode</span><span class="sxs-lookup"><span data-stu-id="b48c1-103">ISmartRenderEngine::SetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="b48c1-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b48c1-104">\[Deprecated.</span></span> <span data-ttu-id="b48c1-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b48c1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b48c1-106">Spécifie un filtre de compression à utiliser lors du rendu du groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="b48c1-106">Specifies a compression filter to use when rendering the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48c1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b48c1-107">Syntax</span></span>


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="b48c1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b48c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b48c1-109">*Groupe*</span><span class="sxs-lookup"><span data-stu-id="b48c1-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="b48c1-110">Index de base zéro du groupe.</span><span class="sxs-lookup"><span data-stu-id="b48c1-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="b48c1-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="b48c1-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="b48c1-112">Pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre de compression.</span><span class="sxs-lookup"><span data-stu-id="b48c1-112">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b48c1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b48c1-113">Return value</span></span>

<span data-ttu-id="b48c1-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b48c1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b48c1-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b48c1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b48c1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b48c1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b48c1-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b48c1-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b48c1-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b48c1-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b48c1-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b48c1-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b48c1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b48c1-120">Requirements</span></span>



| <span data-ttu-id="b48c1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b48c1-121">Requirement</span></span> | <span data-ttu-id="b48c1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b48c1-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b48c1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b48c1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b48c1-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b48c1-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b48c1-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b48c1-125">Library</span></span><br/> | <dl> <span data-ttu-id="b48c1-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b48c1-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b48c1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b48c1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48c1-128">**Interface ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="b48c1-128">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="b48c1-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b48c1-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





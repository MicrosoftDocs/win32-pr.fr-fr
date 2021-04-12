---
description: Fonction de rappel utilisée pour notifier l’hôte lorsqu’un chargement de la tranche de texture est terminé.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks :: LoadTextureSliceComplete, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 674288841ea08ad38c519e88abac4c64a1f1ca7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482393"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span data-ttu-id="faf0a-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks :: LoadTextureSliceComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="faf0a-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureSliceComplete method</span></span>

<span data-ttu-id="faf0a-104">Fonction de rappel utilisée pour notifier l’hôte lorsqu’un chargement de la tranche de texture est terminé.</span><span class="sxs-lookup"><span data-stu-id="faf0a-104">A callback function used to notify the host when a texture slice load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="faf0a-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a><span data-ttu-id="faf0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faf0a-106">Parameters</span></span>

<span data-ttu-id="faf0a-107">*sliceDesc* </span><span class="sxs-lookup"><span data-stu-id="faf0a-107">*sliceDesc* </span></span>  
<span data-ttu-id="faf0a-108">Descripteur de la tranche chargée.</span><span class="sxs-lookup"><span data-stu-id="faf0a-108">A descriptor of the loaded slice.</span></span>

<span data-ttu-id="faf0a-109">*histogramme* </span><span class="sxs-lookup"><span data-stu-id="faf0a-109">*histogram* </span></span>  
<span data-ttu-id="faf0a-110">Adresse des données d’histogramme pour la tranche chargée.</span><span class="sxs-lookup"><span data-stu-id="faf0a-110">The address of histogram data for the loaded slice.</span></span>

## <a name="return-value"></a><span data-ttu-id="faf0a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="faf0a-111">Return value</span></span>

<span data-ttu-id="faf0a-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="faf0a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="faf0a-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="faf0a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf0a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faf0a-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="faf0a-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="faf0a-115">Header</span></span></p></td><td><span data-ttu-id="faf0a-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="faf0a-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="faf0a-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faf0a-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="faf0a-118">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="faf0a-118">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 

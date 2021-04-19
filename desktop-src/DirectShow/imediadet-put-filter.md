---
description: La \_ méthode de filtre put spécifie un filtre source pour le détecteur de média à utiliser.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: IMediaDet ::p ut_Filter, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545466"
---
# <a name="imediadetput_filter-method"></a><span data-ttu-id="571fc-103">IMediaDet ::p \_ méthode de filtre ut</span><span class="sxs-lookup"><span data-stu-id="571fc-103">IMediaDet::put\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="571fc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="571fc-104">\[Deprecated.</span></span> <span data-ttu-id="571fc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="571fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="571fc-106">La `put_Filter` méthode spécifie un filtre source pour le détecteur de média à utiliser.</span><span class="sxs-lookup"><span data-stu-id="571fc-106">The `put_Filter` method specifies a source filter for the media detector to use.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="571fc-107">N’ajoutez pas le filtre source à votre propre graphique de filtre ou utilisez un filtre qui figure déjà dans un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="571fc-107">Do not add the source filter to your own filter graph, or use a filter that is already in a filter graph.</span></span> <span data-ttu-id="571fc-108">L’objet détecteur de média crée automatiquement un graphique de filtres interne, et le fait de placer le filtre dans un autre graphique peut entraîner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="571fc-108">The media detector object automatically builds an internal filter graph, and putting the filter in another graph can cause unexpected results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="571fc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="571fc-109">Syntax</span></span>


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="571fc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="571fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="571fc-111">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="571fc-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="571fc-112">Pointeur vers l’interface **IUnknown** du filtre source.</span><span class="sxs-lookup"><span data-stu-id="571fc-112">Pointer to the source filter's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="571fc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="571fc-113">Return value</span></span>

<span data-ttu-id="571fc-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="571fc-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="571fc-115">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="571fc-115">Possible values include the following:</span></span>



| <span data-ttu-id="571fc-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="571fc-116">Return code</span></span>                                                                                   | <span data-ttu-id="571fc-117">Description</span><span class="sxs-lookup"><span data-stu-id="571fc-117">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="571fc-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="571fc-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="571fc-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="571fc-119">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="571fc-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="571fc-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="571fc-121">*newVal* ne pointe pas vers un filtre.</span><span class="sxs-lookup"><span data-stu-id="571fc-121">*newVal* does not point to a filter.</span></span><br/> |
| <dl> <span data-ttu-id="571fc-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="571fc-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="571fc-123">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="571fc-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="571fc-124">Notes</span><span class="sxs-lookup"><span data-stu-id="571fc-124">Remarks</span></span>

<span data-ttu-id="571fc-125">Pour la plupart des applications, il est plus simple d’appeler la méthode [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) avec le nom d’un fichier source.</span><span class="sxs-lookup"><span data-stu-id="571fc-125">For most applications, it is simpler to call the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method with the name of a source file.</span></span>

> [!Note]  
> <span data-ttu-id="571fc-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="571fc-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="571fc-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="571fc-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="571fc-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="571fc-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="571fc-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="571fc-129">Requirements</span></span>



| <span data-ttu-id="571fc-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="571fc-130">Requirement</span></span> | <span data-ttu-id="571fc-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="571fc-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="571fc-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="571fc-132">Header</span></span><br/>  | <dl> <span data-ttu-id="571fc-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="571fc-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="571fc-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="571fc-134">Library</span></span><br/> | <dl> <span data-ttu-id="571fc-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="571fc-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="571fc-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="571fc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="571fc-137">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="571fc-137">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="571fc-138">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="571fc-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





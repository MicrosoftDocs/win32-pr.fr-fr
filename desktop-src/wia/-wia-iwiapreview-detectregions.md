---
description: 'Appelle le filtre de segmentation du pilote et passe l’image non filtrée mise en cache par la méthode IWiaPreview :: GetNewPreview au filtre.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: IWiaPreview ::D méthode etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201494"
---
# <a name="iwiapreviewdetectregions-method"></a><span data-ttu-id="3a3ad-103">IWiaPreview ::D méthode etectRegions</span><span class="sxs-lookup"><span data-stu-id="3a3ad-103">IWiaPreview::DetectRegions method</span></span>

<span data-ttu-id="3a3ad-104">Appelle le filtre de segmentation du pilote et passe l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) au filtre.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-104">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a3ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a3ad-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3a3ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a3ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a3ad-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a3ad-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a3ad-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="3a3ad-108">Type: **LONG**</span></span>

<span data-ttu-id="3a3ad-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-109">Not used.</span></span> <span data-ttu-id="3a3ad-110">A la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="3a3ad-110">Set to zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a3ad-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a3ad-111">Return value</span></span>

<span data-ttu-id="3a3ad-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3a3ad-112">Type: **HRESULT**</span></span>

<span data-ttu-id="3a3ad-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-113">This method can return one of these values.</span></span>



| <span data-ttu-id="3a3ad-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3a3ad-114">Return code</span></span>                                                                               | <span data-ttu-id="3a3ad-115">Description</span><span class="sxs-lookup"><span data-stu-id="3a3ad-115">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3a3ad-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a3ad-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3a3ad-117">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-117">The operation is successful.</span></span><br/>              |
| <dl> <span data-ttu-id="3a3ad-118"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a3ad-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="3a3ad-119">Le pilote ne prend pas en charge la segmentation.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-119">The driver does not support segmentation.</span></span><br/> |
| <dl> <span data-ttu-id="3a3ad-120"><dt>**dispose**</dt></span><span class="sxs-lookup"><span data-stu-id="3a3ad-120"><dt>**otherwise**</dt></span></span> </dl>  | <span data-ttu-id="3a3ad-121">Code d’erreur COM standard.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-121">A standard COM error code.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="3a3ad-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3a3ad-122">Remarks</span></span>

<span data-ttu-id="3a3ad-123">Une application doit appeler [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-123">An application must call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) before it calls this function.</span></span>

<span data-ttu-id="3a3ad-124">Lorsque le composant d’évaluation WIA (Windows Image Acquisition) 2,0 appelle **IWiaPreview ::D etectregions**, il appelle le filtre de segmentation de pilote et passe l’interface [**IWiaItem2**](-wia-iwiaitem2.md) précédemment passée à [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="3a3ad-124">When the Windows Image Acquisition (WIA) 2.0 Preview Component calls **IWiaPreview::DetectRegions**, it invokes the driver segmentation filter and passes the [**IWiaItem2**](-wia-iwiaitem2.md) interface that was previously passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="3a3ad-125">Il passe également l’image mise en cache en interne au filtre.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-125">It also passes the internally cached image to the filter.</span></span> <span data-ttu-id="3a3ad-126">Le filtre de segmentation utilise l’image mise en cache pour créer les extensions enfants.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-126">The segmentation filter uses the cached image to create the child extents.</span></span>

<span data-ttu-id="3a3ad-127">Si une application modifie des propriétés de l’interface [**IWiaItem2**](-wia-iwiaitem2.md) après avoir appelé [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), les propriétés d’origine doivent être restaurées avant que l’application n’appelle **IWiaPreview ::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-127">If an application changes any properties of the [**IWiaItem2**](-wia-iwiaitem2.md) interface after it calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), then the original properties must be restored before the application calls **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="3a3ad-128">Utilisez [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) et [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) pour restaurer les propriétés d’origine.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) to restore the original properties.</span></span>

<span data-ttu-id="3a3ad-129">**IWiaPreview ::D etectregions** est utilisé pour déterminer les « sous-régions » de l’image mise en cache.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-129">**IWiaPreview::DetectRegions** is used to determine the "sub-regions" of the cached image.</span></span> <span data-ttu-id="3a3ad-130">Pour chaque sous-région détectée, un nouvel élément enfant WIA 2,0 est créé sous l’interface [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="3a3ad-130">For each sub-region detected, a new child WIA 2.0 item is created under the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="3a3ad-131">Pour chaque élément enfant, le filtre de segmentation doit définir les valeurs des propriétés WIA 2,0 suivantes : WIA \_ IPS \_ xpos, WIA \_ IPS \_ Posy, WIA \_ IPS \_ XEXTENT et WIA \_ IPS \_ YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-131">For each child item, the segmentation filter must set the values for the following WIA 2.0 properties: WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT.</span></span> <span data-ttu-id="3a3ad-132">Un filtre plus avancé définit d’autres propriétés WIA 2,0, telles que \_ les adresses IP WIA par \_ \_ \_ décroisement X et les adresses IP WIA, décroissant \_ \_ Y, si le pilote prend en charge l’annulation de la distorsion.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-132">A more advanced filter sets other WIA 2.0 properties, such as WIA\_IPS\_DESKEW\_X and WIA\_IPS\_DESKEW\_Y, if the driver supports de-skewing.</span></span> <span data-ttu-id="3a3ad-133">Les \_ Propriétés WIA IPS \_ xpos, WIA \_ IPS \_ Posy, WIA \_ IPS \_ XEXTENT et WIA \_ IPS \_ YEXTENT représentent le rectangle englobant de la zone à analyser.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-133">The WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT properties represent the bounding rectangle of the area to scan.</span></span>

<span data-ttu-id="3a3ad-134">Le pilote ne prend peut-être pas en charge la segmentation.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-134">The driver might not support segmentation.</span></span> <span data-ttu-id="3a3ad-135">Avant d’appeler **IWiaPreview ::D etectregions**, une application vérifie généralement si le pilote prend en charge la \_ propriété de \_ segmentation IPS WIA.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-135">Before calling **IWiaPreview::DetectRegions**, an application typically checks whether the driver supports the WIA\_IPS\_SEGMENTATION property.</span></span> <span data-ttu-id="3a3ad-136">Si la propriété n’est pas implémentée, la segmentation n’est pas prise en charge et **IWiaPreview ::D etectregions** échoue et retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-136">If the property is not implemented, segmentation is not supported, and **IWiaPreview::DetectRegions** fails and returns E\_NOTIMPL.</span></span>

<span data-ttu-id="3a3ad-137">L’application doit nettoyer les éléments enfants créés en appelant **IWiaPreview ::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-137">The application must clean up the child items that are created by calling **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="3a3ad-138">Par exemple, si une application effectue un appel supplémentaire à **IWiaPreview ::D etectregions** sur le même élément, elle doit nettoyer les éléments enfants précédents.</span><span class="sxs-lookup"><span data-stu-id="3a3ad-138">For example, if an application makes an additional call to **IWiaPreview::DetectRegions** on the same item, it must clean up the previous child items.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a3ad-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a3ad-139">Requirements</span></span>



| <span data-ttu-id="3a3ad-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a3ad-140">Requirement</span></span> | <span data-ttu-id="3a3ad-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a3ad-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a3ad-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a3ad-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3a3ad-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a3ad-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a3ad-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a3ad-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3a3ad-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a3ad-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a3ad-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a3ad-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a3ad-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a3ad-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a3ad-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="3a3ad-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a3ad-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a3ad-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 





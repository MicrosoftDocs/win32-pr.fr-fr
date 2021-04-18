---
title: Image, élément (kit de développement logiciel (SDK) WMP)
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Image, élément (kit de développement logiciel (SDK) WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Élément image lecteur Windows Media
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540594"
---
# <a name="image-element-wmp-sdk"></a><span data-ttu-id="b34ad-105">Image, élément (kit de développement logiciel (SDK) WMP)</span><span class="sxs-lookup"><span data-stu-id="b34ad-105">Image Element (WMP SDK)</span></span>

> [!Note]  
> <span data-ttu-id="b34ad-106">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="b34ad-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b34ad-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b34ad-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b34ad-108">L’élément **image** spécifie les images que le lecteur Windows Media affiche à l’utilisateur pour représenter le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b34ad-108">The **Image** element specifies the images that Windows Media Player displays to the user to represent the online store.</span></span>

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="b34ad-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="b34ad-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="b34ad-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (requis pour les magasins de type 1, ignoré pour le type 2)</span><span class="sxs-lookup"><span data-stu-id="b34ad-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (required for type 1 stores, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="b34ad-111">URL du logo affiché par le lecteur Windows Media dans la boîte de dialogue contrat de licence utilisateur final (CLUF).</span><span class="sxs-lookup"><span data-stu-id="b34ad-111">URL for the logo that Windows Media Player displays in the end user license agreement (EULA) dialog box.</span></span> <span data-ttu-id="b34ad-112">Il doit s’agir d’une image PNG de 80 x 80 pixels.</span><span class="sxs-lookup"><span data-stu-id="b34ad-112">This must be a PNG image that is 80 x 80 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b34ad-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b34ad-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="b34ad-114">URL de l’image affichée par le lecteur Windows Media dans le menu Services.</span><span class="sxs-lookup"><span data-stu-id="b34ad-114">URL for the image that Windows Media Player displays on the services menu.</span></span> <span data-ttu-id="b34ad-115">Cette image doit être de 15 x 15 pixels.</span><span class="sxs-lookup"><span data-stu-id="b34ad-115">This image must be 15 x 15 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b34ad-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b34ad-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="b34ad-117">Pour une boutique en ligne de type 1, il s’agit de l’URL de l’image affichée par le lecteur Windows Media sur l’onglet **magasins en ligne** . Pour le lecteur Windows Media 11, cette image doit être de 45 pixels de large sur 13 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="b34ad-117">For a type 1 online store, this is the URL for the image that Windows Media Player displays on the **Online Stores** tab. For Windows Media Player 11, this image must be 45 pixels wide by 13 pixels high.</span></span> <span data-ttu-id="b34ad-118">Pour le lecteur Windows Media 12, cette image doit être de 45 pixels de large sur 30 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="b34ad-118">For Windows Media Player 12, this image must be 45 pixels wide by 30 pixels high.</span></span> <span data-ttu-id="b34ad-119">Pour prendre en charge les versions 11 et 12 du lecteur Windows Media, vous devez fournir deux documents ServiceInfo.xml distincts, chacun pointant vers l’image de taille appropriée pour ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="b34ad-119">To support both versions 11 and 12 of Windows Media Player, you must provide two separate ServiceInfo.xml documents, each of which points to the appropriately sized image for ServiceLargeURL.</span></span>

<span data-ttu-id="b34ad-120">Pour un magasin de type 2 en ligne, il s’agit de l’URL de l’image que le lecteur Windows Media affiche en regard de l’onglet **magasins en ligne** ou à côté des boutons du volet de tâches.</span><span class="sxs-lookup"><span data-stu-id="b34ad-120">For a type 2 online store, this is the URL for the image that Windows Media Player displays beside the **Online Stores** tab or beside the task pane buttons.</span></span> <span data-ttu-id="b34ad-121">Cette image doit être de 30 x 30 pixels.</span><span class="sxs-lookup"><span data-stu-id="b34ad-121">This image must be 30 x 30 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b34ad-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b34ad-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="b34ad-123">URL du logo qui s’affiche avec la description marketing spécifiée dans l’élément **Description** .</span><span class="sxs-lookup"><span data-stu-id="b34ad-123">URL for the logo that is displayed along with the marketing description specified in the **Description** element.</span></span> <span data-ttu-id="b34ad-124">S’il n’est pas fourni, il est vide.</span><span class="sxs-lookup"><span data-stu-id="b34ad-124">If it is not supplied, it will be blank.</span></span> <span data-ttu-id="b34ad-125">(Tous les types, facultatifs) Il doit s’agir d’une image PNG de 45 pixels de large et de 13 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="b34ad-125">(All types, optional) This must be a PNG image that is 45 pixels wide and 13 pixels high.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="b34ad-126">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="b34ad-126">Parent/Child Elements</span></span>



| <span data-ttu-id="b34ad-127">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b34ad-127">Hierarchy</span></span>       | <span data-ttu-id="b34ad-128">Élément</span><span class="sxs-lookup"><span data-stu-id="b34ad-128">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="b34ad-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b34ad-129">Parent elements</span></span> | <span data-ttu-id="b34ad-130">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b34ad-130">**ServiceInfo**</span></span> |
| <span data-ttu-id="b34ad-131">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b34ad-131">Child elements</span></span>  | <span data-ttu-id="b34ad-132">Aucune</span><span class="sxs-lookup"><span data-stu-id="b34ad-132">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b34ad-133">Notes</span><span class="sxs-lookup"><span data-stu-id="b34ad-133">Remarks</span></span>

<span data-ttu-id="b34ad-134">Les formats d’image pris en charge sont. gif,. jpg,. bmp et. png (format recommandé).</span><span class="sxs-lookup"><span data-stu-id="b34ad-134">The supported image formats are .gif, .jpg, .bmp, and .png (which is the recommended format).</span></span> <span data-ttu-id="b34ad-135">L’utilisation de la transparence Web est prise en charge et recommandée.</span><span class="sxs-lookup"><span data-stu-id="b34ad-135">Using Web transparency is both supported and recommended.</span></span> <span data-ttu-id="b34ad-136">Les fichiers GIF animés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b34ad-136">Animated GIF files are not supported.</span></span>

<span data-ttu-id="b34ad-137">Si vous ne fournissez pas de valeur pour **MenuURL**, le lecteur Windows Media n’affiche aucun graphique dans le menu de votre magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b34ad-137">If you do not supply a value for **MenuURL**, Windows Media Player displays no graphic on the menu for your online store.</span></span>

<span data-ttu-id="b34ad-138">Vous pouvez fournir une image animée pour ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="b34ad-138">You can provide an animated image for ServiceLargeURL.</span></span> <span data-ttu-id="b34ad-139">Dans le lecteur Windows Media 10 ou 11, l’image est animée.</span><span class="sxs-lookup"><span data-stu-id="b34ad-139">In Windows Media Player 10 or 11, the image is animated.</span></span> <span data-ttu-id="b34ad-140">Dans le lecteur Windows Media 12, seule la première image de l’image est affichée.</span><span class="sxs-lookup"><span data-stu-id="b34ad-140">In Windows Media Player 12, only the first frame of the image is displayed.</span></span> <span data-ttu-id="b34ad-141">Pour fournir une image animée, créez un fichier image unique qui contient des frames successifs de votre animation.</span><span class="sxs-lookup"><span data-stu-id="b34ad-141">To provide an animated image, create a single image file that contains successive frames of your animation.</span></span> <span data-ttu-id="b34ad-142">Par exemple, pour une image d’une largeur de 30 pixels et de 30 pixels de haut, vous pouvez fournir 20 images successives côte à côte dans une image de 600 pixels de large et de 30 pixels de haut.</span><span class="sxs-lookup"><span data-stu-id="b34ad-142">For example, for an image that is 30 pixels wide and 30 pixels high, you could supply 20 successive images side by side in an image that is 600 pixels wide and 30 pixels high.</span></span> <span data-ttu-id="b34ad-143">Le lecteur Windows Media animera automatiquement une image de ce type en présentant les 20 images individuelles l’une après l’autre.</span><span class="sxs-lookup"><span data-stu-id="b34ad-143">Windows Media Player would automatically animate such an image by showing the 20 individual images one after another.</span></span> <span data-ttu-id="b34ad-144">Cette animation se produit une seule fois lors de l’ouverture du magasin en ligne. elle ne se répète pas.</span><span class="sxs-lookup"><span data-stu-id="b34ad-144">This animation occurs only once when the online store opens; it does not repeat.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34ad-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b34ad-145">Requirements</span></span>



| <span data-ttu-id="b34ad-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b34ad-146">Requirement</span></span> | <span data-ttu-id="b34ad-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="b34ad-147">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="b34ad-148">Version</span><span class="sxs-lookup"><span data-stu-id="b34ad-148">Version</span></span><br/> | <span data-ttu-id="b34ad-149">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b34ad-149">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b34ad-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b34ad-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34ad-151">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="b34ad-151">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="b34ad-152">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="b34ad-152">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="b34ad-153">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="b34ad-153">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






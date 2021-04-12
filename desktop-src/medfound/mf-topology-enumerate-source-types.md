---
description: Spécifie si le chargeur de topologie énumère les types de médias fournis par la source du média.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: Attribut MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318301"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a><span data-ttu-id="f2ef6-103">\_Attribut de l' \_ énumération \_ des \_ types de source de la topologie MF</span><span class="sxs-lookup"><span data-stu-id="f2ef6-103">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute</span></span>

<span data-ttu-id="f2ef6-104">Spécifie si le chargeur de topologie énumère les types de médias fournis par la source du média.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-104">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="f2ef6-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f2ef6-105">Data type</span></span>

<span data-ttu-id="f2ef6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f2ef6-106">**UINT32**</span></span>

<span data-ttu-id="f2ef6-107">Utilisez l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-107">Use one of the following values.</span></span>



| <span data-ttu-id="f2ef6-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2ef6-108">Value</span></span>                                                                                                                                    | <span data-ttu-id="f2ef6-109">Signification</span><span class="sxs-lookup"><span data-stu-id="f2ef6-109">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="f2ef6-110"><dt>FALSe \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f2ef6-110"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="f2ef6-111">N’énumère pas les types de médias sources.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-111">Do not enumerate the source media types.</span></span><br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="f2ef6-112"><dt>VRAI \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f2ef6-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="f2ef6-113">Énumérer les types de médias sources.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-113">Enumerate the source media types.</span></span><br/>        |



 

## <a name="getset"></a><span data-ttu-id="f2ef6-114">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f2ef6-114">Get/set</span></span>

<span data-ttu-id="f2ef6-115">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f2ef6-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f2ef6-116">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f2ef6-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f2ef6-117">S’applique à</span><span class="sxs-lookup"><span data-stu-id="f2ef6-117">Applies to</span></span>

[<span data-ttu-id="f2ef6-118">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="f2ef6-118">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="f2ef6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f2ef6-119">Remarks</span></span>

<span data-ttu-id="f2ef6-120">Chaque flux sur une source de média peut offrir plusieurs types de média.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-120">Each stream on a media source can offer more than one media type.</span></span> <span data-ttu-id="f2ef6-121">La liste de types est énumérée via l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) sur le descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-121">The list of types is enumerated through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream descriptor.</span></span>

<span data-ttu-id="f2ef6-122">L’ordre dans lequel le chargeur de topologie tente d’obtenir les types de média d’une source multimédia est contrôlé par deux attributs :</span><span class="sxs-lookup"><span data-stu-id="f2ef6-122">The order in which the topology loader tries a media source's media types is controlled by two attributes:</span></span>

-   <span data-ttu-id="f2ef6-123">L' \_ \_ attribut de topologie MF énumérer les \_ \_ types de sources sur la topologie.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-123">The MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute on the topology.</span></span>
-   <span data-ttu-id="f2ef6-124">Attribut [**de \_ \_ \_ méthode de connexion MF TOPONODE**](mf-toponode-connect-method-attribute.md) sur le nœud source.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-124">The [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="f2ef6-125">Si l’attribut de la \_ topologie MF \_ énumérer les \_ \_ types de source est **false** ou non défini, le chargeur de topologie utilise le type de média actuel du flux.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-125">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **FALSE** or not set, the topology loader uses the stream's current media type.</span></span> <span data-ttu-id="f2ef6-126">Elle n’énumère pas la liste des types possibles.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-126">It does not enumerate the list of possible types.</span></span> <span data-ttu-id="f2ef6-127">Si le type de média actuel n’est pas compatible avec le nœud de topologie en aval et qu’aucune combinaison de décodeurs/convertisseurs ne peut être trouvée, la résolution de la topologie échoue.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-127">If the current media type is incompatible with the downstream topology node, and no combination of decoders/converters can be found, topology resolution fails.</span></span>

<span data-ttu-id="f2ef6-128">Si l’attribut de la \_ topologie MF \_ énumérer les \_ \_ types de sources a la **valeur true**, le chargeur de topologie énumère les types de médias de la source jusqu’à ce qu’il trouve un type compatible.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-128">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **TRUE**, the topology loader enumerates the source's media types until it finds a compatible type.</span></span> <span data-ttu-id="f2ef6-129">Dans ce cas, l’ordre exact des opérations varie selon que l’attribut [**de \_ \_ \_ méthode MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) sur le nœud source comprend l’indicateur **MF \_ Connect \_ Resolve \_ Independent \_ sortie OutputTypes** .</span><span class="sxs-lookup"><span data-stu-id="f2ef6-129">In that case, the exact order of operations depends on the whether the [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node includes the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span>

<span data-ttu-id="f2ef6-130">Si \_ la topologie MF \_ énumérer \_ \_ les types de sources a la **valeur true** et que l’indicateur **MF \_ Connect \_ Resolve \_ Independent \_ sortie OutputTypes** est défini, le chargeur de topologie épuise chaque type de média avant de passer au suivant, comme suit :</span><span class="sxs-lookup"><span data-stu-id="f2ef6-130">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** and the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set, the topology loader exhausts each media type before moving to the next, as follows:</span></span>

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

<span data-ttu-id="f2ef6-131">Si \_ la topologie MF \_ \_ d’énumération \_ des types de source est **vraie** mais que la résolution de la **\_ connexion MF \_ \_ \_ sortie OutputTypes** n’est pas définie, le chargeur de topologie tente une connexion directe avec chaque type de média, puis tente chaque type de média avec des convertisseurs, et enfin essaie chaque type de média avec des décodeurs :</span><span class="sxs-lookup"><span data-stu-id="f2ef6-131">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** but **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** is not set, the topology loader tries a direct connection with each media type, then tries each media type with converters, and finally tries each media type with decoders:</span></span>

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

<span data-ttu-id="f2ef6-132">Si \_ la topologie MF \_ énumérer \_ \_ les types de sources a la **valeur false**, l’indicateur de **\_ \_ résolution \_ \_ sortie OutputTypes de la connexion MF MF** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-132">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is ignored.</span></span>

<span data-ttu-id="f2ef6-133">La valeur par défaut de la \_ topologie MF \_ énumérer les types de \_ source \_ est **false**, pour la compatibilité avec les applications existantes.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-133">The default value of MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, for compatibility with existing applications.</span></span>

<span data-ttu-id="f2ef6-134">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-134">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="example"></a><span data-ttu-id="f2ef6-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2ef6-135">Example</span></span>

<span data-ttu-id="f2ef6-136">Voici un exemple qui illustre l’indicateur de **\_ résolution de \_ \_ \_ sortie OutputTypes indépendant de la connexion MF** .</span><span class="sxs-lookup"><span data-stu-id="f2ef6-136">Here is an example that illustrates the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span> <span data-ttu-id="f2ef6-137">Supposons que la topologie a l' \_ attribut de la topologie MF \_ énumérer les \_ \_ types de source défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-137">Assume the topology has the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute set to **TRUE**.</span></span>

<span data-ttu-id="f2ef6-138">La source du média offre les types suivants :</span><span class="sxs-lookup"><span data-stu-id="f2ef6-138">The media source offers the following types:</span></span>

-   <span data-ttu-id="f2ef6-139">T1, T2, T3</span><span class="sxs-lookup"><span data-stu-id="f2ef6-139">T1, T2, T3</span></span>

<span data-ttu-id="f2ef6-140">Le récepteur multimédia accepte les types suivants :</span><span class="sxs-lookup"><span data-stu-id="f2ef6-140">The media sink accepts the following types:</span></span>

-   <span data-ttu-id="f2ef6-141">T3, T4</span><span class="sxs-lookup"><span data-stu-id="f2ef6-141">T3, T4</span></span>

<span data-ttu-id="f2ef6-142">Cas 1 : l’indicateur de **\_ résolution de \_ \_ \_ sortie OutputTypes indépendant de la connexion MF** est défini.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-142">Case 1: The **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set.</span></span>

1.  <span data-ttu-id="f2ef6-143">Le chargeur de topologie tente une connexion directe avec T1.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-143">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="f2ef6-144">Le récepteur rejette T1.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-144">The sink rejects T1.</span></span>
2.  <span data-ttu-id="f2ef6-145">Le chargeur de topologie insère un décodeur qui accepte T1 et des sorties T4.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-145">The topology loader inserts a decoder that accepts T1 and outputs T4.</span></span> <span data-ttu-id="f2ef6-146">Le récepteur accepte T4.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-146">The sink accepts T4.</span></span>
3.  <span data-ttu-id="f2ef6-147">La topologie finale contient : source du média → décodeur → récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-147">The final topology contains: media source → decoder → media sink.</span></span>

<span data-ttu-id="f2ef6-148">Cas 2 : l’indicateur n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-148">Case 2: The flag is not set.</span></span>

1.  <span data-ttu-id="f2ef6-149">Le chargeur de topologie tente une connexion directe avec T1.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-149">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="f2ef6-150">Le récepteur rejette T1.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-150">The sink rejects T1.</span></span>
2.  <span data-ttu-id="f2ef6-151">Le chargeur de topologie tente une connexion directe avec T2.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-151">The topology loader tries a direct connection with T2.</span></span> <span data-ttu-id="f2ef6-152">Le récepteur rejette T2.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-152">The sink rejects T2.</span></span>
3.  <span data-ttu-id="f2ef6-153">Le chargeur de topologie tente une connexion directe avec T3.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-153">The topology loader tries a direct connection with T3.</span></span> <span data-ttu-id="f2ef6-154">Le récepteur accepte T3.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-154">The sink accepts T3.</span></span>
4.  <span data-ttu-id="f2ef6-155">La topologie finale contient : source du média → récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="f2ef6-155">The final topology contains: media source → media sink.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ef6-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2ef6-156">Requirements</span></span>



| <span data-ttu-id="f2ef6-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2ef6-157">Requirement</span></span> | <span data-ttu-id="f2ef6-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2ef6-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ef6-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2ef6-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ef6-160">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2ef6-160">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f2ef6-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2ef6-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ef6-162">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2ef6-162">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f2ef6-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2ef6-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ef6-164"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ef6-164"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ef6-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2ef6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ef6-166">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2ef6-166">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f2ef6-167">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="f2ef6-167">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 





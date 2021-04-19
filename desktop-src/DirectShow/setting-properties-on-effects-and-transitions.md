---
description: Définition des propriétés des effets et des transitions
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Définition des propriétés des effets et des transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ddd129eb9d4ab24ebef6f5c760a4211f26c9a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514704"
---
# <a name="setting-properties-on-effects-and-transitions"></a><span data-ttu-id="9a9d4-103">Définition des propriétés des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="9a9d4-103">Setting Properties on Effects and Transitions</span></span>

<span data-ttu-id="9a9d4-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="9a9d4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9a9d4-105">De nombreux effets et transitions de [services d’édition DirectShow](directshow-editing-services.md) prennent en charge des propriétés qui contrôlent leur comportement.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-105">Many [DirectShow Editing Services](directshow-editing-services.md) effects and transitions support properties that control their behavior.</span></span> <span data-ttu-id="9a9d4-106">Une application peut définir la valeur d’une propriété à l’aide de l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="9a9d4-106">An application can set the value of a property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="9a9d4-107">L’effet sous-jacent ou l’objet de transition doit prendre en charge **IDispatch** pour définir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-107">The underlying effect or transition object must support **IDispatch** for setting the properties.</span></span> <span data-ttu-id="9a9d4-108">Avec les effets vidéo et les transitions, l’application peut définir une plage de valeurs qui changent au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-108">With video effects and transitions, the application can set a range of values that change over time.</span></span> <span data-ttu-id="9a9d4-109">(Par exemple, vous pouvez définir une transition de réinitialisation pour vous déplacer d’une image à l’autre.) Avec les effets audio, la valeur de la propriété est statique et ne peut pas changer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-109">(For example, you can set a wipe transition to move back and forth across the frame.) With audio effects, the value of the property is static and cannot change over time.</span></span> <span data-ttu-id="9a9d4-110">La seule exception est l’effet d' [enveloppe de volume](volume-envelope-effect.md) , qui prend en charge une propriété dynamique pour le niveau de volume.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-110">The only exception is the [Volume Envelope](volume-envelope-effect.md) effect, which supports a dynamic property for the volume level.</span></span>

<span data-ttu-id="9a9d4-111">Pour définir une propriété, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-111">To set a property, perform the following steps.</span></span>

1.  <span data-ttu-id="9a9d4-112">Créez une instance de l’accesseur Set de propriété (CLSID \_ PropertySetter).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-112">Create an instance of the property setter (CLSID\_PropertySetter).</span></span>
2.  <span data-ttu-id="9a9d4-113">Remplissez les structures de [**\_ valeur**](dexter-value.md) [**Dexter \_**](dexter-param.md) et Dexter avec les données de propriété.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-113">Fill [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures with the property data.</span></span> <span data-ttu-id="9a9d4-114">Ces structures sont décrites ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-114">These structures are discussed below.</span></span>
3.  <span data-ttu-id="9a9d4-115">Transmettez les structures de [**\_ valeur**](dexter-value.md) [**Dexter \_**](dexter-param.md) et Dexter à la méthode [**IPropertySetter :: AddProp**](ipropertysetter-addprop.md) .</span><span class="sxs-lookup"><span data-stu-id="9a9d4-115">Pass the [**DEXTER\_PARAM**](dexter-param.md) and [**DEXTER\_VALUE**](dexter-value.md) structures to the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method.</span></span>
4.  <span data-ttu-id="9a9d4-116">Répétez les étapes 2 et 3 pour chaque propriété que vous souhaitez définir.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-116">Repeat steps 2 and 3 for each property you want to set.</span></span>
5.  <span data-ttu-id="9a9d4-117">Transmettez le pointeur d’interface [**IPropertySetter**](ipropertysetter.md) à la méthode [**IAMTimelineObj :: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="9a9d4-117">Pass the [**IPropertySetter**](ipropertysetter.md) interface pointer to the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span>

<span data-ttu-id="9a9d4-118">La structure de [**\_ paramètre Dexter**](dexter-param.md) spécifie la propriété qui est définie.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-118">The [**DEXTER\_PARAM**](dexter-param.md) structure specifies which property is being set.</span></span> <span data-ttu-id="9a9d4-119">Il contient les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-119">It contains the following members.</span></span>

-   <span data-ttu-id="9a9d4-120">**Nom**: nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a9d4-120">**Name**: Name of the property</span></span>
-   <span data-ttu-id="9a9d4-121">**DISPID**: réservé, doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="9a9d4-121">**dispID**: Reserved, must be zero</span></span>
-   <span data-ttu-id="9a9d4-122">**nvaleurs**: nombre de valeurs</span><span class="sxs-lookup"><span data-stu-id="9a9d4-122">**nValues**: Number of values</span></span>

<span data-ttu-id="9a9d4-123">La \_ structure de valeur Dexterity spécifie la valeur d’une propriété à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-123">The DEXTER\_VALUE structure specifies the value of a property at a given time.</span></span> <span data-ttu-id="9a9d4-124">Il contient les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-124">It contains the following members.</span></span>

-   <span data-ttu-id="9a9d4-125">**v**: type Variant qui spécifie une nouvelle valeur pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-125">**v**: VARIANT type that specifies a new value for the property.</span></span> <span data-ttu-id="9a9d4-126">Le membre **VT** de cette variante définit le type de données de la propriété.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-126">The **vt** member of this VARIANT defines the data type of the property.</span></span> <span data-ttu-id="9a9d4-127">Pour plus d’informations sur le type **Variant** , consultez le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-127">For more information on the **VARIANT** type, see the Windows SDK.</span></span>
-   <span data-ttu-id="9a9d4-128">**RT**: temps de référence lorsque la propriété suppose cette valeur, par rapport à l’heure de début de l’effet ou de la transition.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-128">**rt**: Reference time when the property assumes this value, relative to the starting time of the effect or transition.</span></span> <span data-ttu-id="9a9d4-129">L’heure de début de l’effet ou de la transition est relative à l’heure de début de son objet parent.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-129">The start time of the effect or transition is relative to the start time of its parent object.</span></span>
-   <span data-ttu-id="9a9d4-130">**dwInterp**: indicateur qui spécifie la façon dont la propriété passe de la valeur précédente à la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-130">**dwInterp**: Flag that specifies how the property changes from the previous value to the new value.</span></span> <span data-ttu-id="9a9d4-131">Avec l' \_ indicateur de saut DEXTERF, la propriété passe instantanément à la nouvelle valeur à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-131">With the DEXTERF\_JUMP flag, the property jumps instantly to the new value at the specified time.</span></span> <span data-ttu-id="9a9d4-132">Avec l' \_ indicateur d’interpolation DEXTERF, la propriété est interpolée de façon linéaire par rapport à la valeur précédente.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-132">With the DEXTERF\_INTERPOLATE flag, the property is interpolated linearly from the previous value.</span></span>

<span data-ttu-id="9a9d4-133">Si vous définissez le membre **VT** sur VT \_ BSTR, la méthode setter de la propriété effectue toutes les conversions nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-133">If you set the **vt** member to VT\_BSTR, the property setter makes any necessary conversions.</span></span> <span data-ttu-id="9a9d4-134">Pour les valeurs à virgule flottante, incluez le zéro non significatif avant la décimale.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-134">For floating-point values, include the leading zero before the decimal place.</span></span> <span data-ttu-id="9a9d4-135">Par exemple, 0,3, pas. 3.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-135">For example, 0.3, not .3.</span></span>

> [!Note]  
> <span data-ttu-id="9a9d4-136">Les applications doivent éviter de se reposer sur la conversion de **BSTR** en valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-136">Applications should avoid relying on the conversion from **BSTR** s to numeric values.</span></span> <span data-ttu-id="9a9d4-137">Si la propriété a une valeur numérique, utilisez le type de **variante** numérique approprié est possible.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-137">If the property has a numeric value, use the appropriate numeric **VARIANT** type is possible.</span></span>

 

<span data-ttu-id="9a9d4-138">La valeur d’une propriété pouvant changer au fil du temps, la méthode [**IPropertySetter :: AddProp**](ipropertysetter-addprop.md) prend une structure de [**\_ paramètre Dexter**](dexter-param.md) unique et un pointeur vers un tableau de structures de [**\_ valeur Dexterity**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="9a9d4-138">The value of a property can change over time, so the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method takes a single [**DEXTER\_PARAM**](dexter-param.md) structure and a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span> <span data-ttu-id="9a9d4-139">Le tableau définit un ensemble de valeurs basées sur le temps pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-139">The array defines a set of time-based values for the property.</span></span> <span data-ttu-id="9a9d4-140">Les membres du tableau doivent être dans l’ordre chronologique croissant et le membre **nvaleurs** de la \_ structure de paramètre Dexter doit être égal à la longueur du tableau.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-140">The members of the array must be in ascending time order, and the **nValues** member of the DEXTER\_PARAM structure must equal the length of the array.</span></span>

<span data-ttu-id="9a9d4-141">L’exemple de code suivant crée des données de propriété pour la transition de [réinitialisation SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="9a9d4-141">The following code example creates property data for the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span> <span data-ttu-id="9a9d4-142">Elle définit le code de réinitialisation sur 120, ce qui crée une effacement ovale.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-142">It sets the wipe code to 120, which creates an oval wipe.</span></span> <span data-ttu-id="9a9d4-143">Elle définit le temps de référence à zéro, ce qui indique le début de la transition.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-143">It sets the reference time to zero, indicating the start of the transition.</span></span>


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



<span data-ttu-id="9a9d4-144">**Modification dynamique des propriétés**</span><span class="sxs-lookup"><span data-stu-id="9a9d4-144">**Dynamically Changing Properties**</span></span>

<span data-ttu-id="9a9d4-145">Une fois que vous avez rendu un projet de montage vidéo, il est possible de modifier les propriétés d’un objet d’effet ou de transition pendant que le graphique est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-145">After you render a video editing project, it is possible to modify an effect or transition object's properties while the graph is running.</span></span> <span data-ttu-id="9a9d4-146">Toutefois, cela n’est possible que si vous définissez des propriétés sur cet objet avant l’application appelée [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="9a9d4-146">However, this is possible only if you set properties on that object before the application called [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="9a9d4-147">Dans ce cas, vous pouvez appeler [**IAMTimelineObj :: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) sur l’effet ou la transition, effacer ou modifier les propriétés, et les modifications se produisent de manière dynamique à mesure que le graphique est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-147">If so, you can call [**IAMTimelineObj::GetPropertySetter**](iamtimelineobj-getpropertysetter.md) on the effect or transition, clear or modify the properties, and the changes will happen dynamically as the graph is running.</span></span> <span data-ttu-id="9a9d4-148">Il peut y avoir des anomalies visuelles pendant que la modification se produit, ce qui est recommandé uniquement pour la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-148">There may be visual anomalies while the change occurs, so this is recommended only for preview.</span></span> <span data-ttu-id="9a9d4-149">Ne modifiez pas les propriétés lorsque vous écrivez le projet dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-149">Do not change the properties while you are writing the project to a file.</span></span>

<span data-ttu-id="9a9d4-150">Si vous n’avez pas défini de propriétés sur l’objet d’effet ou de transition avant d’appeler **ConnectFrontEnd**, vous ne pouvez pas lui ajouter de propriétés pendant que le graphique est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9a9d4-150">If you did not set any properties on the effect or transition object before you called **ConnectFrontEnd**, you cannot add properties to it while the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a9d4-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a9d4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a9d4-152">Utilisation des effets et des transitions</span><span class="sxs-lookup"><span data-stu-id="9a9d4-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 




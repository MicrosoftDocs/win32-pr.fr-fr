---
description: Source de couleur vidéo
ms.assetid: e6addd55-06ca-4d4b-b2b0-fde281fab244
title: Source de couleur vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c751d74a78b027d50f033acb3709d18fe8f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203615"
---
# <a name="video-color-source"></a><span data-ttu-id="51823-103">Source de couleur vidéo</span><span class="sxs-lookup"><span data-stu-id="51823-103">Video Color Source</span></span>

> [!Note]  
> <span data-ttu-id="51823-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="51823-104">\[Deprecated.</span></span> <span data-ttu-id="51823-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51823-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="51823-106">La source de couleur vidéo crée une image vidéo continue d’une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="51823-106">The Video Color Source creates a continuous video image of a solid color.</span></span>

<span data-ttu-id="51823-107">ID de classe (CLSID) : **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span><span class="sxs-lookup"><span data-stu-id="51823-107">Class ID (CLSID): **{0CFDD070-581A-11D2-9EE6-006008039E37}**</span></span>

<span data-ttu-id="51823-108">Nom de la variable CLSID : **CLSID \_ ColorSource**</span><span class="sxs-lookup"><span data-stu-id="51823-108">CLSID Variable Name: **CLSID\_ColorSource**</span></span>

<span data-ttu-id="51823-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="51823-109">Properties</span></span>



| <span data-ttu-id="51823-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="51823-110">Property</span></span> | <span data-ttu-id="51823-111">Type</span><span class="sxs-lookup"><span data-stu-id="51823-111">Type</span></span>      | <span data-ttu-id="51823-112">Default</span><span class="sxs-lookup"><span data-stu-id="51823-112">Default</span></span> | <span data-ttu-id="51823-113">Description</span><span class="sxs-lookup"><span data-stu-id="51823-113">Description</span></span>                                   |
|----------|-----------|---------|-----------------------------------------------|
| <span data-ttu-id="51823-114">Colorimétrique</span><span class="sxs-lookup"><span data-stu-id="51823-114">"Color"</span></span>  | <span data-ttu-id="51823-115">**GRANDE**</span><span class="sxs-lookup"><span data-stu-id="51823-115">**DWORD**</span></span> | <span data-ttu-id="51823-116">0</span><span class="sxs-lookup"><span data-stu-id="51823-116">0</span></span>       | <span data-ttu-id="51823-117">Spécifie la couleur à générer.</span><span class="sxs-lookup"><span data-stu-id="51823-117">Specifies the color to generate.</span></span> <span data-ttu-id="51823-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="51823-118">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="51823-119">Notes</span><span class="sxs-lookup"><span data-stu-id="51823-119">Remarks</span></span>

<span data-ttu-id="51823-120">La source de couleur vidéo est utilisée avec les objets sources.</span><span class="sxs-lookup"><span data-stu-id="51823-120">The Video Color Source is used with source objects.</span></span> <span data-ttu-id="51823-121">Tout d’abord, créez un nouvel objet source.</span><span class="sxs-lookup"><span data-stu-id="51823-121">First, create a new source object.</span></span> <span data-ttu-id="51823-122">Définissez ensuite le GUID de sous-objet de l’objet source sur CLSID \_ ColorSource, en appelant la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="51823-122">Then set the source object's subobject GUID to CLSID\_ColorSource, by calling the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="51823-123">Pour définir la couleur, créez un objet [accesseur Set de propriété](property-setter.md) et appliquez la propriété « Color » à l’heure zéro.</span><span class="sxs-lookup"><span data-stu-id="51823-123">To set the color, create a [Property Setter](property-setter.md) object and apply the "Color" property at time zero.</span></span> <span data-ttu-id="51823-124">La valeur de cette propriété est un nombre hexadécimal au format *0xAARRGGBB*, où *AA* correspond à la valeur alpha, *RR* à la valeur rouge, *GG* à la valeur verte et *BB* à la valeur bleue.</span><span class="sxs-lookup"><span data-stu-id="51823-124">The value of this property is a hexadecimal number with the format *0xAARRGGBB*, where *AA* is the alpha value, *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="51823-125">Les valeurs alpha sont comprises entre 0x00 (transparent) et 0xFF (opaque).</span><span class="sxs-lookup"><span data-stu-id="51823-125">Alpha values range from 0x00 (transparent) to 0xFF (opaque).</span></span> <span data-ttu-id="51823-126">La propriété est statique et doit être appliquée à l’heure zéro.</span><span class="sxs-lookup"><span data-stu-id="51823-126">The property is static and must be applied at time zero.</span></span>

<span data-ttu-id="51823-127">Si vous ne spécifiez pas la valeur alpha, la valeur par défaut est zéro (transparent).</span><span class="sxs-lookup"><span data-stu-id="51823-127">If you do not specify the alpha value, it defaults to zero (transparent).</span></span> <span data-ttu-id="51823-128">Dans un projet vidéo de couleur de 32 bits, cela entraîne des transitions ou des effets qui utilisent alpha pour rendre la source de couleur vidéo aussi transparente.</span><span class="sxs-lookup"><span data-stu-id="51823-128">In a 32-bit-color video project, this will cause transitions or effects that use alpha to render the Video Color Source as completely transparent.</span></span> <span data-ttu-id="51823-129">Pour être sécurisé, spécifiez toujours le alpha.</span><span class="sxs-lookup"><span data-stu-id="51823-129">To be safe, always specify the alpha.</span></span> <span data-ttu-id="51823-130">Par exemple, le noir opaque est **0xFF000000**.</span><span class="sxs-lookup"><span data-stu-id="51823-130">For example, opaque black is **0xFF000000**.</span></span>

<span data-ttu-id="51823-131">L’exemple de code suivant montre comment utiliser cet objet.</span><span class="sxs-lookup"><span data-stu-id="51823-131">The following code example shows how to use this object.</span></span> <span data-ttu-id="51823-132">Pour plus d’informations sur l’utilisation de [**IPropertySetter**](ipropertysetter.md), consultez [définition des propriétés des effets et des transitions](setting-properties-on-effects-and-transitions.md):</span><span class="sxs-lookup"><span data-stu-id="51823-132">For more information about using [**IPropertySetter**](ipropertysetter.md), see [Setting Properties on Effects and Transitions](setting-properties-on-effects-and-transitions.md):</span></span>


```C++
DWORD           dwYellow = 0xFFFF00;
IAMTimelineObj  *pSource = NULL;

// Create the source.
HRESULT hr = pTimeline->CreateEmptyNode(&pSource, TIMELINE_MAJOR_TYPE_SOURCE);
if (SUCCEEDED(hr))
{
    hr = pSource->SetStartStop(0, 50000000);
}

if (SUCCEEDED(hr))
{
    hr = pSource->SetSubObjectGUID(CLSID_ColorSource);
}

// Create a property setter.
if (SUCCEEDED(hr))
{
    IPropertySetter *pProp = NULL;
    
    hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pProp));

    if SUCCEEDED(hr))
    {
        // Set the color.    
        DEXTER_PARAM param;
        DEXTER_VALUE val;

        param.Name = SysAllocString(OLESTR("Color"));
        param.dispID = 0;
        param.nValues = 1;

        if (param.Name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            val.v.vt = VT_I4;
            val.v.lVal = dwYellow;
            val.rt = 0;  // Time must be zero.
            val.dwInterp = DEXTERF_JUMP;

            hr = pProp->AddProp(param, &val);
            
            SysFreeString(param.Name);
        }

        if (SUCCEEDED(hr))
        {
            hr = pSource->SetPropertySetter(pProp); 
        }
        pProp->Release();
    }
}
```



<span data-ttu-id="51823-133">L’exemple suivant illustre la représentation XML de l’objet créé dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="51823-133">The following example shows the XML representation of the object created in the previous example.</span></span> <span data-ttu-id="51823-134">Dans ce cas, l’élément [**param**](param-element.md) ne prend pas en charge les éléments [**at**](at-element.md) ou [**Linear**](linear-element.md) , car l’objet ne prend pas en charge les propriétés dynamiques :</span><span class="sxs-lookup"><span data-stu-id="51823-134">In this case the [**param**](param-element.md) element does not support [**at**](at-element.md) or [**linear**](linear-element.md) elements, because the object does not support dynamic properties:</span></span>


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 




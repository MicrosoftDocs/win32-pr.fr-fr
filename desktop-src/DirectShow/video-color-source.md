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
# <a name="video-color-source"></a>Source de couleur vidéo

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La source de couleur vidéo crée une image vidéo continue d’une couleur unie.

ID de classe (CLSID) : **{0CFDD070-581A-11D2-9EE6-006008039E37}**

Nom de la variable CLSID : **CLSID \_ ColorSource**

Propriétés



| Propriété | Type      | Default | Description                                   |
|----------|-----------|---------|-----------------------------------------------|
| Colorimétrique  | **GRANDE** | 0       | Spécifie la couleur à générer. Consultez la section Notes. |



 

## <a name="remarks"></a>Notes

La source de couleur vidéo est utilisée avec les objets sources. Tout d’abord, créez un nouvel objet source. Définissez ensuite le GUID de sous-objet de l’objet source sur CLSID \_ ColorSource, en appelant la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Pour définir la couleur, créez un objet [accesseur Set de propriété](property-setter.md) et appliquez la propriété « Color » à l’heure zéro. La valeur de cette propriété est un nombre hexadécimal au format *0xAARRGGBB*, où *AA* correspond à la valeur alpha, *RR* à la valeur rouge, *GG* à la valeur verte et *BB* à la valeur bleue. Les valeurs alpha sont comprises entre 0x00 (transparent) et 0xFF (opaque). La propriété est statique et doit être appliquée à l’heure zéro.

Si vous ne spécifiez pas la valeur alpha, la valeur par défaut est zéro (transparent). Dans un projet vidéo de couleur de 32 bits, cela entraîne des transitions ou des effets qui utilisent alpha pour rendre la source de couleur vidéo aussi transparente. Pour être sécurisé, spécifiez toujours le alpha. Par exemple, le noir opaque est **0xFF000000**.

L’exemple de code suivant montre comment utiliser cet objet. Pour plus d’informations sur l’utilisation de [**IPropertySetter**](ipropertysetter.md), consultez [définition des propriétés des effets et des transitions](setting-properties-on-effects-and-transitions.md):


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



L’exemple suivant illustre la représentation XML de l’objet créé dans l’exemple précédent. Dans ce cas, l’élément [**param**](param-element.md) ne prend pas en charge les éléments [**at**](at-element.md) ou [**Linear**](linear-element.md) , car l’objet ne prend pas en charge les propriétés dynamiques :


```C++
<clip start="0" stop="5" clsid="{0CFDD070-581A-11D2-9EE6-006008039E37}">
    <param name="Color" value="16776960"/>
</clip>
```



 

 




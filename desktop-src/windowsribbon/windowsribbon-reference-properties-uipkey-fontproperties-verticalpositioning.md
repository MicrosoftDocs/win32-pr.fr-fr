---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifie la \_ \_ propriété FontProperties VerticalPositioning de l’interface utilisateur \_ .
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031708"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="9e704-103">IU \_ \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="9e704-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="9e704-104">Identifie la \_ \_ propriété FontProperties VerticalPositioning de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="9e704-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="9e704-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9e704-105">Remarks</span></span>

<span data-ttu-id="9e704-106">L’interface utilisateur \_ \_ FontProperties \_ VerticalPositioning est utilisée par une application pour interroger la valeur des contrôles **Superscript** et **indice** .</span><span class="sxs-lookup"><span data-stu-id="9e704-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="9e704-107">La valeur de la propriété provient de l’énumération [**\_ FONTVERTICALPOSITION de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .</span><span class="sxs-lookup"><span data-stu-id="9e704-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="9e704-108">La valeur par défaut est `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="9e704-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="9e704-109">**La capture** d’écran suivante montre les boutons **exposant et indice** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="9e704-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="9e704-111">Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9e704-111">The following table describes the properties and the UI result.</span></span>



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="9e704-112">Les boutons exposant et **indice** sont désactivés **et ne** peuvent être définis que par l’application.</span><span class="sxs-lookup"><span data-stu-id="9e704-112">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="9e704-113">**Les boutons exposant et** **indice** ne sont pas sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9e704-113">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="9e704-114">Le bouton **exposant** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9e704-114">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="9e704-115">Le bouton d' **indice** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9e704-115">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="9e704-116">Les  boutons exposant et **indice** ne peuvent pas être sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9e704-116">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9e704-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e704-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e704-118">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="9e704-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="9e704-119">**interface utilisateur \_ FONTVERTICALPOSITION**</span><span class="sxs-lookup"><span data-stu-id="9e704-119">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="9e704-120">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="9e704-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 
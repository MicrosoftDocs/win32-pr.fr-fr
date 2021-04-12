---
title: UI_PKEY_ColorType
description: Identifie la propriété de la propriété de la propriété de l’interface utilisateur \_ \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315701"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="67fbd-103">Interface utilisateur de l’IU \_ \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="67fbd-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="67fbd-104">Identifie la propriété de la propriété de la propriété de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="67fbd-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="67fbd-105">Notes</span><span class="sxs-lookup"><span data-stu-id="67fbd-105">Remarks</span></span>

<span data-ttu-id="67fbd-106">L’interface utilisateur de l’IU \_ \_ ColorType est utilisée par une application pour interroger le paramètre de couleur du contrôle [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="67fbd-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="67fbd-107">La valeur de la propriété provient de l’énumération [**\_ SWATCHCOLORTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="67fbd-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67fbd-108">nocolor SWATCHCOLORTYPE de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="67fbd-108">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="67fbd-109">L’application doit traiter le paramètre de couleur comme étant transparent.</span><span class="sxs-lookup"><span data-stu-id="67fbd-109">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="67fbd-110">Généralement utilisé conjointement avec le paramètre de couleur **sans** couleur.</span><span class="sxs-lookup"><span data-stu-id="67fbd-110">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="67fbd-111">\_SWATCHCOLORTYPE \_ automatique de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="67fbd-111">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="67fbd-112">L’application doit interroger [GetSysColor (couleur \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="67fbd-112">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="67fbd-113">Généralement utilisé conjointement avec le paramètre de couleur **automatique** .</span><span class="sxs-lookup"><span data-stu-id="67fbd-113">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="67fbd-114">interface utilisateur \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="67fbd-114">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="67fbd-115">L’application doit interroger la [ \_ \_ couleur](windowsribbon-reference-properties-uipkey-color.md) de la couleur de l’interface utilisateur pour le paramètre de couleur.</span><span class="sxs-lookup"><span data-stu-id="67fbd-115">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="67fbd-116">L’interface utilisateur de l’IU \_ \_ ColorType est transmise à la méthode de rappel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) lorsqu’un échantillon de couleur est sélectionné dans un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="67fbd-116">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67fbd-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67fbd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67fbd-118">Propriétés du sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="67fbd-118">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 
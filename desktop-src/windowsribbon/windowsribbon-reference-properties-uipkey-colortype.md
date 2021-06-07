---
title: UI_PKEY_ColorType
description: Identifie la propriété de la propriété de la propriété de l’interface utilisateur \_ \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443890"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="29d82-103">Interface utilisateur de l’IU \_ \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="29d82-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="29d82-104">Identifie la propriété de la propriété de la propriété de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="29d82-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="29d82-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="29d82-105">Remarks</span></span>

<span data-ttu-id="29d82-106">L’interface utilisateur de l’IU \_ \_ ColorType est utilisée par une application pour interroger le paramètre de couleur du contrôle [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="29d82-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="29d82-107">La valeur de la propriété provient de l’énumération [**\_ SWATCHCOLORTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="29d82-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|    <span data-ttu-id="29d82-108">Propriété</span><span class="sxs-lookup"><span data-stu-id="29d82-108">Property</span></span>                            |    <span data-ttu-id="29d82-109">Description</span><span class="sxs-lookup"><span data-stu-id="29d82-109">Description</span></span>                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29d82-110">nocolor SWATCHCOLORTYPE de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="29d82-110">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="29d82-111">L’application doit traiter le paramètre de couleur comme étant transparent.</span><span class="sxs-lookup"><span data-stu-id="29d82-111">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="29d82-112">Généralement utilisé conjointement avec le paramètre de couleur **sans** couleur.</span><span class="sxs-lookup"><span data-stu-id="29d82-112">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="29d82-113">\_SWATCHCOLORTYPE \_ automatique de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="29d82-113">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="29d82-114">L’application doit interroger [GetSysColor (couleur \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span><span class="sxs-lookup"><span data-stu-id="29d82-114">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="29d82-115">Généralement utilisé conjointement avec le paramètre de couleur **automatique** .</span><span class="sxs-lookup"><span data-stu-id="29d82-115">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="29d82-116">interface utilisateur \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="29d82-116">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="29d82-117">L’application doit interroger la [ \_ \_ couleur](windowsribbon-reference-properties-uipkey-color.md) de la couleur de l’interface utilisateur pour le paramètre de couleur.</span><span class="sxs-lookup"><span data-stu-id="29d82-117">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="29d82-118">L’interface utilisateur de l’IU \_ \_ ColorType est transmise à la méthode de rappel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) lorsqu’un échantillon de couleur est sélectionné dans un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="29d82-118">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29d82-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29d82-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29d82-120">Propriétés du sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="29d82-120">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 
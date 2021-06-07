---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifie la \_ \_ propriété FontProperties BackgroundColorType de l’interface utilisateur \_ .
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443820"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="88479-103">IU \_ \_ FontProperties \_ BackgroundColorType</span><span class="sxs-lookup"><span data-stu-id="88479-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="88479-104">Identifie la \_ \_ propriété FontProperties BackgroundColorType de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="88479-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="88479-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="88479-105">Remarks</span></span>

<span data-ttu-id="88479-106">L’interface utilisateur \_ \_ FontProperties \_ BackgroundColorType est utilisée par une application, conjointement avec [l’interface utilisateur de l’IU \_ \_ FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), pour interroger les paramètres de la Galerie de **couleurs de surbrillance du texte** .</span><span class="sxs-lookup"><span data-stu-id="88479-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="88479-107">La valeur de la propriété provient de l’énumération [**\_ SWATCHCOLORTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="88479-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="88479-108">La valeur par défaut est `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="88479-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="88479-109">Le tableau suivant décrit les valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="88479-109">The following table describes the property values.</span></span>



|   <span data-ttu-id="88479-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="88479-110">Property</span></span>                             |   <span data-ttu-id="88479-111">Description</span><span class="sxs-lookup"><span data-stu-id="88479-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="88479-112">L’application doit interroger la mesure système appropriée pour la valeur de couleur en général la **couleur d’arrière-plan** de la fenêtre de thème Windows actuelle qui est récupérée avec GetSysColor (fenêtre de couleur \_ ).</span><span class="sxs-lookup"><span data-stu-id="88479-112">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="88479-113">Non pris en charge par [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="88479-113">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="88479-114">L’application doit interroger l' [interface utilisateur \_ \_ FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) pour obtenir la valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="88479-114">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="88479-115">La valeur de couleur de l' [interface utilisateur \_ \_ FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) est affichée dans le bouton **couleur de surbrillance du texte** et sélectionnée dans la Galerie de **couleurs de mise en surbrillance du texte** .</span><span class="sxs-lookup"><span data-stu-id="88479-115">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="88479-116">L’interface utilisateur \_ \_ FontProperties \_ BackgroundColorType est transmise à la méthode de rappel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) lorsqu’un échantillon de couleur est sélectionné dans la Galerie de **couleurs de surbrillance du texte** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="88479-116">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="88479-117">Il est fortement recommandé que l’application ne définisse qu’une valeur de **couleur de mise en surbrillance du texte** initiale et ne réaffecte pas cette valeur lorsque le curseur est repositionné dans un document.</span><span class="sxs-lookup"><span data-stu-id="88479-117">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="88479-118">La dernière sélection doit être conservée pour éviter de devoir resélectionner la couleur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="88479-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="88479-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88479-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88479-120">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="88479-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="88479-121">**interface utilisateur \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="88479-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="88479-122">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="88479-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 


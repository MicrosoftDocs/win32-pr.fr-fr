---
title: UI_PKEY_FontProperties_Family
description: Identifie la propriété de la famille FontProperties de l’interface utilisateur \_ \_ \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509262"
---
# <a name="ui_pkey_fontproperties_family"></a><span data-ttu-id="9b628-103">\_Famille de \_ FontProperties de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="9b628-103">UI\_PKEY\_FontProperties\_Family</span></span>

<span data-ttu-id="9b628-104">Identifie la propriété de la famille FontProperties de l’interface utilisateur \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9b628-104">Identifies the UI\_PKEY\_FontProperties\_Family property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="9b628-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9b628-105">Remarks</span></span>

<span data-ttu-id="9b628-106">L’interface utilisateur \_ \_ FontProperties \_ Family est utilisée par une application pour interroger la valeur de la Galerie de listes déroulantes de la **famille de polices** .</span><span class="sxs-lookup"><span data-stu-id="9b628-106">UI\_PKEY\_FontProperties\_Family is used by an application to query the value of the **Font family** drop-down gallery.</span></span>

<span data-ttu-id="9b628-107">La valeur de la famille FontProperties de l’interface utilisateur est \_ \_ identique à celle d' \_ un nom de famille de [polices Windows GDI](../gdi/font-families.md) récupéré avec la [fonction EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) ou la [fonction EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span><span class="sxs-lookup"><span data-stu-id="9b628-107">The value of UI\_PKEY\_FontProperties\_Family matches a [Windows GDI Font Families](../gdi/font-families.md) name retrieved with the [EnumFontFamilies function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) or [EnumFontFamiliesEx function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span></span>

<span data-ttu-id="9b628-108">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="9b628-108">The default value is an empty string.</span></span>

<span data-ttu-id="9b628-109">Si une chaîne vide est fournie pour la valeur de la famille FontProperties de l’interface utilisateur \_ \_ \_ , la sélection de la police est désactivée.</span><span class="sxs-lookup"><span data-stu-id="9b628-109">If an empty string is supplied for the value for UI\_PKEY\_FontProperties\_Family, then the font selection is cleared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b628-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b628-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b628-111">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="9b628-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="9b628-112">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="9b628-112">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 
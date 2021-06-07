---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifie la propriété de l’interface utilisateur FontProperties de l’interface utilisateur \_ \_ \_ .
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444390"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="e950e-103">FontProperties de l’IU \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e950e-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="e950e-104">Identifie la propriété de l’interface utilisateur FontProperties de l’interface utilisateur \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e950e-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="e950e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e950e-105">Remarks</span></span>

<span data-ttu-id="e950e-106">L’interface utilisateur \_ \_ FontProperties la valeur de l’option de type de variable \_ est utilisée par une application dans les cas où il n’est pas possible pour l’application de spécifier une valeur pour la **taille de police**, par exemple lorsqu’une série de texte de taille hétérogène est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e950e-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="e950e-107">Le contrôle de **taille de police** est défini sur vide et l’interface utilisateur FontProperties de l’interface utilisateur \_ \_ \_ est utilisée pour capturer l’interaction de l’utilisateur avec les boutons **agrandir la police** et **réduire la police** .</span><span class="sxs-lookup"><span data-stu-id="e950e-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="e950e-108">L’interface utilisateur de la FontProperties de l’interface utilisateur \_ \_ \_ est incluse dans [l’IU \_ \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="e950e-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="e950e-109">La capture d’écran suivante montre les boutons **agrandir la police** et **réduire la police** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="e950e-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![capture d’écran des boutons agrandir la police et réduire la police sur le fontcontrol.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="e950e-111">Le tableau suivant décrit les valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e950e-111">The following table describes the property values.</span></span>



|     <span data-ttu-id="e950e-112">Value</span><span class="sxs-lookup"><span data-stu-id="e950e-112">Value</span></span>                 |  <span data-ttu-id="e950e-113">Description</span><span class="sxs-lookup"><span data-stu-id="e950e-113">Description</span></span>                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="e950e-114">L’utilisateur a cliqué sur le bouton **agrandir la police** .</span><span class="sxs-lookup"><span data-stu-id="e950e-114">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="e950e-115">Clic sur le bouton **réduire la police** .</span><span class="sxs-lookup"><span data-stu-id="e950e-115">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e950e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e950e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e950e-117">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="e950e-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="e950e-118">**interface utilisateur \_ FONTDELTASIZE**</span><span class="sxs-lookup"><span data-stu-id="e950e-118">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="e950e-119">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="e950e-119">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 
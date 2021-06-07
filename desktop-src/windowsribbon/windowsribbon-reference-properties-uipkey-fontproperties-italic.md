---
title: UI_PKEY_FontProperties_Italic
description: Identifie la \_ \_ propriété FontProperties italique de l’interface utilisateur \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443810"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="fc764-103">IU \_ \_ FontProperties \_ italique</span><span class="sxs-lookup"><span data-stu-id="fc764-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="fc764-104">Identifie la \_ \_ propriété FontProperties italique de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="fc764-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="fc764-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc764-105">Remarks</span></span>

<span data-ttu-id="fc764-106">IU \_ \_ FontProperties \_ italique est utilisé par une application pour interroger l’état du bouton **italique** .</span><span class="sxs-lookup"><span data-stu-id="fc764-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="fc764-107">La valeur de la propriété provient de l’énumération [**\_ FONTPROPERTIES de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="fc764-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="fc764-108">La valeur par défaut est `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="fc764-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="fc764-109">Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fc764-109">The following table describes the properties and the UI result.</span></span>



|    <span data-ttu-id="fc764-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="fc764-110">Property</span></span>                      |       <span data-ttu-id="fc764-111">Résultat de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="fc764-111">UI Result</span></span>                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="fc764-112">Le bouton **italique** est désactivé et ne peut être défini que par l’application.</span><span class="sxs-lookup"><span data-stu-id="fc764-112">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="fc764-113">Le bouton **italique** n’est pas sélectionné.</span><span class="sxs-lookup"><span data-stu-id="fc764-113">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="fc764-114">Le bouton **italique** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="fc764-114">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="fc764-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc764-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc764-116">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="fc764-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="fc764-117">**interface utilisateur \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="fc764-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="fc764-118">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="fc764-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 
---
description: Une application peut récupérer des métriques de police pour une police physique uniquement après que la police a été sélectionnée dans un contexte de périphérique.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Unité et unités de conception
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863661"
---
# <a name="device-vs-design-units"></a><span data-ttu-id="cab8c-103">Unité et unités de conception</span><span class="sxs-lookup"><span data-stu-id="cab8c-103">Device vs. Design Units</span></span>

<span data-ttu-id="cab8c-104">Une application peut récupérer des métriques de police pour une police physique uniquement après que la police a été sélectionnée dans un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cab8c-104">An application can retrieve font metrics for a physical font only after the font has been selected into a device context.</span></span> <span data-ttu-id="cab8c-105">Lorsqu’une police est sélectionnée dans un contexte de périphérique, elle est mise à l’échelle pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cab8c-105">When a font is selected into a device context, it is scaled for the device.</span></span> <span data-ttu-id="cab8c-106">Les métriques de police spécifiques à l’appareil sont appelées unités de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cab8c-106">The font metrics specific to the device are known as device units.</span></span>

<span data-ttu-id="cab8c-107">Les métriques portables dans les polices sont appelées unités de conception.</span><span class="sxs-lookup"><span data-stu-id="cab8c-107">Portable metrics in fonts are known as design units.</span></span> <span data-ttu-id="cab8c-108">Pour appliquer à un appareil spécifié, les unités de conception doivent être converties en unités de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cab8c-108">To apply to a specified device, design units must be converted to device units.</span></span> <span data-ttu-id="cab8c-109">Utilisez la formule suivante pour convertir les unités de conception en unités de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cab8c-109">Use the following formula to convert design units to device units.</span></span>

<span data-ttu-id="cab8c-110">*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*pointer*/72) \* *DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="cab8c-110">*DeviceUnits* = (*DesignUnits*/*unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*</span></span>

<span data-ttu-id="cab8c-111">Les variables de cette formule ont les significations suivantes.</span><span class="sxs-lookup"><span data-stu-id="cab8c-111">The variables in this formula have the following meanings.</span></span>



| <span data-ttu-id="cab8c-112">Variable</span><span class="sxs-lookup"><span data-stu-id="cab8c-112">Variable</span></span>           | <span data-ttu-id="cab8c-113">Description</span><span class="sxs-lookup"><span data-stu-id="cab8c-113">Description</span></span>                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab8c-114">*DeviceUnits*</span><span class="sxs-lookup"><span data-stu-id="cab8c-114">*DeviceUnits*</span></span>      | <span data-ttu-id="cab8c-115">Spécifie la métrique de police *DesignUnits* convertie en unités de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cab8c-115">Specifies the *DesignUnits* font metric converted to device units.</span></span> <span data-ttu-id="cab8c-116">Cette valeur est dans les mêmes unités que la valeur spécifiée pour *DeviceResolution*.</span><span class="sxs-lookup"><span data-stu-id="cab8c-116">This value is in the same units as the value specified for *DeviceResolution*.</span></span>                          |
| <span data-ttu-id="cab8c-117">*DesignUnits*</span><span class="sxs-lookup"><span data-stu-id="cab8c-117">*DesignUnits*</span></span>      | <span data-ttu-id="cab8c-118">Spécifie la métrique de police à convertir en unités de périphérique.</span><span class="sxs-lookup"><span data-stu-id="cab8c-118">Specifies the font metric to be converted to device units.</span></span> <span data-ttu-id="cab8c-119">Cette valeur peut être n’importe quelle mesure de police, y compris la largeur d’un caractère ou la valeur de l’ascendeur pour une police entière.</span><span class="sxs-lookup"><span data-stu-id="cab8c-119">This value can be any font metric, including the width of a character or the ascender value for an entire font.</span></span> |
| <span data-ttu-id="cab8c-120">*unitsPerEm*</span><span class="sxs-lookup"><span data-stu-id="cab8c-120">*unitsPerEm*</span></span>       | <span data-ttu-id="cab8c-121">Spécifie la taille du carré em de la police.</span><span class="sxs-lookup"><span data-stu-id="cab8c-121">Specifies the em square size for the font.</span></span>                                                                                                                                 |
| <span data-ttu-id="cab8c-122">*PointSize*</span><span class="sxs-lookup"><span data-stu-id="cab8c-122">*PointSize*</span></span>        | <span data-ttu-id="cab8c-123">Spécifie la taille de la police, en points.</span><span class="sxs-lookup"><span data-stu-id="cab8c-123">Specifies size of the font, in points.</span></span> <span data-ttu-id="cab8c-124">(Un point est égal à 1/72 de pouce.)</span><span class="sxs-lookup"><span data-stu-id="cab8c-124">(One point equals 1/72 of an inch.)</span></span>                                                                                                 |
| <span data-ttu-id="cab8c-125">*DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="cab8c-125">*DeviceResolution*</span></span> | <span data-ttu-id="cab8c-126">Spécifie le nombre d’unités de l’appareil (en pixels) par pouce.</span><span class="sxs-lookup"><span data-stu-id="cab8c-126">Specifies number of device units (pixels) per inch.</span></span> <span data-ttu-id="cab8c-127">Les valeurs standard peuvent être 300 pour une imprimante laser ou 96 pour un écran VGA.</span><span class="sxs-lookup"><span data-stu-id="cab8c-127">Typical values might be 300 for a laser printer or 96 for a VGA screen.</span></span>                                                |



 

<span data-ttu-id="cab8c-128">Cette formule ne doit pas être utilisée pour reconvertir les unités de périphérique en unités de conception.</span><span class="sxs-lookup"><span data-stu-id="cab8c-128">This formula should not be used to convert device units back to design units.</span></span> <span data-ttu-id="cab8c-129">Les unités de périphérique sont toujours arrondies au pixel le plus proche.</span><span class="sxs-lookup"><span data-stu-id="cab8c-129">Device units are always rounded to the nearest pixel.</span></span> <span data-ttu-id="cab8c-130">L’erreur d’arrondi propagée peut devenir très importante, en particulier lorsqu’une application utilise des tailles d’écran.</span><span class="sxs-lookup"><span data-stu-id="cab8c-130">The propagated round-off error can become very large, especially when an application is working with screen sizes.</span></span>

<span data-ttu-id="cab8c-131">Pour demander des unités de conception, créez une police logique dont la hauteur est spécifiée en tant que *unitsPerEm*.</span><span class="sxs-lookup"><span data-stu-id="cab8c-131">To request design units, create a logical font whose height is specified as *unitsPerEm*.</span></span> <span data-ttu-id="cab8c-132">Les applications peuvent récupérer la valeur de *unitsPerEm* en appelant la fonction [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) et en vérifiant le membre **ntmSizeEM** de la structure [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="cab8c-132">Applications can retrieve the value for *unitsPerEm* by calling the [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function and checking the **ntmSizeEM** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span>

 

 




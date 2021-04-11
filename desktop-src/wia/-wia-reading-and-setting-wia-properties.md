---
description: L’interface IWiaPropertyStorage fournit des méthodes pour lire et écrire les propriétés d’un élément WIA (Windows Image Acquisition). Les propriétés d’élément incluent les commandes d’appareil, les informations de format d’élément et les informations de périphérique.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lecture et définition des propriétés WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113286"
---
# <a name="reading-and-setting-wia-properties"></a><span data-ttu-id="b78c7-104">Lecture et définition des propriétés WIA</span><span class="sxs-lookup"><span data-stu-id="b78c7-104">Reading and Setting WIA Properties</span></span>

<span data-ttu-id="b78c7-105">L’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fournit des méthodes pour lire et écrire les propriétés d’un élément WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="b78c7-105">The [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface provides methods for reading and writing a Windows Image Acquisition (WIA) item's properties.</span></span> <span data-ttu-id="b78c7-106">Les propriétés d’élément incluent les commandes d’appareil, les informations de format d’élément et les informations de périphérique.</span><span class="sxs-lookup"><span data-stu-id="b78c7-106">Item properties include device commands, item format information, and device information.</span></span>

<span data-ttu-id="b78c7-107">Une application peut obtenir un pointeur vers une interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) d’un élément en énumérant les informations d’appareil ou les informations d’événement de l’élément en appelant [**IWiaItem :: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) ou [**IWiaItem :: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ou en interrogeant l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b78c7-107">An application can obtain a pointer to an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of an item either by enumerating the item's device information or event information by calling [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) or [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) or by querying the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of the item.</span></span> <span data-ttu-id="b78c7-108">(Dans WIA 2,0, faites-le en appelant [**IWiaItem2 :: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) ou [**IWiaItem2 :: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) ou en interrogeant l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément.)</span><span class="sxs-lookup"><span data-stu-id="b78c7-108">(In WIA 2.0, do this by calling [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) or by querying the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item.)</span></span>

<span data-ttu-id="b78c7-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) hérite de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) et les méthodes héritées sont implémentées comme décrit dans la section de référence de stockage structuré dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="b78c7-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) inherits from [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) and the inherited methods are implemented as described in the reference section of Structured Storage in the Windows Software Development Kit (SDK).</span></span>

> [!Note]
>
> <span data-ttu-id="b78c7-110">Les applications WIA doivent toujours lire les en-têtes de données image pour obtenir des informations d’image précises.</span><span class="sxs-lookup"><span data-stu-id="b78c7-110">WIA applications should always read image data headers for accurate image information.</span></span> <span data-ttu-id="b78c7-111">Le pilote WIA peut modifier les propriétés WIA et les en-têtes de données d’image pendant le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="b78c7-111">The WIA driver can alter the WIA properties and image data headers during data transfer.</span></span>
>
> <span data-ttu-id="b78c7-112">Si aucun en-tête de données image n’est fourni avec le format spécifié, l’application WIA doit utiliser les propriétés WIA comme source d’informations sur le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="b78c7-112">If there is no image data header supplied with the specified format, the WIA application should use the WIA properties as an information source about the data transfer.</span></span> <span data-ttu-id="b78c7-113">L’application WIA doit relire les propriétés WIA nécessaires une fois l’analyse ou la capture terminée pour obtenir les paramètres mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b78c7-113">The WIA application should reread the needed WIA properties after the scan or capture completes to get the updated settings.</span></span>

 

<span data-ttu-id="b78c7-114">Les sections suivantes décrivent les différentes propriétés WIA :</span><span class="sxs-lookup"><span data-stu-id="b78c7-114">The following sections describe the various WIA properties:</span></span>

-   [<span data-ttu-id="b78c7-115">Validation de la propriété WIA</span><span class="sxs-lookup"><span data-stu-id="b78c7-115">WIA Property Validation</span></span>](-wia-wia-property-validation.md)
-   [<span data-ttu-id="b78c7-116">Propriétés des informations sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="b78c7-116">Device Information Properties</span></span>](-wia-device-information-properties-wia-dip-xxxx.md)
-   [<span data-ttu-id="b78c7-117">Propriétés de l’appareil</span><span class="sxs-lookup"><span data-stu-id="b78c7-117">Device Properties</span></span>](-wia-device-properties.md)
-   [<span data-ttu-id="b78c7-118">Propriétés d'élément</span><span class="sxs-lookup"><span data-stu-id="b78c7-118">Item Properties</span></span>](-wia-item-properties.md)
-   [<span data-ttu-id="b78c7-119">Propriétés WIA supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b78c7-119">Additional WIA Properties</span></span>](-wia-additional-wia-properties.md)
-   [<span data-ttu-id="b78c7-120">Définition des propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="b78c7-120">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
-   [<span data-ttu-id="b78c7-121">Utilisation de propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="b78c7-121">Using Custom Properties</span></span>](-wia-using-custom-properties.md)
-   [<span data-ttu-id="b78c7-122">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="b78c7-122">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)

 

 

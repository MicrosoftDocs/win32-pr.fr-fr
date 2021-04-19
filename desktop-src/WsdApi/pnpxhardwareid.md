---
description: Spécifie l’identificateur matériel PnP-X du service.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Élément PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517779"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="56afa-103">Élément PnPXHardwareId</span><span class="sxs-lookup"><span data-stu-id="56afa-103">PnPXHardwareId element</span></span>

<span data-ttu-id="56afa-104">Spécifie l’identificateur matériel PnP-X du service.</span><span class="sxs-lookup"><span data-stu-id="56afa-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="56afa-105">PnP correspond à cet élément avec la ou les descriptions matérielles fournies dans \[ la \] section PnpxDevice du fichier INF de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="56afa-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="56afa-106">En fonction de ces informations, le service PnP sélectionne et charge le pilote de périphérique le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="56afa-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="56afa-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="56afa-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="56afa-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="56afa-108">Attributes</span></span>

<span data-ttu-id="56afa-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="56afa-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="56afa-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="56afa-110">Child elements</span></span>

<span data-ttu-id="56afa-111">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="56afa-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="56afa-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="56afa-112">Parent elements</span></span>



| <span data-ttu-id="56afa-113">Élément</span><span class="sxs-lookup"><span data-stu-id="56afa-113">Element</span></span>                             | <span data-ttu-id="56afa-114">Description</span><span class="sxs-lookup"><span data-stu-id="56afa-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="56afa-115">**Hébergement**</span><span class="sxs-lookup"><span data-stu-id="56afa-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="56afa-116">Définit des éléments pour les services définis par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="56afa-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="56afa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="56afa-117">Remarks</span></span>

<span data-ttu-id="56afa-118">Pour spécifier plusieurs ID de matériel, séparez les identificateurs par un espace, par exemple, « PnPX \_ SampleService \_ HWID \_ 1 PnPX SampleService HWID \_ \_ \_ 2 PnPX SampleService1 \_ \_ HWID \_ 3 ».</span><span class="sxs-lookup"><span data-stu-id="56afa-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="56afa-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="56afa-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="56afa-120">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56afa-120">Minimum supported system</span></span><br/> | <span data-ttu-id="56afa-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56afa-121">Windows Vista</span></span> |
| <span data-ttu-id="56afa-122">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="56afa-122">Can be empty</span></span>                        | <span data-ttu-id="56afa-123">Oui</span><span class="sxs-lookup"><span data-stu-id="56afa-123">Yes</span></span>           |



 

 





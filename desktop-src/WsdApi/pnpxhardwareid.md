---
description: Spécifie l’identificateur matériel PnP-X du service.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Élément PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996526"
---
# <a name="pnpxhardwareid-element"></a><span data-ttu-id="04fe8-103">Élément PnPXHardwareId</span><span class="sxs-lookup"><span data-stu-id="04fe8-103">PnPXHardwareId element</span></span>

<span data-ttu-id="04fe8-104">Spécifie l’identificateur matériel PnP-X du service.</span><span class="sxs-lookup"><span data-stu-id="04fe8-104">Specifies the PnP-X Hardware Identifier of the service.</span></span> <span data-ttu-id="04fe8-105">PnP correspond à cet élément avec la ou les descriptions matérielles fournies dans \[ la \] section PnpxDevice du fichier INF de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="04fe8-105">PnP matches this element with the hardware description(s) provided in the \[PnpxDevice\] section of the device's INF file.</span></span> <span data-ttu-id="04fe8-106">En fonction de ces informations, le service PnP sélectionne et charge le pilote de périphérique le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="04fe8-106">Based on this information, the PnP service selects and loads the most appropriate device driver.</span></span>

## <a name="usage"></a><span data-ttu-id="04fe8-107">Usage</span><span class="sxs-lookup"><span data-stu-id="04fe8-107">Usage</span></span>

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a><span data-ttu-id="04fe8-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="04fe8-108">Attributes</span></span>

<span data-ttu-id="04fe8-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="04fe8-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="04fe8-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="04fe8-110">Child elements</span></span>

<span data-ttu-id="04fe8-111">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="04fe8-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="04fe8-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="04fe8-112">Parent elements</span></span>



| <span data-ttu-id="04fe8-113">Élément</span><span class="sxs-lookup"><span data-stu-id="04fe8-113">Element</span></span>                             | <span data-ttu-id="04fe8-114">Description</span><span class="sxs-lookup"><span data-stu-id="04fe8-114">Description</span></span>                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="04fe8-115">**Hébergement**</span><span class="sxs-lookup"><span data-stu-id="04fe8-115">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="04fe8-116">Définit des éléments pour les services définis par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="04fe8-116">Defines elements for the services defined by the service host.</span></span> <br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="04fe8-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="04fe8-117">Remarks</span></span>

<span data-ttu-id="04fe8-118">Pour spécifier plusieurs ID de matériel, séparez les identificateurs par un espace, par exemple, « PnPX \_ SampleService \_ HWID \_ 1 PnPX SampleService HWID \_ \_ \_ 2 PnPX SampleService1 \_ \_ HWID \_ 3 ».</span><span class="sxs-lookup"><span data-stu-id="04fe8-118">To specify more than one hardware ID, separate the identifiers with a space character, for example, "PnPX\_SampleService\_HWID\_1 PnPX\_SampleService\_HWID\_2 PnPX\_SampleService1\_HWID\_3".</span></span>

## <a name="element-information"></a><span data-ttu-id="04fe8-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="04fe8-119">Element information</span></span>



| <span data-ttu-id="04fe8-120">Étiquette</span><span class="sxs-lookup"><span data-stu-id="04fe8-120">Label</span></span> | <span data-ttu-id="04fe8-121">Value</span><span class="sxs-lookup"><span data-stu-id="04fe8-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="04fe8-122">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04fe8-122">Minimum supported system</span></span><br/> | <span data-ttu-id="04fe8-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04fe8-123">Windows Vista</span></span> |
| <span data-ttu-id="04fe8-124">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="04fe8-124">Can be empty</span></span>                        | <span data-ttu-id="04fe8-125">Oui</span><span class="sxs-lookup"><span data-stu-id="04fe8-125">Yes</span></span>           |



 

 





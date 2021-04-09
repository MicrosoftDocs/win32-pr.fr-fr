---
description: Se produit lors de la génération d’un nouveau rapport d’adresse postale.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Événement NewCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868890"
---
# <a name="newcivicaddressreport-event"></a><span data-ttu-id="97bd0-103">Événement NewCivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="97bd0-103">NewCivicAddressReport event</span></span>

<span data-ttu-id="97bd0-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="97bd0-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97bd0-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="97bd0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="97bd0-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="97bd0-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="97bd0-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="97bd0-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="97bd0-108">Se produit lors de la génération d’un nouveau rapport d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="97bd0-108">Occurs when a new civic address report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="97bd0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97bd0-109">Syntax</span></span>


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="97bd0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97bd0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97bd0-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="97bd0-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="97bd0-112">Nouvel objet [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) .</span><span class="sxs-lookup"><span data-stu-id="97bd0-112">The new [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97bd0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97bd0-113">Return value</span></span>

<span data-ttu-id="97bd0-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="97bd0-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="97bd0-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="97bd0-115">Examples</span></span>

<span data-ttu-id="97bd0-116">Pour obtenir un exemple d’utilisation de cet événement, consultez [écoute des événements de rapport d’adresse postale](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="97bd0-116">For an example of how to use this event, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="97bd0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97bd0-117">Requirements</span></span>



| <span data-ttu-id="97bd0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97bd0-118">Requirement</span></span> | <span data-ttu-id="97bd0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="97bd0-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="97bd0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97bd0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97bd0-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97bd0-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97bd0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97bd0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97bd0-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97bd0-123">None supported</span></span><br/>                  |



 


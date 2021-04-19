---
description: Le ITStreamQualityControl expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité du flux.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interface ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530327"
---
# <a name="itstreamqualitycontrol-interface"></a><span data-ttu-id="2d65c-103">Interface ITStreamQualityControl</span><span class="sxs-lookup"><span data-stu-id="2d65c-103">ITStreamQualityControl interface</span></span>

<span data-ttu-id="2d65c-104">\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2d65c-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2d65c-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2d65c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2d65c-106">Le **ITStreamQualityControl** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité du flux.</span><span class="sxs-lookup"><span data-stu-id="2d65c-106">The **ITStreamQualityControl** exposes methods that allow an application to get and set parameters for stream quality control.</span></span>

<span data-ttu-id="2d65c-107">Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="2d65c-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="2d65c-108">Elle est exposée uniquement lorsqu’un appel utilise ces fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="2d65c-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="2d65c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2d65c-109">Members</span></span>

<span data-ttu-id="2d65c-110">L’interface **ITStreamQualityControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2d65c-110">The **ITStreamQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2d65c-111">**ITStreamQualityControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2d65c-111">**ITStreamQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="2d65c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d65c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d65c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d65c-113">Methods</span></span>

<span data-ttu-id="2d65c-114">L’interface **ITStreamQualityControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2d65c-114">The **ITStreamQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="2d65c-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="2d65c-115">Method</span></span>                                              | <span data-ttu-id="2d65c-116">Description</span><span class="sxs-lookup"><span data-stu-id="2d65c-116">Description</span></span>                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d65c-117">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="2d65c-117">**Get**</span></span>](itstreamqualitycontrol-get.md)           | <span data-ttu-id="2d65c-118">Obtient la valeur d’une [propriété de qualité de flux](streamqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="2d65c-118">Gets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="2d65c-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="2d65c-119">**GetRange**</span></span>](itstreamqualitycontrol-getrange.md) | <span data-ttu-id="2d65c-120">Obtient la plage de valeurs valides pour une [propriété de qualité de flux](streamqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="2d65c-120">Gets the range of valid values for a given [stream quality property](streamqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="2d65c-121">**Définissez**</span><span class="sxs-lookup"><span data-stu-id="2d65c-121">**Set**</span></span>](itstreamqualitycontrol-set.md)           | <span data-ttu-id="2d65c-122">Définit la valeur d’une [propriété de qualité de flux](streamqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="2d65c-122">Sets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2d65c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d65c-123">Requirements</span></span>



| <span data-ttu-id="2d65c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d65c-124">Requirement</span></span> | <span data-ttu-id="2d65c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d65c-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2d65c-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2d65c-126">TAPI version</span></span><br/> | <span data-ttu-id="2d65c-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="2d65c-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="2d65c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d65c-128">Header</span></span><br/>       | <dl> <span data-ttu-id="2d65c-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d65c-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d65c-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d65c-130">Library</span></span><br/>      | <dl> <span data-ttu-id="2d65c-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d65c-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="2d65c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2d65c-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="2d65c-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d65c-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 


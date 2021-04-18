---
description: L’interface ITFormatControl expose des méthodes qui permettent à une application de récupérer des informations concernant le format d’un flux de réception ou de transmission pour un appel.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interface ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526633"
---
# <a name="itformatcontrol-interface"></a><span data-ttu-id="8e54d-103">Interface ITFormatControl</span><span class="sxs-lookup"><span data-stu-id="8e54d-103">ITFormatControl interface</span></span>

<span data-ttu-id="8e54d-104">\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8e54d-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e54d-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8e54d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8e54d-106">L’interface **ITFormatControl** expose des méthodes qui permettent à une application de récupérer des informations concernant le format d’un flux de réception ou de transmission pour un appel.</span><span class="sxs-lookup"><span data-stu-id="8e54d-106">The **ITFormatControl** interface exposes methods that allow an application to retrieve information concerning the format of a receive or transmit stream for a call.</span></span>

<span data-ttu-id="8e54d-107">Cette interface est implémentée par le [MSP H323](h323-msp.md) et est exposée uniquement lorsqu’un appel utilise ce fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="8e54d-107">This interface is implemented by the [H323 MSP](h323-msp.md) and is exposed only when a call uses this service provider.</span></span>

## <a name="members"></a><span data-ttu-id="8e54d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8e54d-108">Members</span></span>

<span data-ttu-id="8e54d-109">L’interface **ITFormatControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8e54d-109">The **ITFormatControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8e54d-110">**ITFormatControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e54d-110">**ITFormatControl** also has these types of members:</span></span>

-   [<span data-ttu-id="8e54d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8e54d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8e54d-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8e54d-112">Methods</span></span>

<span data-ttu-id="8e54d-113">L’interface **ITFormatControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8e54d-113">The **ITFormatControl** interface has these methods.</span></span>



| <span data-ttu-id="8e54d-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="8e54d-114">Method</span></span>                                                                     | <span data-ttu-id="8e54d-115">Description</span><span class="sxs-lookup"><span data-stu-id="8e54d-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="8e54d-116">**GetCurrentFormat**</span><span class="sxs-lookup"><span data-stu-id="8e54d-116">**GetCurrentFormat**</span></span>](itformatcontrol-getcurrentformat.md)               | <span data-ttu-id="8e54d-117">Obtient le format multimédia du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="8e54d-117">Gets the media format of the current stream.</span></span><br/>                        |
| [<span data-ttu-id="8e54d-118">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8e54d-118">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md) | <span data-ttu-id="8e54d-119">Obtient le nombre de fonctionnalités associées au format actuel.</span><span class="sxs-lookup"><span data-stu-id="8e54d-119">Gets the number of capabilities associated with the current format.</span></span><br/> |
| [<span data-ttu-id="8e54d-120">**GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="8e54d-120">**GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)                     | <span data-ttu-id="8e54d-121">Obtient les fonctionnalités associées à un index de format donné.</span><span class="sxs-lookup"><span data-stu-id="8e54d-121">Gets the capabilities associated with a given format index.</span></span><br/>         |
| [<span data-ttu-id="8e54d-122">**ReleaseFormat**</span><span class="sxs-lookup"><span data-stu-id="8e54d-122">**ReleaseFormat**</span></span>](itformatcontrol-releaseformat.md)                     | <span data-ttu-id="8e54d-123">Libère la structure associée au format.</span><span class="sxs-lookup"><span data-stu-id="8e54d-123">Releases the structure associated with the format.</span></span><br/>                  |
| [<span data-ttu-id="8e54d-124">**ReOrderCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8e54d-124">**ReOrderCapabilities**</span></span>](itformatcontrol-reordercapabilities.md)         | <span data-ttu-id="8e54d-125">Définit une nouvelle commande pour les fonctionnalités de format.</span><span class="sxs-lookup"><span data-stu-id="8e54d-125">Sets a new order for format capabilities.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="8e54d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e54d-126">Requirements</span></span>



| <span data-ttu-id="8e54d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e54d-127">Requirement</span></span> | <span data-ttu-id="8e54d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e54d-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e54d-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8e54d-129">TAPI version</span></span><br/> | <span data-ttu-id="8e54d-130">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8e54d-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="8e54d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e54d-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8e54d-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e54d-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e54d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e54d-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8e54d-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e54d-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="8e54d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8e54d-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8e54d-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e54d-136"><dt>Tapi3.dll</dt></span></span> </dl> |



 


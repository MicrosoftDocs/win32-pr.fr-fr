---
description: L’interface ITCallQualityControl expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité des appels.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interface ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537510"
---
# <a name="itcallqualitycontrol-interface"></a><span data-ttu-id="87d38-103">Interface ITCallQualityControl</span><span class="sxs-lookup"><span data-stu-id="87d38-103">ITCallQualityControl interface</span></span>

<span data-ttu-id="87d38-104">\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="87d38-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="87d38-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="87d38-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="87d38-106">L’interface **ITCallQualityControl** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité des appels.</span><span class="sxs-lookup"><span data-stu-id="87d38-106">The **ITCallQualityControl** interface exposes methods that allow an application to get and set parameters for call quality control.</span></span>

<span data-ttu-id="87d38-107">Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="87d38-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="87d38-108">Elle est exposée uniquement lorsqu’un appel utilise ces fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="87d38-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="87d38-109">Membres</span><span class="sxs-lookup"><span data-stu-id="87d38-109">Members</span></span>

<span data-ttu-id="87d38-110">L’interface **ITCallQualityControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="87d38-110">The **ITCallQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="87d38-111">**ITCallQualityControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="87d38-111">**ITCallQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="87d38-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87d38-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="87d38-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87d38-113">Methods</span></span>

<span data-ttu-id="87d38-114">L’interface **ITCallQualityControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="87d38-114">The **ITCallQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="87d38-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="87d38-115">Method</span></span>                                            | <span data-ttu-id="87d38-116">Description</span><span class="sxs-lookup"><span data-stu-id="87d38-116">Description</span></span>                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87d38-117">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="87d38-117">**Get**</span></span>](itcallqualitycontrol-get.md)           | <span data-ttu-id="87d38-118">Obtient la valeur d’une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="87d38-118">Gets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="87d38-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="87d38-119">**GetRange**</span></span>](itcallqualitycontrol-getrange.md) | <span data-ttu-id="87d38-120">Obtient la plage de valeurs valides pour une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="87d38-120">Gets the range of valid values for a given [call quality control property](callqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="87d38-121">**Définissez**</span><span class="sxs-lookup"><span data-stu-id="87d38-121">**Set**</span></span>](itcallqualitycontrol-set.md)           | <span data-ttu-id="87d38-122">Définit la valeur d’une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="87d38-122">Sets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="87d38-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87d38-123">Requirements</span></span>



| <span data-ttu-id="87d38-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87d38-124">Requirement</span></span> | <span data-ttu-id="87d38-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="87d38-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87d38-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="87d38-126">TAPI version</span></span><br/> | <span data-ttu-id="87d38-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="87d38-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="87d38-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="87d38-128">Header</span></span><br/>       | <dl> <span data-ttu-id="87d38-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="87d38-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="87d38-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87d38-130">Library</span></span><br/>      | <dl> <span data-ttu-id="87d38-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87d38-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="87d38-132">DLL</span><span class="sxs-lookup"><span data-stu-id="87d38-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="87d38-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d38-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 


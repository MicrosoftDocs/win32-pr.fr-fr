---
description: L’interface ITQOSApplicationID expose une méthode qui permet à une application d’obtenir l’identificateur de QOS pour l’appel en cours.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interface ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543976"
---
# <a name="itqosapplicationid-interface"></a><span data-ttu-id="3a806-103">Interface ITQOSApplicationID</span><span class="sxs-lookup"><span data-stu-id="3a806-103">ITQOSApplicationID interface</span></span>

<span data-ttu-id="3a806-104">\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3a806-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3a806-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3a806-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3a806-106">L’interface **ITQOSApplicationID** expose une méthode qui permet à une application d’obtenir l’identificateur de QoS pour l’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="3a806-106">The **ITQOSApplicationID** interface exposes a method that allows an application to get the QOS identifier for the current call.</span></span>

<span data-ttu-id="3a806-107">Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et est exposée uniquement lorsqu’un appel utilise la conférence IP.</span><span class="sxs-lookup"><span data-stu-id="3a806-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and is exposed only when a call uses IP Conferencing.</span></span>

## <a name="members"></a><span data-ttu-id="3a806-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3a806-108">Members</span></span>

<span data-ttu-id="3a806-109">L’interface **ITQOSApplicationID** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3a806-109">The **ITQOSApplicationID** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3a806-110">**ITQOSApplicationID** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a806-110">**ITQOSApplicationID** also has these types of members:</span></span>

-   [<span data-ttu-id="3a806-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3a806-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3a806-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3a806-112">Methods</span></span>

<span data-ttu-id="3a806-113">L’interface **ITQOSApplicationID** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3a806-113">The **ITQOSApplicationID** interface has these methods.</span></span>



| <span data-ttu-id="3a806-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="3a806-114">Method</span></span>                                                                | <span data-ttu-id="3a806-115">Description</span><span class="sxs-lookup"><span data-stu-id="3a806-115">Description</span></span>                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="3a806-116">**SetQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="3a806-116">**SetQOSApplicationID**</span></span>](itqosapplicationid-setqosapplicationid.md) | <span data-ttu-id="3a806-117">Définit l’identificateur de QOS.</span><span class="sxs-lookup"><span data-stu-id="3a806-117">Sets the QOS identifier.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a806-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a806-118">Requirements</span></span>



| <span data-ttu-id="3a806-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a806-119">Requirement</span></span> | <span data-ttu-id="3a806-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a806-120">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a806-121">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3a806-121">TAPI version</span></span><br/> | <span data-ttu-id="3a806-122">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="3a806-122">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="3a806-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a806-123">Header</span></span><br/>       | <dl> <span data-ttu-id="3a806-124"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a806-124"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a806-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a806-125">Library</span></span><br/>      | <dl> <span data-ttu-id="3a806-126"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a806-126"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="3a806-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3a806-127">DLL</span></span><br/>          | <dl> <span data-ttu-id="3a806-128"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a806-128"><dt>Tapi3.dll</dt></span></span> </dl> |



 


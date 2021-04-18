---
description: L’interface IUpdateServiceRegistration définit les propriétés suivantes.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Propriétés IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515972"
---
# <a name="iupdateserviceregistration-properties"></a><span data-ttu-id="7fee4-103">Propriétés IUpdateServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="7fee4-103">IUpdateServiceRegistration Properties</span></span>

<span data-ttu-id="7fee4-104">L’interface **IUpdateServiceRegistration** définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7fee4-104">The **IUpdateServiceRegistration** interface defines the following properties.</span></span>



| <span data-ttu-id="7fee4-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="7fee4-105">Property</span></span>                                                                                      | <span data-ttu-id="7fee4-106">Description</span><span class="sxs-lookup"><span data-stu-id="7fee4-106">Description</span></span>                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fee4-107">**IsPendingRegistrationWithAU**</span><span class="sxs-lookup"><span data-stu-id="7fee4-107">**IsPendingRegistrationWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | <span data-ttu-id="7fee4-108">Obtient une valeur booléenne qui indique si le service est également inscrit avec Mises à jour automatiques, lorsqu’il est ajouté.</span><span class="sxs-lookup"><span data-stu-id="7fee4-108">Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.</span></span>                                  |
| [<span data-ttu-id="7fee4-109">**RegistrationState**</span><span class="sxs-lookup"><span data-stu-id="7fee4-109">**RegistrationState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | <span data-ttu-id="7fee4-110">Obtient une valeur [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) qui indique l’état actuel de l’inscription du service.</span><span class="sxs-lookup"><span data-stu-id="7fee4-110">Gets an [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) value that indicates the current state of the service registration.</span></span> |
| [<span data-ttu-id="7fee4-111">**Service**</span><span class="sxs-lookup"><span data-stu-id="7fee4-111">**Service**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | <span data-ttu-id="7fee4-112">Obtient un pointeur vers une interface [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) .</span><span class="sxs-lookup"><span data-stu-id="7fee4-112">Gets a pointer to an [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) interface.</span></span> <span data-ttu-id="7fee4-113">Cette propriété est la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="7fee4-113">This property is the default property.</span></span>                                    |



 

 

 




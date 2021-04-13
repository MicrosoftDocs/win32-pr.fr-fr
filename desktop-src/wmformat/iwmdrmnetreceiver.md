---
title: Interface IWMDRMNetReceiver
description: L’interface IWMDRMNetReceiver fournit les méthodes nécessaires à l’utilisation de Microsoft Windows Media DRM pour les périphériques réseau en tant que récepteur. Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject. Transmettez IID \_ IWMDRMNetReceiver comme paramètre riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Format Windows Media de l’interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380973"
---
# <a name="iwmdrmnetreceiver-interface"></a><span data-ttu-id="281e1-106">Interface IWMDRMNetReceiver</span><span class="sxs-lookup"><span data-stu-id="281e1-106">IWMDRMNetReceiver interface</span></span>

<span data-ttu-id="281e1-107">L’interface **IWMDRMNetReceiver** fournit les méthodes nécessaires à l’utilisation de Microsoft Windows Media DRM pour les périphériques réseau en tant que récepteur.</span><span class="sxs-lookup"><span data-stu-id="281e1-107">The **IWMDRMNetReceiver** interface provides methods needed to use Microsoft Windows Media DRM for Network Devices as a receiver.</span></span>

<span data-ttu-id="281e1-108">Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="281e1-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="281e1-109">Transmettez **IID \_ IWMDRMNetReceiver** comme paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="281e1-109">Pass **IID\_IWMDRMNetReceiver** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="281e1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="281e1-110">Members</span></span>

<span data-ttu-id="281e1-111">L’interface **IWMDRMNetReceiver** hérite de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="281e1-111">The **IWMDRMNetReceiver** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="281e1-112">**IWMDRMNetReceiver** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="281e1-112">**IWMDRMNetReceiver** also has these types of members:</span></span>

-   [<span data-ttu-id="281e1-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="281e1-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="281e1-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="281e1-114">Methods</span></span>

<span data-ttu-id="281e1-115">L’interface **IWMDRMNetReceiver** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="281e1-115">The **IWMDRMNetReceiver** interface has these methods.</span></span>



| <span data-ttu-id="281e1-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="281e1-116">Method</span></span>                                                                               | <span data-ttu-id="281e1-117">Description</span><span class="sxs-lookup"><span data-stu-id="281e1-117">Description</span></span>                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="281e1-118">**GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="281e1-118">**GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)                 | <span data-ttu-id="281e1-119">Génère une demande de licence qui est envoyée à l’émetteur lors de la demande de contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="281e1-119">Generates a license challenge that is sent to the transmitter when requesting protected content.</span></span><br/>                     |
| [<span data-ttu-id="281e1-120">**GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="281e1-120">**GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)       | <span data-ttu-id="281e1-121">Génère une demande d’inscription envoyée à l’émetteur lors de l’inscription ou de la revalidation du récepteur.</span><span class="sxs-lookup"><span data-stu-id="281e1-121">Generates a registration challenge that is sent to the transmitter when the receiver is registering or revalidating.</span></span><br/> |
| [<span data-ttu-id="281e1-122">**ProcessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="281e1-122">**ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)           | <span data-ttu-id="281e1-123">Traite la réponse de licence envoyée par l’émetteur en réponse à une demande de licence.</span><span class="sxs-lookup"><span data-stu-id="281e1-123">Processes the license response sent by the transmitter in reply to a license challenge.</span></span><br/>                              |
| [<span data-ttu-id="281e1-124">**ProcessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="281e1-124">**ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md) | <span data-ttu-id="281e1-125">Traite la réponse d’inscription envoyée par l’émetteur en réponse à une demande d’inscription.</span><span class="sxs-lookup"><span data-stu-id="281e1-125">Processes the registration response sent by the transmitter in reply to a registration challenge.</span></span><br/>                    |



 

## <a name="see-also"></a><span data-ttu-id="281e1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="281e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281e1-127">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="281e1-127">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="281e1-128">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="281e1-128">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> <dt>

[<span data-ttu-id="281e1-129">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="281e1-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 






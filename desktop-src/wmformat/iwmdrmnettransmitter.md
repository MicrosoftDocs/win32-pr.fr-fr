---
title: Interface IWMDRMNetTransmitter
description: L’interface IWMDRMNetTransmitter fournit les méthodes nécessaires pour utiliser Windows Media DRM pour les périphériques réseau en tant qu’émetteur. Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject. Transmettez IID \_ IWMDRMNetTransmitter comme paramètre riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Format Windows Media de l’interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315755"
---
# <a name="iwmdrmnettransmitter-interface"></a><span data-ttu-id="dba47-106">Interface IWMDRMNetTransmitter</span><span class="sxs-lookup"><span data-stu-id="dba47-106">IWMDRMNetTransmitter interface</span></span>

<span data-ttu-id="dba47-107">L’interface **IWMDRMNetTransmitter** fournit les méthodes nécessaires pour utiliser Windows Media DRM pour les périphériques réseau en tant qu’émetteur.</span><span class="sxs-lookup"><span data-stu-id="dba47-107">The **IWMDRMNetTransmitter** interface provides methods needed to use Windows Media DRM for Network Devices as a transmitter.</span></span>

<span data-ttu-id="dba47-108">Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="dba47-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="dba47-109">Transmettez **IID \_ IWMDRMNetTransmitter** comme paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="dba47-109">Pass **IID\_IWMDRMNetTransmitter** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="dba47-110">Membres</span><span class="sxs-lookup"><span data-stu-id="dba47-110">Members</span></span>

<span data-ttu-id="dba47-111">L’interface **IWMDRMNetTransmitter** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dba47-111">The **IWMDRMNetTransmitter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dba47-112">**IWMDRMNetTransmitter** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dba47-112">**IWMDRMNetTransmitter** also has these types of members:</span></span>

-   [<span data-ttu-id="dba47-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dba47-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dba47-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dba47-114">Methods</span></span>

<span data-ttu-id="dba47-115">L’interface **IWMDRMNetTransmitter** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dba47-115">The **IWMDRMNetTransmitter** interface has these methods.</span></span>



| <span data-ttu-id="dba47-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="dba47-116">Method</span></span>                                                                        | <span data-ttu-id="dba47-117">Description</span><span class="sxs-lookup"><span data-stu-id="dba47-117">Description</span></span>                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dba47-118">**GetLeafLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="dba47-118">**GetLeafLicenseResponse**</span></span>](iwmdrmnettransmitter-getleaflicenseresponse.md) | <span data-ttu-id="dba47-119">Génère un message de réponse de licence feuille.</span><span class="sxs-lookup"><span data-stu-id="dba47-119">Generates a leaf license response message.</span></span><br/>                                                       |
| [<span data-ttu-id="dba47-120">**GetRootLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="dba47-120">**GetRootLicenseResponse**</span></span>](iwmdrmnettransmitter-getrootlicenseresponse.md) | <span data-ttu-id="dba47-121">Génère un message de réponse de la licence racine</span><span class="sxs-lookup"><span data-stu-id="dba47-121">Generates a root license response message</span></span><br/>                                                        |
| [<span data-ttu-id="dba47-122">**SetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="dba47-122">**SetLicenseChallenge**</span></span>](iwmdrmnettransmitter-setlicensechallenge.md)       | <span data-ttu-id="dba47-123">Traite un challenge de licence envoyé par un récepteur Microsoft Windows Media DRM pour les périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="dba47-123">Processes a license challenge sent by a Microsoft Windows Media DRM for Network Devices receiver</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="dba47-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dba47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba47-125">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="dba47-125">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="dba47-126">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="dba47-126">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> </dl>

 


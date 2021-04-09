---
description: Définit une méthode de rappel unique.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interface IConnectionRequestCallback (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953096"
---
# <a name="iconnectionrequestcallback-interface"></a><span data-ttu-id="099c8-103">Interface IConnectionRequestCallback</span><span class="sxs-lookup"><span data-stu-id="099c8-103">IConnectionRequestCallback interface</span></span>

<span data-ttu-id="099c8-104">L’interface **IConnectionRequestCallback** définit une méthode de rappel unique.</span><span class="sxs-lookup"><span data-stu-id="099c8-104">The **IConnectionRequestCallback** interface defines a single callback method.</span></span> <span data-ttu-id="099c8-105">Une application Windows Mobile Devices (WPD) implémente cette interface COM (Component Object Model) facultative pour recevoir des notifications sur les demandes terminées et pour annuler les demandes en attente.</span><span class="sxs-lookup"><span data-stu-id="099c8-105">A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests.</span></span> <span data-ttu-id="099c8-106">Les demandes sont envoyées à l’aide des méthodes [**IPortableDeviceConnector :: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) et [**IPortableDeviceConnector ::D éconnecter**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="099c8-106">The requests are sent using the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="members"></a><span data-ttu-id="099c8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="099c8-107">Members</span></span>

<span data-ttu-id="099c8-108">L’interface **IConnectionRequestCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="099c8-108">The **IConnectionRequestCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="099c8-109">**IConnectionRequestCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="099c8-109">**IConnectionRequestCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="099c8-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="099c8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="099c8-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="099c8-111">Methods</span></span>

<span data-ttu-id="099c8-112">L’interface **IConnectionRequestCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="099c8-112">The **IConnectionRequestCallback** interface has these methods.</span></span>



| <span data-ttu-id="099c8-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="099c8-113">Method</span></span>                                                      | <span data-ttu-id="099c8-114">Description</span><span class="sxs-lookup"><span data-stu-id="099c8-114">Description</span></span>                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="099c8-115">**OnComplete**</span><span class="sxs-lookup"><span data-stu-id="099c8-115">**OnComplete**</span></span>](iconnectionrequestcallback-oncomplete.md) | <span data-ttu-id="099c8-116">Avertit une application qu’une demande précédemment planifiée est terminée.</span><span class="sxs-lookup"><span data-stu-id="099c8-116">Notifies an application that a previously scheduled request has completed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="099c8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="099c8-117">Requirements</span></span>



| <span data-ttu-id="099c8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="099c8-118">Requirement</span></span> | <span data-ttu-id="099c8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="099c8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099c8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="099c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="099c8-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="099c8-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="099c8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="099c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="099c8-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="099c8-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="099c8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="099c8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="099c8-125"><dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="099c8-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="099c8-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="099c8-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="099c8-127"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="099c8-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="099c8-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="099c8-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="099c8-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="099c8-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 


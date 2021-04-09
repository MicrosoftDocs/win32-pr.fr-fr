---
description: Notifie une application qu’une demande de connexion ou de déconnexion précédemment planifiée à l’appareil MTP/Bluetooth est terminée.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'IConnectionRequestCallback :: OnComplete, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866522"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a><span data-ttu-id="7ec48-103">IConnectionRequestCallback :: OnComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="7ec48-103">IConnectionRequestCallback::OnComplete method</span></span>

<span data-ttu-id="7ec48-104">La méthode **OnComplete** notifie une application qu’une demande de connexion ou de déconnexion précédemment planifiée à l’appareil MTP/Bluetooth est terminée</span><span class="sxs-lookup"><span data-stu-id="7ec48-104">The **OnComplete** method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec48-105">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a><span data-ttu-id="7ec48-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ec48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec48-107">*hrStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ec48-107">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec48-108">État de la demande de connexion ou de déconnexion d’un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="7ec48-108">The status of the request to connect or disconnect a given device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec48-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ec48-109">Return value</span></span>

<span data-ttu-id="7ec48-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7ec48-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7ec48-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7ec48-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7ec48-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7ec48-112">Return code</span></span>                                                                          | <span data-ttu-id="7ec48-113">Description</span><span class="sxs-lookup"><span data-stu-id="7ec48-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7ec48-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ec48-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7ec48-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ec48-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ec48-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7ec48-116">Remarks</span></span>

<span data-ttu-id="7ec48-117">Une application implémente l’interface [**IConnectionRequestCallback**](iconnectionrequestcallback.md) pour recevoir des notifications sur les demandes terminées et annuler les demandes en attente.</span><span class="sxs-lookup"><span data-stu-id="7ec48-117">An application implements the [**IConnectionRequestCallback**](iconnectionrequestcallback.md) interface to receive notifications about completed requests and to cancel pending requests.</span></span>

<span data-ttu-id="7ec48-118">Les appareils mobiles Windows (WPD) appellent cette méthode pour avertir une application qu’une demande précédemment planifiée est terminée.</span><span class="sxs-lookup"><span data-stu-id="7ec48-118">Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.</span></span> <span data-ttu-id="7ec48-119">Chaque demande peut être suivie et annulée par son rappel fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="7ec48-119">Each request can be tracked and canceled by its application-supplied callback.</span></span> <span data-ttu-id="7ec48-120">Par conséquent, si l’application doit envoyer plusieurs demandes en même temps à l’aide du même objet [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , chaque demande doit recevoir un objet [**IConnectionRequestCallback**](iconnectionrequestcallback.md) unique comme paramètre d’entrée des méthodes [**IPortableDeviceConnector :: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) et [**IPortableDeviceConnector ::D éconnecter**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="7ec48-120">Therefore, if the application needs to send multiple requests at the same time using the same [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) object, each request should be passed a unique [**IConnectionRequestCallback**](iconnectionrequestcallback.md) object as the input parameter to the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec48-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec48-121">Requirements</span></span>



| <span data-ttu-id="7ec48-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ec48-122">Requirement</span></span> | <span data-ttu-id="7ec48-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec48-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec48-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec48-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec48-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ec48-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="7ec48-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec48-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec48-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ec48-127">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="7ec48-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ec48-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ec48-129"><dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ec48-129"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="7ec48-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="7ec48-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ec48-131"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ec48-131"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="7ec48-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ec48-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ec48-133"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ec48-133"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="7ec48-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ec48-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec48-135">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="7ec48-135">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)
</dt> </dl>

 

 





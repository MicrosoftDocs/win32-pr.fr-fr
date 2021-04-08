---
description: Interfaces de connexion MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de connexion MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035167"
---
# <a name="mtpbluetooth-connection-interfaces"></a><span data-ttu-id="fd3f7-103">Interfaces de connexion MTP/Bluetooth</span><span class="sxs-lookup"><span data-stu-id="fd3f7-103">MTP/Bluetooth Connection Interfaces</span></span>

<span data-ttu-id="fd3f7-104">Les interfaces suivantes permettent aux applications d’énumérer et de se connecter uniquement aux périphériques qui prennent en charge le protocole MTP (Media Transfer Protocol) sur Bluetooth (MTP/Bluetooth).</span><span class="sxs-lookup"><span data-stu-id="fd3f7-104">The following interfaces allow applications to enumerate and connect only to devices that support the Media Transfer Protocol (MTP) over Bluetooth (MTP/Bluetooth).</span></span> <span data-ttu-id="fd3f7-105">Les interfaces du pilote WPD, du regroupement et du client ne sont pas limitées au protocole MTP/Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="fd3f7-105">The WPD driver-, collection-, and client-interfaces are not restricted to the MTP/ Bluetooth protocol.</span></span>



| <span data-ttu-id="fd3f7-106">Interface</span><span class="sxs-lookup"><span data-stu-id="fd3f7-106">Interface</span></span>                                                              | <span data-ttu-id="fd3f7-107">Description</span><span class="sxs-lookup"><span data-stu-id="fd3f7-107">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd3f7-108">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="fd3f7-108">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)       | <span data-ttu-id="fd3f7-109">Définit une méthode de rappel unique que les applications utilisent pour recevoir une notification des demandes terminées et annulées.</span><span class="sxs-lookup"><span data-stu-id="fd3f7-109">Defines a single callback method that applications use to receive notification of completed and cancelled requests.</span></span> |
| [<span data-ttu-id="fd3f7-110">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="fd3f7-110">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md) | <span data-ttu-id="fd3f7-111">Énumère les interfaces **IPortableDeviceConnector** .</span><span class="sxs-lookup"><span data-stu-id="fd3f7-111">Enumerates **IPortableDeviceConnector** interfaces.</span></span>                                                                 |
| [<span data-ttu-id="fd3f7-112">**IPortableDeviceConnector**</span><span class="sxs-lookup"><span data-stu-id="fd3f7-112">**IPortableDeviceConnector**</span></span>](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | <span data-ttu-id="fd3f7-113">Prend en charge les méthodes que les applications appellent pour établir des connexions aux périphériques Bluetooth MTP.</span><span class="sxs-lookup"><span data-stu-id="fd3f7-113">Supports methods that applications call to establish connections to MTP Bluetooth devices.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="fd3f7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd3f7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd3f7-115">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="fd3f7-115">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




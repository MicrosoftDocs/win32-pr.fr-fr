---
description: Installation du service dans le SPI Windows Sockets 2 (Winsock).
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Installation du service dans le SPI Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536358"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a><span data-ttu-id="96e82-103">Installation du service dans le SPI Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="96e82-103">Service Installation in the Windows Sockets 2 SPI</span></span>

-   [<span data-ttu-id="96e82-104">**NSPInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="96e82-104">**NSPInstallServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [<span data-ttu-id="96e82-105">**NSPRemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="96e82-105">**NSPRemoveServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [<span data-ttu-id="96e82-106">**NSPSetService**</span><span class="sxs-lookup"><span data-stu-id="96e82-106">**NSPSetService**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

<span data-ttu-id="96e82-107">Quand la classe de service requise n’existe pas encore, un client SPI d’espace de noms utilise [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) pour installer une nouvelle classe de service en fournissant un nom de classe de service, un GUID pour l’identificateur de classe de service et une série de structures [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="96e82-107">When the required service class does not already exist, a namespace SPI client uses [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="96e82-108">Ces structures sont spécifiques à un espace de noms particulier et fournissent des valeurs communes telles que des numéros de port TCP recommandés ou des identificateurs SAP SAP.</span><span class="sxs-lookup"><span data-stu-id="96e82-108">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="96e82-109">Une classe de service peut être supprimée en appelant [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) et en fournissant le GUID correspondant à l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="96e82-109">A service class can be removed by calling [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="96e82-110">Une fois qu’une classe de service existe, des instances spécifiques d’un service peuvent être installées ou supprimées via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span><span class="sxs-lookup"><span data-stu-id="96e82-110">Once a service class exists, specific instances of a service can be installed or removed via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span></span> <span data-ttu-id="96e82-111">Cette fonction prend une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) comme paramètre d’entrée avec un code d’opération et des indicateurs d’opération.</span><span class="sxs-lookup"><span data-stu-id="96e82-111">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="96e82-112">Le code d’opération indique si le service est en cours d’installation ou de suppression.</span><span class="sxs-lookup"><span data-stu-id="96e82-112">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="96e82-113">La structure **WSAQUERYSET** fournit toutes les informations pertinentes relatives au service, notamment l’identificateur de classe de service, le nom de service (pour cette instance), l’identificateur d’espace de noms applicable et les informations de protocole, ainsi qu’un ensemble d’adresses de transport vers lequel le service écoute.</span><span class="sxs-lookup"><span data-stu-id="96e82-113">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses to which the service listens.</span></span>

 

 




---
description: Winsock fournit une interface de fournisseur de services pour la création de services Winsock, communément appelée SPI Winsock.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: À propos de Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113115"
---
# <a name="about-the-winsock-spi"></a><span data-ttu-id="68cb0-103">À propos de Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="68cb0-103">About the Winsock SPI</span></span>

<span data-ttu-id="68cb0-104">Winsock fournit une interface de fournisseur de services pour la création de services Winsock, communément appelée SPI Winsock.</span><span class="sxs-lookup"><span data-stu-id="68cb0-104">Winsock provides a Service Provider Interface for creating Winsock services, commonly referred to as the Winsock SPI.</span></span> <span data-ttu-id="68cb0-105">Il existe deux types de fournisseurs de services : les fournisseurs de transport et les fournisseurs d’espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="68cb0-105">Two types of service providers exist: transport providers and namespace providers.</span></span> <span data-ttu-id="68cb0-106">Les exemples de fournisseurs de transport incluent des piles de protocole telles que TCP/IP ou IPX/SPX, tandis qu’un exemple de fournisseur d’espace de noms serait une interface avec le système d’attribution de noms de domaine (DNS) d’Internet.</span><span class="sxs-lookup"><span data-stu-id="68cb0-106">Examples of transport providers include protocol stacks such as TCP/IP or IPX/SPX, while an example of a namespace provider would be an interface to the Internet's Domain Naming System (DNS).</span></span> <span data-ttu-id="68cb0-107">Des sections distinctes de la spécification de l’interface du fournisseur de services s’appliquent à chaque type de fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="68cb0-107">Separate sections of the service provider interface specification apply to each type of service provider.</span></span>

<span data-ttu-id="68cb0-108">Les fournisseurs de services de [transport](transport-service-providers-2.md) et d' [espace de noms](name-space-service-providers-2.md) doivent être inscrits auprès de l' \_32.dll Ws2 au moment où ils sont installés.</span><span class="sxs-lookup"><span data-stu-id="68cb0-108">[Transport](transport-service-providers-2.md) and [namespace](name-space-service-providers-2.md) service providers must be registered with the Ws2\_32.dll at the time they are installed.</span></span> <span data-ttu-id="68cb0-109">Cette inscription ne doit être effectuée qu’une seule fois pour chaque fournisseur, car les informations nécessaires sont conservées dans un stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="68cb0-109">This registration need only be done once for each provider as the necessary information is retained in persistent storage.</span></span>

 

 




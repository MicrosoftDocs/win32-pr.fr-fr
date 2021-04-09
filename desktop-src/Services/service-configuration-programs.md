---
description: Les programmeurs et les administrateurs système utilisent des programmes de configuration de service pour modifier ou interroger la base de données des services installés.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programmes de configuration de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112782"
---
# <a name="service-configuration-programs"></a><span data-ttu-id="73470-103">Programmes de configuration de service</span><span class="sxs-lookup"><span data-stu-id="73470-103">Service Configuration Programs</span></span>

<span data-ttu-id="73470-104">Les programmeurs et les administrateurs système utilisent des programmes de configuration de service pour modifier ou interroger la base de données des services installés.</span><span class="sxs-lookup"><span data-stu-id="73470-104">Programmers and system administrators use service configuration programs to modify or query the database of installed services.</span></span> <span data-ttu-id="73470-105">La base de données est également accessible à l’aide des fonctions de registre.</span><span class="sxs-lookup"><span data-stu-id="73470-105">The database can also be accessed by using the registry functions.</span></span> <span data-ttu-id="73470-106">Toutefois, vous devez utiliser uniquement les fonctions de configuration SCM, qui garantissent que le service est correctement installé et configuré.</span><span class="sxs-lookup"><span data-stu-id="73470-106">However, you should only use the SCM configuration functions, which ensure that the service is properly installed and configured.</span></span>

<span data-ttu-id="73470-107">Les fonctions de configuration SCM requièrent soit un handle vers un objet SCManager, soit un handle vers un objet de service.</span><span class="sxs-lookup"><span data-stu-id="73470-107">The SCM configuration functions require either a handle to an SCManager object or a handle to a service object.</span></span> <span data-ttu-id="73470-108">Pour obtenir ces handles, le programme de configuration de service doit :</span><span class="sxs-lookup"><span data-stu-id="73470-108">To obtain these handles, the service configuration program must:</span></span>

1.  <span data-ttu-id="73470-109">Utilisez la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pour obtenir un descripteur de la base de données SCM sur une machine spécifiée.</span><span class="sxs-lookup"><span data-stu-id="73470-109">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="73470-110">Utilisez la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) pour obtenir un handle de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="73470-110">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="73470-111">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="73470-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="73470-112">Installation, suppression et énumération des services</span><span class="sxs-lookup"><span data-stu-id="73470-112">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
-   [<span data-ttu-id="73470-113">Configuration de service</span><span class="sxs-lookup"><span data-stu-id="73470-113">Service Configuration</span></span>](service-configuration.md)
-   [<span data-ttu-id="73470-114">Configuration d’un service à l’aide de SC</span><span class="sxs-lookup"><span data-stu-id="73470-114">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)

 

 




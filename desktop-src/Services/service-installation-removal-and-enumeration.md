---
description: Un programme de configuration utilise la fonction CreateService pour installer un nouveau service dans la base de données SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Installation, suppression et énumération des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751060"
---
# <a name="service-installation-removal-and-enumeration"></a><span data-ttu-id="9f74d-103">Installation, suppression et énumération des services</span><span class="sxs-lookup"><span data-stu-id="9f74d-103">Service Installation, Removal, and Enumeration</span></span>

<span data-ttu-id="9f74d-104">Un programme de configuration utilise la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) pour installer un nouveau service dans la base de données SCM.</span><span class="sxs-lookup"><span data-stu-id="9f74d-104">A configuration program uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a new service in the SCM database.</span></span> <span data-ttu-id="9f74d-105">Cette fonction spécifie le nom du service et fournit des informations de configuration qui sont stockées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="9f74d-105">This function specifies the name of the service and provides configuration information that is stored in the database.</span></span> <span data-ttu-id="9f74d-106">Pour obtenir une description des informations stockées dans la base de données pour chaque service, consultez [base de données des services installés](database-of-installed-services.md).</span><span class="sxs-lookup"><span data-stu-id="9f74d-106">For a description of the information stored in the database for each service, see [Database of Installed Services](database-of-installed-services.md).</span></span> <span data-ttu-id="9f74d-107">Pour obtenir un exemple de code, consultez [installation d’un service](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="9f74d-107">For sample code, see [Installing a Service](installing-a-service.md).</span></span>

<span data-ttu-id="9f74d-108">Un programme de configuration utilise la fonction [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) pour supprimer un service installé de la base de données.</span><span class="sxs-lookup"><span data-stu-id="9f74d-108">A configuration program uses the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to remove an installed service from the database.</span></span> <span data-ttu-id="9f74d-109">Pour plus d’informations, consultez [Suppression d’un service](deleting-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="9f74d-109">For more information, see [Deleting a Service](deleting-a-service.md).</span></span>

<span data-ttu-id="9f74d-110">Pour obtenir le nom du service, appelez la fonction [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) .</span><span class="sxs-lookup"><span data-stu-id="9f74d-110">To obtain the service name, call the [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) function.</span></span> <span data-ttu-id="9f74d-111">Le nom d’affichage du service, utilisé dans l’applet services du panneau de configuration, peut être obtenu en appelant la fonction [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .</span><span class="sxs-lookup"><span data-stu-id="9f74d-111">The service display name, used in the Services control panel applet, can be obtained by calling the [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) function.</span></span>

<span data-ttu-id="9f74d-112">Un programme de configuration de service peut utiliser la fonction [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) pour énumérer tous les services et leurs États.</span><span class="sxs-lookup"><span data-stu-id="9f74d-112">A service configuration program can use the [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to enumerate all services and their statuses.</span></span> <span data-ttu-id="9f74d-113">Elle peut également utiliser la fonction [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) pour énumérer les services qui dépendent d’un objet de service spécifié.</span><span class="sxs-lookup"><span data-stu-id="9f74d-113">It can also use the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate which services are dependent on a specified service object.</span></span>

 

 




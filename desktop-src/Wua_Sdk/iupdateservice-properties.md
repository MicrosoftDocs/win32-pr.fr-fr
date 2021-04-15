---
description: L’interface IUpdateService définit les propriétés suivantes.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Propriétés IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485129"
---
# <a name="iupdateservice-properties"></a><span data-ttu-id="7e60c-103">Propriétés IUpdateService</span><span class="sxs-lookup"><span data-stu-id="7e60c-103">IUpdateService Properties</span></span>

<span data-ttu-id="7e60c-104">L’interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e60c-104">The [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface defines the following properties.</span></span>



| <span data-ttu-id="7e60c-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="7e60c-105">Property</span></span>                                                              | <span data-ttu-id="7e60c-106">Description</span><span class="sxs-lookup"><span data-stu-id="7e60c-106">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e60c-107">**CanRegisterWithAU**</span><span class="sxs-lookup"><span data-stu-id="7e60c-107">**CanRegisterWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | <span data-ttu-id="7e60c-108">Obtient une valeur booléenne qui indique si le service peut s’inscrire auprès de Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="7e60c-108">Gets a Boolean value that indicates whether the service can register with Automatic Updates.</span></span>    |
| [<span data-ttu-id="7e60c-109">**ContentValidationCert**</span><span class="sxs-lookup"><span data-stu-id="7e60c-109">**ContentValidationCert**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | <span data-ttu-id="7e60c-110">Obtient un hachage SHA-1 du certificat utilisé pour signer le contenu du service.</span><span class="sxs-lookup"><span data-stu-id="7e60c-110">Gets an SHA-1 hash of the certificate that is used to sign the contents of the service.</span></span>         |
| [<span data-ttu-id="7e60c-111">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="7e60c-111">**ExpirationDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | <span data-ttu-id="7e60c-112">Obtient la date à laquelle le fichier cab d’autorisation expire.</span><span class="sxs-lookup"><span data-stu-id="7e60c-112">Gets the date on which the authorization cabinet file expires.</span></span>                                  |
| [<span data-ttu-id="7e60c-113">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="7e60c-113">**IsManaged**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | <span data-ttu-id="7e60c-114">Obtient une valeur booléenne qui indique si un service est un service managé.</span><span class="sxs-lookup"><span data-stu-id="7e60c-114">Gets a Boolean value that indicates whether a service is a managed service.</span></span>                     |
| [<span data-ttu-id="7e60c-115">**IsRegisteredWithAU**</span><span class="sxs-lookup"><span data-stu-id="7e60c-115">**IsRegisteredWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | <span data-ttu-id="7e60c-116">Obtient une valeur booléenne qui indique si un service est inscrit avec Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="7e60c-116">Gets a Boolean value that indicates whether a service is registered with Automatic Updates.</span></span>     |
| [<span data-ttu-id="7e60c-117">**IsScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="7e60c-117">**IsScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | <span data-ttu-id="7e60c-118">Obtient une valeur booléenne qui indique si un service est basé sur un package d’analyse.</span><span class="sxs-lookup"><span data-stu-id="7e60c-118">Gets a Boolean value that indicates whether a service is based on a scan package.</span></span>               |
| [<span data-ttu-id="7e60c-119">**Émis**</span><span class="sxs-lookup"><span data-stu-id="7e60c-119">**IssueDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | <span data-ttu-id="7e60c-120">Obtient la date à laquelle le fichier cab d’autorisation a été émis.</span><span class="sxs-lookup"><span data-stu-id="7e60c-120">Gets the date on which the authorization cabinet file was issued.</span></span>                               |
| [<span data-ttu-id="7e60c-121">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7e60c-121">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | <span data-ttu-id="7e60c-122">Obtient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="7e60c-122">Gets the name of the service.</span></span>                                                                   |
| [<span data-ttu-id="7e60c-123">**OffersWindowsUpdates**</span><span class="sxs-lookup"><span data-stu-id="7e60c-123">**OffersWindowsUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | <span data-ttu-id="7e60c-124">Obtient une valeur booléenne qui indique si le service en cours propose des mises à jour à partir des mises à jour Windows.</span><span class="sxs-lookup"><span data-stu-id="7e60c-124">Gets a Boolean value indicates whether the current service offers updates from Windows Updates.</span></span> |
| [<span data-ttu-id="7e60c-125">**RedirectUrls**</span><span class="sxs-lookup"><span data-stu-id="7e60c-125">**RedirectUrls**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | <span data-ttu-id="7e60c-126">Obtient l’URL du fichier CAB du redirecteur.</span><span class="sxs-lookup"><span data-stu-id="7e60c-126">Gets the URL for the redirector cabinet file.</span></span>                                                   |
| [<span data-ttu-id="7e60c-127">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="7e60c-127">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | <span data-ttu-id="7e60c-128">Obtient l’identificateur d’un service.</span><span class="sxs-lookup"><span data-stu-id="7e60c-128">Gets the identifier for a service.</span></span>                                                              |
| [<span data-ttu-id="7e60c-129">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="7e60c-129">**ServiceUrl**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | <span data-ttu-id="7e60c-130">Obtient l’URL du service.</span><span class="sxs-lookup"><span data-stu-id="7e60c-130">Gets the URL for the service.</span></span>                                                                   |
| [<span data-ttu-id="7e60c-131">**SetupPrefix**</span><span class="sxs-lookup"><span data-stu-id="7e60c-131">**SetupPrefix**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | <span data-ttu-id="7e60c-132">Obtient le préfixe pour les fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="7e60c-132">Gets the prefix for the setup files.</span></span>                                                            |



 

 

 




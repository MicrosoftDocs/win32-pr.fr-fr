---
title: Proxy d'application web
description: Proxy d'application web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104102465"
---
# <a name="web-application-proxy"></a><span data-ttu-id="4578e-103">Proxy d'application web</span><span class="sxs-lookup"><span data-stu-id="4578e-103">Web Application Proxy</span></span>

## <a name="platform"></a><span data-ttu-id="4578e-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="4578e-104">Platform</span></span>

<span data-ttu-id="4578e-105">**Serveurs-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4578e-105">**Servers -** Windows Server 2012 R2</span></span>  






## <a name="description"></a><span data-ttu-id="4578e-106">Description</span><span class="sxs-lookup"><span data-stu-id="4578e-106">Description</span></span>

<span data-ttu-id="4578e-107">Dans Windows Server 2012 R2, nous avons ajouté un nouveau service appelé proxy d’application Web sous le rôle accès à distance qui permet aux administrateurs de publier des applications pour un accès externe.</span><span class="sxs-lookup"><span data-stu-id="4578e-107">In Windows Server 2012 R2, we added a new service called the Web Application Proxy under the Remote Access role that allows administrators to publish applications for external access.</span></span> <span data-ttu-id="4578e-108">Ce service agit comme un proxy inverse et comme un proxy services de fédération Active Directory (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="4578e-108">This service acts as a reverse proxy and as an Active Directory Federation Services (AD FS) proxy.</span></span> <span data-ttu-id="4578e-109">En fait, ce service remplace le service de proxy AD FS tel qu’il a été connu dans Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="4578e-109">In fact, this service replaces the AD FS proxy service as it was known in Windows Server 2012.</span></span>

<span data-ttu-id="4578e-110">Avec le proxy d’application Web, une organisation peut mettre des ressources Web locales à la disposition d’un accès externe tout en gérant le risque de cet accès en contrôlant les stratégies d’authentification et d’autorisation sur le AD FS.</span><span class="sxs-lookup"><span data-stu-id="4578e-110">With the Web Application Proxy, an organization can make on-premises web resources available for external access while at the same time managing the risk of this access by controlling authentication and authorization policies on the AD FS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="4578e-111">Manifestation</span><span class="sxs-lookup"><span data-stu-id="4578e-111">Manifestation</span></span>

<span data-ttu-id="4578e-112">Le service proxy AD FS n’est plus sous le rôle services de fédération Active Directory (AD FS) (AD FS), mais il a été remplacé par le proxy d’application Web sous le rôle accès à distance.</span><span class="sxs-lookup"><span data-stu-id="4578e-112">The AD FS proxy service is no longer under the Active Directory Federation Services role (AD FS), but has been replaced by the Web Application Proxy under the Remote Access role.</span></span> <span data-ttu-id="4578e-113">Cela représente une expansion du service de proxy AD FS en incluant la fonctionnalité de proxy inverse pour la publication d’applications.</span><span class="sxs-lookup"><span data-stu-id="4578e-113">This represents an expansion of the AD FS proxy service by including reverse proxy functionality for application publishing.</span></span>

## <a name="solution"></a><span data-ttu-id="4578e-114">Solution</span><span class="sxs-lookup"><span data-stu-id="4578e-114">Solution</span></span>

<span data-ttu-id="4578e-115">Pour accéder au proxy d’application Web, les administrateurs peuvent accéder à Gestionnaire de serveur et ajouter un nouveau rôle/service de rôle.</span><span class="sxs-lookup"><span data-stu-id="4578e-115">To access the Web Application Proxy, administrators can go to Server Manager and add a new role/role service.</span></span> <span data-ttu-id="4578e-116">L’administrateur trouvera le proxy d’application Web sous le rôle accès à distance.</span><span class="sxs-lookup"><span data-stu-id="4578e-116">The administrator will find the Web Application Proxy under the Remote Access role.</span></span>

## <a name="resources"></a><span data-ttu-id="4578e-117">Ressources</span><span class="sxs-lookup"><span data-stu-id="4578e-117">Resources</span></span>

-   <span data-ttu-id="4578e-118">[Guide des solutions](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="4578e-118">[Solution guide](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span></span>

 

 
---
description: Décisions de conception des clés de contrôle parental
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Décisions de conception des clés de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042744"
---
# <a name="parental-controls-key-design-decisions"></a><span data-ttu-id="216aa-103">Décisions de conception des clés de contrôle parental</span><span class="sxs-lookup"><span data-stu-id="216aa-103">Parental Controls Key Design Decisions</span></span>

<span data-ttu-id="216aa-104">Les principales décisions en matière de conception dans le développement des contrôles parentaux Windows Vista sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="216aa-104">Major design decisions in the development of Windows Vista Parental Controls are:</span></span>

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a><span data-ttu-id="216aa-105">Dépendance essentielle sur la fonctionnalité de contrôle de compte d’utilisateur (UAC) de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="216aa-105">Essential Dependency on Windows Vista User Account Control (UAC) Feature</span></span>

<span data-ttu-id="216aa-106">Une décision essentielle pour le contrôle parental de Windows Vista consiste à s’appuyer sur la nouvelle fonctionnalité de contrôle de compte d’utilisateur (UAC) pour implémenter les identités de compte de droits réduites, particulièrement nécessaires pour les restrictions hors connexion sur les utilisateurs contrôlés.</span><span class="sxs-lookup"><span data-stu-id="216aa-106">A key decision for Windows Vista Parental Controls is to rely on the new User Account Control (UAC) feature to implement the reduced rights account identities especially needed for offline restrictions on controlled users.</span></span> <span data-ttu-id="216aa-107">Pour plus d’informations sur [le contrôle de compte d’utilisateur, consultez Windows Vista et Windows Server 2008 Developer Story : Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="216aa-107">For more information about UAC, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)).</span></span> <span data-ttu-id="216aa-108">En résumé, chaque compte disposant de droits d’administrateur a des privilèges suffisants pour l’affichage des données de journal et la définition des stratégies.</span><span class="sxs-lookup"><span data-stu-id="216aa-108">In summary, every account with administrator rights effectively has privileges to perform the parent or guardian role of viewing log data and setting policies.</span></span> <span data-ttu-id="216aa-109">Les contrôles parentaux ne peuvent être définis que sur les utilisateurs à droits standard (anciennement appelés comptes d’utilisateur dotés de privilèges minimum, ou LUAs), car ils ne peuvent pas modifier les journaux et les paramètres avec les listes de Access Control (ACL) configurés uniquement pour les administrateurs à écrire.</span><span class="sxs-lookup"><span data-stu-id="216aa-109">Parental controls may only be set on standard-rights users (formerly called Least-privileged User Accounts, or LUAs), as only they cannot alter logs and settings with Access Control Lists (ACLs) configured only for administrators to write.</span></span> <span data-ttu-id="216aa-110">En d’autres termes :</span><span class="sxs-lookup"><span data-stu-id="216aa-110">In other words:</span></span>

-   <span data-ttu-id="216aa-111">Une identité parente ou Guardian est implicitement égale à un compte disposant des droits d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="216aa-111">A parent or guardian identity implicitly equals an account that has rights of an administrator.</span></span>
-   <span data-ttu-id="216aa-112">Les utilisateurs sous contrôle parent doivent être des utilisateurs standard.</span><span class="sxs-lookup"><span data-stu-id="216aa-112">Parentally controlled users must be standard users.</span></span>

## <a name="nearly-all-settings-are-available-by-apis"></a><span data-ttu-id="216aa-113">Presque tous les paramètres sont disponibles par les API</span><span class="sxs-lookup"><span data-stu-id="216aa-113">Nearly All Settings Are Available by APIs</span></span>

<span data-ttu-id="216aa-114">À l’exception des éléments tels que les définitions de système de contrôle d’accès, les paramètres disponibles pour la manipulation par l’interface utilisateur des contrôles parentaux peuvent également être modifiés par les API exposées.</span><span class="sxs-lookup"><span data-stu-id="216aa-114">With the exception of items such as ratings system definitions, settings available for manipulation by the Parental Controls User Interface may also be modified by exposed APIs.</span></span> <span data-ttu-id="216aa-115">Il est nécessaire que les programmes implémentent l’élévation aux droits d’administration afin de modifier les paramètres, comme indiqué ci-dessus pour le contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="216aa-115">It is necessary for programs to implement elevation to administrative rights in order to alter settings, as noted above for UAC.</span></span>

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a><span data-ttu-id="216aa-116">Le contrôle parental de Windows Vista est une technologie exclusivement réservée aux consommateurs.</span><span class="sxs-lookup"><span data-stu-id="216aa-116">Windows Vista Parental Controls Is a Consumer-only Technology</span></span>

<span data-ttu-id="216aa-117">Les contrôles parentaux Windows Vista ne sont pas destinés à être utilisés avec les comptes de domaine.</span><span class="sxs-lookup"><span data-stu-id="216aa-117">Windows Vista Parental Controls are not intended to be used with domain accounts.</span></span> <span data-ttu-id="216aa-118">En tant que technologie de consommation, le contrôle parental n’est pas déployé sur les références SKU commerciales de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="216aa-118">As a consumer technology, Parental Controls is not deployed in business SKUs of Windows Vista.</span></span> <span data-ttu-id="216aa-119">Si un ordinateur est joint à un domaine, les liens de l’interface utilisateur de sécurité de famille seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="216aa-119">If a computer is joined to a domain, the Family Safety user interface links will be suppressed.</span></span>

<span data-ttu-id="216aa-120">Un mécanisme sera fourni pour exposer les fonctionnalités du cas joint à un domaine, mais seuls les comptes d’utilisateur non-domaine peuvent être configurés avec des contrôles de contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="216aa-120">A mechanism will be provided to expose the functionality for the domain-joined case, but only non-domain user accounts may be configured with Parental Controls.</span></span>

 

 

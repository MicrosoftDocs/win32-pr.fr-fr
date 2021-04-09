---
description: L’objet TrustedDomain stocke les informations relatives à une relation d’approbation avec un domaine.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Objet TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862297"
---
# <a name="trusteddomain-object"></a><span data-ttu-id="e5c75-103">Objet TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="e5c75-103">TrustedDomain Object</span></span>

<span data-ttu-id="e5c75-104">L’objet **trustedDomain** stocke les informations relatives à une relation d’approbation avec un domaine.</span><span class="sxs-lookup"><span data-stu-id="e5c75-104">The **TrustedDomain** object stores information about a trust relationship with a domain.</span></span> <span data-ttu-id="e5c75-105">Un objet **trustedDomain** est créé sur le système d’approbation pour identifier un compte au sein du domaine approuvé qui peut être utilisé pour envoyer des demandes d’authentification et effectuer d’autres opérations, telles que le nom et les traductions de l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID).</span><span class="sxs-lookup"><span data-stu-id="e5c75-105">A **TrustedDomain** object is created on the trusting system to identify an account within the trusted domain that can be used to submit authentication requests and to perform other operations, such as name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) translations.</span></span>

<span data-ttu-id="e5c75-106">Les informations stockées dans un objet **trustedDomain** incluent :</span><span class="sxs-lookup"><span data-stu-id="e5c75-106">The information stored in a **TrustedDomain** object includes:</span></span>

-   <span data-ttu-id="e5c75-107">SID du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="e5c75-107">The SID of the trusted domain.</span></span> <span data-ttu-id="e5c75-108">Ces informations ne sont pas modifiables et doivent être uniques parmi tous les objets **trustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="e5c75-108">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="e5c75-109">Nom du domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="e5c75-109">The name of the trusted domain.</span></span> <span data-ttu-id="e5c75-110">Ces informations ne sont pas modifiables et doivent être uniques parmi tous les objets **trustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="e5c75-110">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="e5c75-111">Nom du compte dans le domaine approuvé utilisé pour soumettre les demandes d’authentification et pour effectuer des traductions de nom et SID.</span><span class="sxs-lookup"><span data-stu-id="e5c75-111">The name of the account in the trusted domain used to submit authentication requests and to perform name and SID translations.</span></span> <span data-ttu-id="e5c75-112">Ce nom n’est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="e5c75-112">This name is not modifiable.</span></span>
-   <span data-ttu-id="e5c75-113">Mot de passe utilisé pour soumettre les demandes d’authentification et effectuer des traductions de nom et SID.</span><span class="sxs-lookup"><span data-stu-id="e5c75-113">The password used to submit authentication requests and perform name and SID translations.</span></span>

<span data-ttu-id="e5c75-114">Pour plus d’informations, consultez [type d’objet trustedDomain](the-trusteddomain-object-type.md).</span><span class="sxs-lookup"><span data-stu-id="e5c75-114">For more information, see [The TrustedDomain Object Type](the-trusteddomain-object-type.md).</span></span>

 

 

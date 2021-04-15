---
description: Les termes suivants décrivent les domaines qui existent sur les systèmes distants.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Domaines principaux et approuvés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525719"
---
# <a name="primary-and-trusted-domains"></a><span data-ttu-id="62655-103">Domaines principaux et approuvés</span><span class="sxs-lookup"><span data-stu-id="62655-103">Primary and Trusted Domains</span></span>

<span data-ttu-id="62655-104">Les termes suivants décrivent les domaines qui existent sur les systèmes distants.</span><span class="sxs-lookup"><span data-stu-id="62655-104">The following terms describe domains that exist on remote systems.</span></span>

-   [<span data-ttu-id="62655-105">Domaine principal</span><span class="sxs-lookup"><span data-stu-id="62655-105">Primary Domain</span></span>](#primary-domain)
-   [<span data-ttu-id="62655-106">Domaine approuvé</span><span class="sxs-lookup"><span data-stu-id="62655-106">Trusted Domain</span></span>](#primary-and-trusted-domains)

## <a name="primary-domain"></a><span data-ttu-id="62655-107">Domaine principal</span><span class="sxs-lookup"><span data-stu-id="62655-107">Primary Domain</span></span>

<span data-ttu-id="62655-108">Un domaine principal est le domaine qui est responsable de l’établissement de relations d’approbation supplémentaires et de l’exécution de l’authentification (ou pour la transmission d’une demande d’authentification à un domaine approuvé approprié).</span><span class="sxs-lookup"><span data-stu-id="62655-108">A primary domain is the domain that is responsible for establishing further trust relationships and performing authentication (or for passing an authentication request on to an appropriate trusted domain).</span></span> <span data-ttu-id="62655-109">Les contrôleurs de domaine dans le domaine principal gèrent ou transmettent les demandes d’authentification qui proviennent de la station de travail.</span><span class="sxs-lookup"><span data-stu-id="62655-109">The domain controllers in the primary domain handle or pass along authentication requests that originate at the workstation.</span></span>

<span data-ttu-id="62655-110">Lorsque l’ouverture de session se produit, l’autorité LSA vérifie les informations d’authentification dans les domaines intégrés et de compte.</span><span class="sxs-lookup"><span data-stu-id="62655-110">When logon occurs, the LSA checks the built-in and account domains for authentication information.</span></span> <span data-ttu-id="62655-111">Si le compte qui est connecté à ne figure pas dans l’un de ces domaines, la demande d’ouverture de session est transmise au domaine principal du système.</span><span class="sxs-lookup"><span data-stu-id="62655-111">If the account being logged on to is not in either of these domains, the logon request is handed off to the system's primary domain.</span></span>

## <a name="trusted-domain"></a><span data-ttu-id="62655-112">Domaine approuvé</span><span class="sxs-lookup"><span data-stu-id="62655-112">Trusted Domain</span></span>

<span data-ttu-id="62655-113">Un domaine approuvé est un domaine approuvé par le système local pour authentifier les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="62655-113">A trusted domain is a domain that the local system trusts to authenticate users.</span></span> <span data-ttu-id="62655-114">En d’autres termes, si un utilisateur ou une application est authentifié par un domaine approuvé, cette authentification est acceptée par tous les domaines qui approuvent le domaine d’authentification.</span><span class="sxs-lookup"><span data-stu-id="62655-114">In other words, if a user or application is authenticated by a trusted domain, this authentication is accepted by all domains that trust the authenticating domain.</span></span>

<span data-ttu-id="62655-115">Chaque domaine subordonné a automatiquement une relation d’approbation bidirectionnelle avec le domaine principal.</span><span class="sxs-lookup"><span data-stu-id="62655-115">Each subordinate domain automatically has a two-way trust relationship with the main domain.</span></span> <span data-ttu-id="62655-116">Par défaut, cette approbation est transitive, ce qui signifie que si un système approuve le domaine A, il approuve également tous les domaines approuvés par le domaine A.</span><span class="sxs-lookup"><span data-stu-id="62655-116">By default, this trust is transitive, meaning that if a system trusts Domain A, it also trusts all domains that Domain A trusts.</span></span> <span data-ttu-id="62655-117">Les approbations à sens unique sont également prises en charge pour les systèmes d’exploitation antérieurs à Windows 2000, qui ne prennent pas en charge les approbations transitives bidirectionnelles.</span><span class="sxs-lookup"><span data-stu-id="62655-117">One-way trusts are also supported for operating systems earlier than Windows 2000, which do not support transitive, two-way trusts.</span></span>

<span data-ttu-id="62655-118">L' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) a un type d’objet, [**trustedDomain**](the-trusteddomain-object-type.md), qui est utilisé pour stocker des informations sur les relations d’approbation, y compris le nom et l' [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du domaine approuvé, le compte dans le domaine à utiliser pour les demandes d’authentification, les demandes de traduction de nom et SID et les noms des contrôleurs de domaine dans le domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="62655-118">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) has an object type, [**TrustedDomain**](the-trusteddomain-object-type.md), that is used to store information about trust relationships, including the name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the trusted domain, the account in the domain to use for authentication requests, name and SID translation requests, and the names of domain controllers in the trusted domain.</span></span>

<span data-ttu-id="62655-119">Sur les contrôleurs de domaine, l’autorité LSA crée une instance d’un objet [**trustedDomain**](the-trusteddomain-object-type.md) pour chaque domaine approuvé par le système local.</span><span class="sxs-lookup"><span data-stu-id="62655-119">On domain controllers, the LSA creates an instance of a [**TrustedDomain**](the-trusteddomain-object-type.md) object for each domain trusted by the local system.</span></span>

<span data-ttu-id="62655-120">Par exemple, si une station de travail Windows XP approuve un contrôleur de domaine Windows 2000 qui, à son tour, approuve quatre autres systèmes, la station de travail, connectée à l’aide d’une approbation transitive, aura cinq objets [**trustedDomain**](the-trusteddomain-object-type.md) sur son système local.</span><span class="sxs-lookup"><span data-stu-id="62655-120">For example, if a Windows XP workstation trusts a Windows 2000 domain controller that in turn trusts four other systems, the workstation, connected using transitive trust, will have five [**TrustedDomain**](the-trusteddomain-object-type.md) objects on its local system.</span></span>

 

 

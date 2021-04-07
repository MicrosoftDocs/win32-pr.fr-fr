---
title: À propos de NAP
description: À propos de NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671417"
---
# <a name="about-nap"></a><span data-ttu-id="b758c-103">À propos de NAP</span><span class="sxs-lookup"><span data-stu-id="b758c-103">About NAP</span></span>

> [!Note]  
> <span data-ttu-id="b758c-104">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b758c-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b758c-105">La protection d’accès réseau (NAP) est conçue pour aider les administrateurs à maintenir l’intégrité des ordinateurs sur le réseau, ce qui, à son tour, permet de maintenir l’intégrité globale du réseau.</span><span class="sxs-lookup"><span data-stu-id="b758c-105">Network Access Protection (NAP) is designed to help administrators maintain the health of the computers on the network, which in turns helps maintain the overall integrity of the network.</span></span> <span data-ttu-id="b758c-106">Elle n’est pas conçue pour protéger un réseau contre les utilisateurs malveillants.</span><span class="sxs-lookup"><span data-stu-id="b758c-106">It is not designed to secure a network from malicious users.</span></span> <span data-ttu-id="b758c-107">Par exemple, si un ordinateur dispose de tous les logiciels et configurations requis par la stratégie d’accès réseau, l’ordinateur est considéré comme sain ou conforme, et il se verra accorder l’accès approprié au réseau.</span><span class="sxs-lookup"><span data-stu-id="b758c-107">For example, if a computer has all the software and configurations that the network access policy requires, the computer is considered healthy or compliant, and it will be granted the appropriate access to the network.</span></span> <span data-ttu-id="b758c-108">La protection d’accès réseau n’empêche pas un utilisateur autorisé avec un ordinateur conforme de télécharger un programme malveillant sur le réseau ou d’effectuer un autre comportement inapproprié.</span><span class="sxs-lookup"><span data-stu-id="b758c-108">NAP does not prevent an authorized user with a compliant computer from uploading a malicious program to the network or engaging in other inappropriate behavior.</span></span>

<span data-ttu-id="b758c-109">Pour protéger l’accès à un réseau, une infrastructure réseau doit fournir les zones de fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="b758c-109">To protect access to a network, a network infrastructure needs to provide the following areas of functionality:</span></span>

-   <span data-ttu-id="b758c-110">Validation de l’intégrité : détermine si les ordinateurs sont conformes aux spécifications d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="b758c-110">Health validation: Determines whether the computers are compliant with system health requirements.</span></span>
-   <span data-ttu-id="b758c-111">Restriction réseau : restreint l’accès au réseau ou à la communication pour les clients qui ne sont pas conformes aux exigences d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="b758c-111">Network restriction: Restricts access to the network or communication for clients that do not comply with system health requirements.</span></span>
-   <span data-ttu-id="b758c-112">Correction : fournit les mises à jour nécessaires pour permettre à l’ordinateur de corriger son état d’intégrité non conforme.</span><span class="sxs-lookup"><span data-stu-id="b758c-112">Remediation: Provides necessary updates to allow the computer to correct its noncompliant health state.</span></span>
-   <span data-ttu-id="b758c-113">Conformité en cours : autorise l’accès au réseau tant que l’ordinateur de l’utilisateur répond aux exigences de la stratégie de contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="b758c-113">Ongoing compliance: Permits access to the network as long as the user's computer meets health policy requirements.</span></span>

<span data-ttu-id="b758c-114">Windows XP avec Service Pack 3 (SP3), Windows Vista et Windows Server 2008 fournissent des méthodes de contrainte de mise en conformité NAP pour la configuration des adresses DHCP (Dynamic Host Configuration Protocol), les connexions de réseau privé virtuel (VPN) basées sur l’accès à distance, les connexions câblées et sans fil authentifiées par IEEE 802.1 X et les communications basées sur la sécurité du protocole Internet.</span><span class="sxs-lookup"><span data-stu-id="b758c-114">Windows XP with Service Pack 3 (SP3), Windows Vista, and Windows Server 2008 provide NAP enforcement methods for Dynamic Host Configuration Protocol (DHCP) address configuration, remote access-based virtual private network (VPN) connections, IEEE 802.1X-authenticated wired and wireless connections, and Internet Protocol security (IPsec)-based communications.</span></span> <span data-ttu-id="b758c-115">En outre, la plateforme NAP prend en charge une architecture via laquelle la validation d’intégrité, la restriction réseau, la mise à jour et la conformité continue sont prises en charge par des composants supplémentaires qui peuvent être fournis par des éditeurs de logiciels tiers ou par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b758c-115">The NAP platform additionally supports an architecture through which health validation, network restriction, remediation, and ongoing compliance are supported by additional components that can be supplied by third-party software vendors or by Microsoft.</span></span>

<span data-ttu-id="b758c-116">La plateforme NAP comprend les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="b758c-116">The NAP platform includes the following components:</span></span>

-   [<span data-ttu-id="b758c-117">Architecture du client NAP</span><span class="sxs-lookup"><span data-stu-id="b758c-117">NAP Client Architecture</span></span>](nap-client-architecture.md)
-   [<span data-ttu-id="b758c-118">Architecture côté serveur NAP</span><span class="sxs-lookup"><span data-stu-id="b758c-118">NAP Server-side Architecture</span></span>](nap-server-side-architecture.md)
-   [<span data-ttu-id="b758c-119">Communication entre le client NAP et le composant côté serveur</span><span class="sxs-lookup"><span data-stu-id="b758c-119">NAP Client and Server-side Component Communication</span></span>](nap-client-and-server-side-component-communication.md)

<span data-ttu-id="b758c-120">Le client NAP requiert Windows Vista, Windows XP avec SP3 ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b758c-120">The NAP client requires Windows Vista, Windows XP with SP3, or Windows Server 2008.</span></span> <span data-ttu-id="b758c-121">Le serveur de stratégie de contrôle d’intégrité NAP et les points de contrainte de mise en conformité NAP pour la contrainte DHCP, VPN et IPsec nécessitent Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b758c-121">The NAP health policy server and NAP enforcement points for DHCP, VPN, and IPsec enforcement require Windows Server 2008.</span></span>

 

 





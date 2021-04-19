---
description: La stratégie de ticket Kerberos est définie au niveau du domaine et implémentée par le centre de distribution de clés du domaine (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Stratégie Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531989"
---
# <a name="kerberos-policy"></a><span data-ttu-id="cee3e-103">Stratégie Kerberos</span><span class="sxs-lookup"><span data-stu-id="cee3e-103">Kerberos Policy</span></span>

<span data-ttu-id="cee3e-104">La stratégie de ticket Kerberos est définie au niveau du domaine et implémentée par le [*Centre de distribution de clés*](../secgloss/k-gly.md) du domaine (KDC).</span><span class="sxs-lookup"><span data-stu-id="cee3e-104">Kerberos ticket policy is defined at the domain level and implemented by the domain's [*Key Distribution Center*](../secgloss/k-gly.md) (KDC).</span></span> <span data-ttu-id="cee3e-105">La stratégie Kerberos est stockée dans le Active Directory en tant que sous-ensemble des attributs de la stratégie de sécurité du domaine.</span><span class="sxs-lookup"><span data-stu-id="cee3e-105">Kerberos policy is stored in the Active Directory as a subset of the attributes of domain security policy.</span></span> <span data-ttu-id="cee3e-106">Par défaut, les options de stratégie peuvent être définies uniquement par les membres du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="cee3e-106">By default, policy options can be set only by members of the Domain Administrators group.</span></span> <span data-ttu-id="cee3e-107">La stratégie de domaine comprend des options qui :</span><span class="sxs-lookup"><span data-stu-id="cee3e-107">Domain policy includes options that:</span></span>

-   <span data-ttu-id="cee3e-108">Prise en charge des tickets postdatés</span><span class="sxs-lookup"><span data-stu-id="cee3e-108">Support postdated tickets</span></span>
-   <span data-ttu-id="cee3e-109">Prendre en charge la délégation avec restriction (Windows Server 2003 uniquement)</span><span class="sxs-lookup"><span data-stu-id="cee3e-109">Support constrained delegation (Windows Server 2003 only)</span></span>
-   <span data-ttu-id="cee3e-110">Tickets de support qui peuvent être transférés</span><span class="sxs-lookup"><span data-stu-id="cee3e-110">Support tickets that can be forwarded</span></span>
-   <span data-ttu-id="cee3e-111">Prendre en charge les tickets renouvelés</span><span class="sxs-lookup"><span data-stu-id="cee3e-111">Support renewable tickets</span></span>
-   <span data-ttu-id="cee3e-112">Définir l’âge maximal du ticket</span><span class="sxs-lookup"><span data-stu-id="cee3e-112">Set maximum ticket age</span></span>
-   <span data-ttu-id="cee3e-113">Définir l’âge de renouvellement maximal</span><span class="sxs-lookup"><span data-stu-id="cee3e-113">Set maximum renewal age</span></span>
-   <span data-ttu-id="cee3e-114">Définir l’âge maximal du ticket proxy</span><span class="sxs-lookup"><span data-stu-id="cee3e-114">Set maximum proxy ticket age</span></span>
-   <span data-ttu-id="cee3e-115">Déconnecter de force les utilisateurs lorsque les tickets expirent</span><span class="sxs-lookup"><span data-stu-id="cee3e-115">Forcibly log off users when tickets expire</span></span>

<span data-ttu-id="cee3e-116">Avec la [*délégation avec restriction*](../secgloss/c-gly.md), un ordinateur peut être configuré pour autoriser le transfert des informations d’identification uniquement vers une liste spécifique de services.</span><span class="sxs-lookup"><span data-stu-id="cee3e-116">With [*constrained delegation*](../secgloss/c-gly.md), a computer can be set to allow forwarding of credentials only to a specific list of services.</span></span> <span data-ttu-id="cee3e-117">Ces services doivent se trouver dans le même domaine que l’ordinateur qui transfère les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cee3e-117">Those services must reside in the same domain as the computer forwarding the credentials.</span></span> <span data-ttu-id="cee3e-118">Sous la *délégation avec restriction*, les tickets ne sont plus envoyés du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="cee3e-118">Under *constrained delegation*, tickets are no longer sent from the client to the server.</span></span> <span data-ttu-id="cee3e-119">L’ordinateur serveur crée des tickets de service pour transférer les informations utilisées pour authentifier le client, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cee3e-119">The server computer creates service tickets to forward as necessary from information used to authenticate the client.</span></span>

<span data-ttu-id="cee3e-120">Bien que la stratégie Kerberos pour un domaine puisse autoriser l’authentification déléguée en autorisant le transfert de tickets, cet aspect de la stratégie ne doit pas s’appliquer à tous les utilisateurs ou à tous les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="cee3e-120">Although Kerberos policy for a domain may permit delegated authentication by allowing tickets to be forwarded, that aspect of policy need not apply to all users or all computers.</span></span> <span data-ttu-id="cee3e-121">Un attribut d’un compte d’utilisateur individuel peut être défini pour désactiver le transfert des [*informations d’identification*](../secgloss/c-gly.md) de cet utilisateur par n’importe quel serveur.</span><span class="sxs-lookup"><span data-stu-id="cee3e-121">An attribute of an individual user account can be set to disable forwarding of that user's [*credentials*](../secgloss/c-gly.md) by any server.</span></span> <span data-ttu-id="cee3e-122">Un attribut du compte d’un ordinateur individuel peut être défini pour désactiver le transfert des informations d’identification de n’importe quel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cee3e-122">An attribute of an individual computer's account can be set to disable forwarding of credentials from any user.</span></span> <span data-ttu-id="cee3e-123">Dans les deux cas, la délégation peut être désactivée en créant une stratégie de groupe à appliquer à tous les utilisateurs ou à tous les ordinateurs d’une unité d’organisation du Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cee3e-123">In both cases, delegation can be disabled by creating a group policy to apply to all users or all computers in an organizational unit of the Active Directory.</span></span>

<span data-ttu-id="cee3e-124">**Windows XP/2000 :** La délégation avec restriction n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cee3e-124">**Windows XP/2000:** Constrained delegation is not supported.</span></span>

 

 

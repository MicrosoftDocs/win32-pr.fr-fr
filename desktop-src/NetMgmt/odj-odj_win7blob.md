---
title: ODJ_WIN7BLOB
description: Définition du ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104316704"
---
# <a name="odj_win7blob-structure"></a><span data-ttu-id="93e80-103">Structure ODJ_WIN7BLOB</span><span class="sxs-lookup"><span data-stu-id="93e80-103">ODJ_WIN7BLOB structure</span></span>

<span data-ttu-id="93e80-104">Contient les informations de base requises pour joindre un client à un domaine.</span><span class="sxs-lookup"><span data-stu-id="93e80-104">Contains the basic information required to join a client to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e80-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93e80-105">Syntax</span></span>

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a><span data-ttu-id="93e80-106">Membres</span><span class="sxs-lookup"><span data-stu-id="93e80-106">Members</span></span>

### <a name="lpdomain"></a><span data-ttu-id="93e80-107">lpDomain</span><span class="sxs-lookup"><span data-stu-id="93e80-107">lpDomain</span></span>

<span data-ttu-id="93e80-108">Doit être défini sur le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="93e80-108">Must be set to the domain name.</span></span>

### <a name="lpmachinename"></a><span data-ttu-id="93e80-109">lpMachineName</span><span class="sxs-lookup"><span data-stu-id="93e80-109">lpMachineName</span></span>

<span data-ttu-id="93e80-110">Doit être défini sur le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="93e80-110">Must be set to the machine name.</span></span>

### <a name="lpmachinepassword"></a><span data-ttu-id="93e80-111">lpMachinePassword</span><span class="sxs-lookup"><span data-stu-id="93e80-111">lpMachinePassword</span></span>

<span data-ttu-id="93e80-112">Doit être défini sur un mot de passe en texte clair pour le compte d’ordinateur identifié par lpMachineName</span><span class="sxs-lookup"><span data-stu-id="93e80-112">Must be set to a cleartext password for the machine account identified by lpMachineName</span></span>

### <a name="dnsdomaininfo"></a><span data-ttu-id="93e80-113">DnsDomainInfo</span><span class="sxs-lookup"><span data-stu-id="93e80-113">DnsDomainInfo</span></span>

<span data-ttu-id="93e80-114">Contient des informations sur le domaine qui est joint.</span><span class="sxs-lookup"><span data-stu-id="93e80-114">Contains information about the domain being joined.</span></span>

### <a name="dcinfo"></a><span data-ttu-id="93e80-115">DcInfo</span><span class="sxs-lookup"><span data-stu-id="93e80-115">DcInfo</span></span>

<span data-ttu-id="93e80-116">Contient les informations d’attribution de noms et d’adressage relatives au contrôleur de domaine qui a été utilisé pour créer le compte d’ordinateur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93e80-116">Contains naming and addressing information about the domain controller that was used to create the machine account Active Directory.</span></span>

### <a name="options"></a><span data-ttu-id="93e80-117">Options</span><span class="sxs-lookup"><span data-stu-id="93e80-117">Options</span></span>

<span data-ttu-id="93e80-118">Doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="93e80-118">Must be set to zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="93e80-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93e80-119">See also</span></span>

[<span data-ttu-id="93e80-120">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="93e80-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="93e80-121">**\_ \_ \_ informations sur le domaine \_ DNS de la stratégie ODJ**</span><span class="sxs-lookup"><span data-stu-id="93e80-121">**ODJ\_POLICY\_DNS\_DOMAIN\_INFO**</span></span>](odj-odj_policy_dns_domain_info.md)

[<span data-ttu-id="93e80-122">**DOMAIN_CONTROLLER_INFOW**</span><span class="sxs-lookup"><span data-stu-id="93e80-122">**DOMAIN_CONTROLLER_INFOW**</span></span>](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)




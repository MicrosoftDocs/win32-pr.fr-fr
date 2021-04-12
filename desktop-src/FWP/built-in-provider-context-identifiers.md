---
title: Identificateurs de contexte fournisseur intégrés (Fwpmu. h)
description: Les contextes de fournisseur intégrés identifient les stratégies par défaut à utiliser avec les sockets sécurisés.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464234"
---
# <a name="built-in-provider-context-identifiers"></a><span data-ttu-id="a67d7-103">Identificateurs de contexte fournisseur intégrés</span><span class="sxs-lookup"><span data-stu-id="a67d7-103">Built-in Provider Context Identifiers</span></span>

<span data-ttu-id="a67d7-104">Les identificateurs des contextes de fournisseur intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.</span><span class="sxs-lookup"><span data-stu-id="a67d7-104">The identifiers for the provider contexts that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="a67d7-105">Ces contextes de fournisseur intégrés identifient les stratégies par défaut à utiliser avec les sockets sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a67d7-105">These built-in provider contexts identify the default policies to use with secure sockets.</span></span>

<span data-ttu-id="a67d7-106">Ces identificateurs sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="a67d7-106">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="a67d7-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**contexte du fournisseur FWPM de \_ \_ \_ \_ Socket sécurisé \_ AUTHIP**</span><span class="sxs-lookup"><span data-stu-id="a67d7-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a67d7-108">Stratégie par défaut en mode principal protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP) pour les sockets sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a67d7-108">Authenticated Internet Protocol (AuthIP) main mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a67d7-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_contexte du fournisseur FWPM \_ \_ \_ IPSec Socket sécurisé \_**</span><span class="sxs-lookup"><span data-stu-id="a67d7-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a67d7-110">Stratégie par défaut du mode rapide IPsec (Internet Protocol Security) pour les sockets sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a67d7-110">Internet Protocol Security (IPsec) quick mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a67d7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a67d7-111">Requirements</span></span>



| <span data-ttu-id="a67d7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a67d7-112">Requirement</span></span> | <span data-ttu-id="a67d7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a67d7-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a67d7-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a67d7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a67d7-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a67d7-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a67d7-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a67d7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a67d7-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a67d7-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a67d7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="a67d7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a67d7-119"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="a67d7-119"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






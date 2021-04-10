---
title: Les appels distants au protocole SAM RPC sont limités aux seuls administrateurs locaux
description: Le protocole SAM RPC est limité. Cela signifie que seuls les membres du groupe Administrateurs local peuvent effectuer des appels distants par rapport aux méthodes de ce protocole. Active Directory comportement du contrôleur de domaine n’est pas affecté.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100817"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a><span data-ttu-id="70699-105">Les appels distants au protocole SAM RPC sont limités aux seuls administrateurs locaux</span><span class="sxs-lookup"><span data-stu-id="70699-105">Remote calls to the SAM RPC protocol are restricted to only local administrators</span></span>

<span data-ttu-id="70699-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="70699-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="70699-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="70699-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="70699-108">Le protocole SAM RPC est limité.</span><span class="sxs-lookup"><span data-stu-id="70699-108">The SAM RPC protocol is being restricted.</span></span> <span data-ttu-id="70699-109">Cela signifie que seuls les membres du groupe Administrateurs local peuvent effectuer des appels distants par rapport aux méthodes de ce protocole.</span><span class="sxs-lookup"><span data-stu-id="70699-109">This means that only members of the local Administrator group can make remote calls against methods in this protocol.</span></span> <span data-ttu-id="70699-110">Active Directory comportement du contrôleur de domaine n’est pas affecté.</span><span class="sxs-lookup"><span data-stu-id="70699-110">Active Directory domain controller behavior is unaffected.</span></span>

## <a name="mitigations"></a><span data-ttu-id="70699-111">Corrections</span><span class="sxs-lookup"><span data-stu-id="70699-111">Mitigations</span></span>

<span data-ttu-id="70699-112">Vérifiez que les utilisateurs appropriés sont définis en tant qu’administrateurs sur le PC.</span><span class="sxs-lookup"><span data-stu-id="70699-112">Ensure that the right users are set as administrators on the PC.</span></span> <span data-ttu-id="70699-113">La liste de contrôle d’accès utilisée pour la vérification d’accès est configurable via la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="70699-113">The ACL used for the access check is configurable via group policy.</span></span>

 

 





---
title: BypassNegotiation
description: La clé de Registre BypassNegotiation détermine si la négociation des fonctionnalités entre le serveur et le client se produit ou si des paramètres préconfigurés sont utilisés.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381289"
---
# <a name="bypassnegotiation"></a><span data-ttu-id="2512a-103">BypassNegotiation</span><span class="sxs-lookup"><span data-stu-id="2512a-103">BypassNegotiation</span></span>

<span data-ttu-id="2512a-104">La clé de Registre BypassNegotiation détermine si la négociation des fonctionnalités entre le serveur et le client se produit ou si des paramètres préconfigurés sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="2512a-104">The BypassNegotiation registry key determines if capabilities negotiation between the server and client occurs or if pre-configured settings are used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2512a-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="2512a-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a><span data-ttu-id="2512a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="2512a-106">Remarks</span></span>

<span data-ttu-id="2512a-107">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2512a-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="2512a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2512a-108">Value</span></span>   | <span data-ttu-id="2512a-109">Description</span><span class="sxs-lookup"><span data-stu-id="2512a-109">Description</span></span>                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2512a-110">0</span><span class="sxs-lookup"><span data-stu-id="2512a-110">0</span></span>       | <span data-ttu-id="2512a-111">Serveurs et clients négocient les fonctionnalités EAP.</span><span class="sxs-lookup"><span data-stu-id="2512a-111">Server and client negotiate EAP capabilities.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2512a-112">différente</span><span class="sxs-lookup"><span data-stu-id="2512a-112">nonzero</span></span> | <span data-ttu-id="2512a-113">Le serveur et le client ne négocient pas les fonctionnalités EAP.</span><span class="sxs-lookup"><span data-stu-id="2512a-113">Server and client do not negotiate EAP capabilities.</span></span> <span data-ttu-id="2512a-114">Le serveur et le client utilisent la valeur de clé de Registre [AssumePhase2Fragmentation](assumephase2fragmentation.md) pour rechercher les fonctionnalités de l’autre partie.</span><span class="sxs-lookup"><span data-stu-id="2512a-114">Server and client use the [AssumePhase2Fragmentation](assumephase2fragmentation.md) registry key value to find the other party's capabilities.</span></span> |



 

<span data-ttu-id="2512a-115">Si cette valeur de Registre n’est pas présente, le serveur et le client négocient les fonctionnalités EAP.</span><span class="sxs-lookup"><span data-stu-id="2512a-115">If this registry value is not present, the server and client negotiate EAP capabilities..</span></span>

## <a name="related-topics"></a><span data-ttu-id="2512a-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2512a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2512a-117">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="2512a-117">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 





---
title: AssumePhase2Fragmentation
description: La clé de Registre AssumePhase2Fragmentation détermine si le serveur et le client supposent la fragmentation de la phase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381271"
---
# <a name="assumephase2fragmentation"></a><span data-ttu-id="d3a40-103">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="d3a40-103">AssumePhase2Fragmentation</span></span>

<span data-ttu-id="d3a40-104">La clé de Registre AssumePhase2Fragmentation détermine si le serveur et le client supposent la fragmentation de la phase 2.</span><span class="sxs-lookup"><span data-stu-id="d3a40-104">The AssumePhase2Fragmentation registry key determines if the server and client assume phase 2 fragmentation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d3a40-105">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="d3a40-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a><span data-ttu-id="d3a40-106">Notes</span><span class="sxs-lookup"><span data-stu-id="d3a40-106">Remarks</span></span>

<span data-ttu-id="d3a40-107">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d3a40-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="d3a40-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3a40-108">Value</span></span>   | <span data-ttu-id="d3a40-109">Description</span><span class="sxs-lookup"><span data-stu-id="d3a40-109">Description</span></span>                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a40-110">0</span><span class="sxs-lookup"><span data-stu-id="d3a40-110">0</span></span>       | <span data-ttu-id="d3a40-111">Le serveur et le client supposent que l’autre partie n’est pas en charge de la fragmentation de phase 2 pendant l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="d3a40-111">Server and client assume the other party is not capable of phase 2 fragmentation during PEAP authentication.</span></span> |
| <span data-ttu-id="d3a40-112">différente</span><span class="sxs-lookup"><span data-stu-id="d3a40-112">nonzero</span></span> | <span data-ttu-id="d3a40-113">Le serveur et le client supposent que l’autre partie est en charge de la fragmentation de phase 2 pendant l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="d3a40-113">Server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>     |



 

<span data-ttu-id="d3a40-114">Si cette valeur de Registre n’est pas présente, le serveur et le client supposent que l’autre partie est en charge de la fragmentation de phase 2 pendant l’authentification PEAP.</span><span class="sxs-lookup"><span data-stu-id="d3a40-114">If this registry value is not present, the server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3a40-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3a40-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3a40-116">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="d3a40-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 





---
title: PreferredServerBitness
description: Définit l’architecture préférée, 32 bits ou 64 bits, pour ce serveur COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valeur de Registre PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316547"
---
# <a name="preferredserverbitness"></a><span data-ttu-id="35ae3-104">PreferredServerBitness</span><span class="sxs-lookup"><span data-stu-id="35ae3-104">PreferredServerBitness</span></span>

<span data-ttu-id="35ae3-105">Définit l’architecture préférée, 32 bits ou 64 bits, pour ce serveur COM.</span><span class="sxs-lookup"><span data-stu-id="35ae3-105">Sets the preferred architecture, 32-bit or 64-bit, for this COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="35ae3-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="35ae3-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a><span data-ttu-id="35ae3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="35ae3-107">Remarks</span></span>

<span data-ttu-id="35ae3-108">Il s’agit d’une valeur **reg \_ DWORD** qui est uniquement disponible sur les versions 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="35ae3-108">This is a **REG\_DWORD** value that is available only on 64-bit versions of Windows.</span></span>



| <span data-ttu-id="35ae3-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ae3-109">Value</span></span> | <span data-ttu-id="35ae3-110">Description</span><span class="sxs-lookup"><span data-stu-id="35ae3-110">Description</span></span>                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ae3-111">1</span><span class="sxs-lookup"><span data-stu-id="35ae3-111">1</span></span>     | <span data-ttu-id="35ae3-112">Faire correspondre l’architecture du serveur à l’architecture du client.</span><span class="sxs-lookup"><span data-stu-id="35ae3-112">Match the server architecture to the client architecture.</span></span> <span data-ttu-id="35ae3-113">Par exemple, si le client est 32 bits, utilisez une version 32 bits du serveur, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="35ae3-113">For example, if the client is 32-bit, use a 32-bit version of the server, if it is available.</span></span> <span data-ttu-id="35ae3-114">Si ce n’est pas le cas, la demande d’activation du client échoue.</span><span class="sxs-lookup"><span data-stu-id="35ae3-114">If not, the client's activation request will fail.</span></span> |
| <span data-ttu-id="35ae3-115">2</span><span class="sxs-lookup"><span data-stu-id="35ae3-115">2</span></span>     | <span data-ttu-id="35ae3-116">Utilisez une version 32 bits du serveur.</span><span class="sxs-lookup"><span data-stu-id="35ae3-116">Use a 32-bit version of the server.</span></span> <span data-ttu-id="35ae3-117">S’il n’en existe pas, la demande d’activation du client échoue.</span><span class="sxs-lookup"><span data-stu-id="35ae3-117">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |
| <span data-ttu-id="35ae3-118">3</span><span class="sxs-lookup"><span data-stu-id="35ae3-118">3</span></span>     | <span data-ttu-id="35ae3-119">Utilisez une version 64 bits du serveur.</span><span class="sxs-lookup"><span data-stu-id="35ae3-119">Use a 64-bit version of the server.</span></span> <span data-ttu-id="35ae3-120">S’il n’en existe pas, la demande d’activation du client échoue.</span><span class="sxs-lookup"><span data-stu-id="35ae3-120">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |



 

<span data-ttu-id="35ae3-121">Si cette valeur n’est pas présente, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="35ae3-121">If this value is not present, then:</span></span>

-   <span data-ttu-id="35ae3-122">Si l’ordinateur qui héberge le serveur exécute Windows XP ou Windows Server 2003 sans SP1 ou version ultérieure, COM préfère une version 64 bits du serveur si elle est disponible ; dans le cas contraire, elle activera une version 32 bits du serveur.</span><span class="sxs-lookup"><span data-stu-id="35ae3-122">If the computer that hosts the server is running Windows XP or Windows Server 2003 without SP1 or later installed, then COM will prefer a 64-bit version of the server if available; otherwise it will activate a 32-bit version of the server.</span></span>
-   <span data-ttu-id="35ae3-123">Si l’ordinateur qui héberge le serveur exécute Windows Server 2003 avec SP1 ou une version ultérieure, COM essaiera de faire correspondre l’architecture du serveur à l’architecture du client.</span><span class="sxs-lookup"><span data-stu-id="35ae3-123">If the computer that hosts the server is running Windows Server 2003 with SP1 or later installed, then COM will try to match the server architecture to the client architecture.</span></span> <span data-ttu-id="35ae3-124">En d’autres termes, pour un client 32 bits, COM activera un serveur 32 bits s’il est disponible ; dans le cas contraire, elle activera une version 64 bits du serveur.</span><span class="sxs-lookup"><span data-stu-id="35ae3-124">In other words, for a 32-bit client, COM will activate a 32-bit server if available; otherwise it will activate a 64-bit version of the server.</span></span> <span data-ttu-id="35ae3-125">Pour un client 64 bits, COM activera un serveur 64 bits s’il est disponible ; dans le cas contraire, il activera un serveur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="35ae3-125">For a 64-bit client, COM will activate a 64-bit server if available; otherwise it will activate a 32-bit server.</span></span>

<span data-ttu-id="35ae3-126">Le client peut également spécifier sa propre architecture à l’aide des \_ indicateurs CLSCTX activate \_ 32 \_ bit \_ Server et CLSCTX \_ Activate \_ 64 \_ bit Server \_ , et ceux-ci remplacent les préférences du serveur.</span><span class="sxs-lookup"><span data-stu-id="35ae3-126">The client can also specify its own architecture preference via the CLSCTX\_ACTIVATE\_32\_BIT\_SERVER and CLSCTX\_ACTIVATE\_64\_BIT\_SERVER flags, and these will override the server's preference.</span></span> <span data-ttu-id="35ae3-127">Pour plus d’informations et pour obtenir un graphique des interactions possibles entre les préférences de l’architecture du client et du serveur, consultez [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span><span class="sxs-lookup"><span data-stu-id="35ae3-127">For more information, and a chart of possible interactions between client and server architecture preferences, see [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="35ae3-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35ae3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35ae3-129">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="35ae3-129">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 
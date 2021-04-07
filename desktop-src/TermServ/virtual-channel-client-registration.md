---
title: Inscription du client du canal virtuel
description: Vous devez stocker le nom de la DLL cliente dans le registre.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727893"
---
# <a name="virtual-channel-client-registration"></a><span data-ttu-id="4785b-103">Inscription du client du canal virtuel</span><span class="sxs-lookup"><span data-stu-id="4785b-103">Virtual Channel Client Registration</span></span>

<span data-ttu-id="4785b-104">Vous devez stocker le nom de la DLL cliente dans le registre.</span><span class="sxs-lookup"><span data-stu-id="4785b-104">You must store the name of the client DLL in the registry.</span></span>

<span data-ttu-id="4785b-105">Dans le registre, ajoutez une sous-clé à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="4785b-105">In the registry, add a subkey to one of the following locations:</span></span>

<span data-ttu-id="4785b-106">**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** par défaut du client Microsoft Terminal Server du logiciel utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="4785b-106">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**Addins**</span></span>

<span data-ttu-id="4785b-107">**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** de connexion client Microsoft Terminal Server du logiciel utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="4785b-107">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**connection**\\**Addins**</span></span>

> [!Note]  
> <span data-ttu-id="4785b-108">Dans le chemin d’accès du Registre, la *connexion* représente le nom d’une connexion dans le gestionnaire de connexions.</span><span class="sxs-lookup"><span data-stu-id="4785b-108">In the registry path, *connection* represents the name of a connection in Connection Manager.</span></span>

 

<span data-ttu-id="4785b-109">Les entrées sous la clé de **\\ \\ compléments par défaut** s’appliquent à toutes les connexions.</span><span class="sxs-lookup"><span data-stu-id="4785b-109">Entries under the **\\Default\\Addins** key apply to all connections.</span></span> <span data-ttu-id="4785b-110">Les entrées sous la clé de **\\  \\ compléments de connexion** s’appliquent uniquement à la connexion identifiée par la *connexion*.</span><span class="sxs-lookup"><span data-stu-id="4785b-110">Entries under the **\\***connection***\\Addins** key apply only to the connection identified by *connection*.</span></span> <span data-ttu-id="4785b-111">Les connexions peuvent être créées et gérées à l’aide du gestionnaire de connexions.</span><span class="sxs-lookup"><span data-stu-id="4785b-111">Connections can be created and managed by using Connection Manager.</span></span>

<span data-ttu-id="4785b-112">Vous pouvez attribuer n’importe quel nom à la sous-clé.</span><span class="sxs-lookup"><span data-stu-id="4785b-112">The subkey can be given any name.</span></span> <span data-ttu-id="4785b-113">Il doit contenir une valeur SZ **reg \_** ou **reg \_ expand \_** et peut éventuellement contenir une valeur **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="4785b-113">It must contain a **REG\_SZ** or **REG\_EXPAND\_SZ** value and may optionally contain a **REG\_DWORD** value.</span></span> <span data-ttu-id="4785b-114">La syntaxe de la valeur de **reg \_ SZ** ou **reg \_ expand \_** est la suivante.</span><span class="sxs-lookup"><span data-stu-id="4785b-114">The syntax of the **REG\_SZ** or **REG\_EXPAND\_SZ** value is as follows.</span></span>

``` syntax
Name = DLLname
```

<span data-ttu-id="4785b-115">Si **Name** est une valeur de **reg \_ expand \_ SZ** , il peut contenir des variables d’environnement non développées qui sont développées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4785b-115">If **Name** is a **REG\_EXPAND\_SZ** value, it can contain unexpanded environment variables that are expanded at runtime.</span></span>

<span data-ttu-id="4785b-116">La valeur de *DLLname* peut être un chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="4785b-116">The value of *DLLname* can be a fully qualified path.</span></span> <span data-ttu-id="4785b-117">Si *DLLname* ne contient pas de chemin d’accès, la stratégie de recherche de dll standard est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4785b-117">If *DLLname* does not contain a path, the standard DLL search strategy is used.</span></span> <span data-ttu-id="4785b-118">Pour plus d’informations, consultez la section Notes pour [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="4785b-118">For more information, see the Remarks section for [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

 

 
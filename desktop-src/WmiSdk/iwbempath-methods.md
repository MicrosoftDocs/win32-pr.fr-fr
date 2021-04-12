---
description: L’interface IWbemPath expose les méthodes suivantes.
ms.assetid: 36EC7EF6-5CCA-4D18-AB09-9EE41D1B9524
ms.tgt_platform: multiple
title: Méthodes IWbemPath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ae802fd7741e5b1317160991a50bd2a535a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202287"
---
# <a name="iwbempath-methods"></a><span data-ttu-id="d1374-103">Méthodes IWbemPath</span><span class="sxs-lookup"><span data-stu-id="d1374-103">IWbemPath Methods</span></span>

<span data-ttu-id="d1374-104">L’interface [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1374-104">The [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d1374-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d1374-105">In this section</span></span>

-   [<span data-ttu-id="d1374-106">**Méthode CreateClassPart**</span><span class="sxs-lookup"><span data-stu-id="d1374-106">**CreateClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-createclasspart)
-   [<span data-ttu-id="d1374-107">**Méthode DeleteClassPart**</span><span class="sxs-lookup"><span data-stu-id="d1374-107">**DeleteClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-deleteclasspart)
-   [<span data-ttu-id="d1374-108">**Méthode GetClassName**</span><span class="sxs-lookup"><span data-stu-id="d1374-108">**GetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getclassname)
-   [<span data-ttu-id="d1374-109">**GetInfo, méthode**</span><span class="sxs-lookup"><span data-stu-id="d1374-109">**GetInfo method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getinfo)
-   [<span data-ttu-id="d1374-110">**Méthode GetKeyList**</span><span class="sxs-lookup"><span data-stu-id="d1374-110">**GetKeyList method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getkeylist)
-   [<span data-ttu-id="d1374-111">**Méthode GetNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="d1374-111">**GetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespaceat)
-   [<span data-ttu-id="d1374-112">**Méthode GetNamespaceCount**</span><span class="sxs-lookup"><span data-stu-id="d1374-112">**GetNamespaceCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespacecount)
-   [<span data-ttu-id="d1374-113">**Méthode GetScope,**</span><span class="sxs-lookup"><span data-stu-id="d1374-113">**GetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscope)
-   [<span data-ttu-id="d1374-114">**Méthode GetScopeAsText**</span><span class="sxs-lookup"><span data-stu-id="d1374-114">**GetScopeAsText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopeastext)
-   [<span data-ttu-id="d1374-115">**Méthode GetScopeCount**</span><span class="sxs-lookup"><span data-stu-id="d1374-115">**GetScopeCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopecount)
-   [<span data-ttu-id="d1374-116">**Méthode GetServer**</span><span class="sxs-lookup"><span data-stu-id="d1374-116">**GetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getserver)
-   [<span data-ttu-id="d1374-117">**GetText (méthode)**</span><span class="sxs-lookup"><span data-stu-id="d1374-117">**GetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-gettext)
-   [<span data-ttu-id="d1374-118">**Méthode IsLocal**</span><span class="sxs-lookup"><span data-stu-id="d1374-118">**IsLocal method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-islocal)
-   [<span data-ttu-id="d1374-119">**Méthode IsRelative**</span><span class="sxs-lookup"><span data-stu-id="d1374-119">**IsRelative method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelative)
-   [<span data-ttu-id="d1374-120">**Méthode IsRelativeOrChild**</span><span class="sxs-lookup"><span data-stu-id="d1374-120">**IsRelativeOrChild method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelativeorchild)
-   [<span data-ttu-id="d1374-121">**Méthode IsSameClassName**</span><span class="sxs-lookup"><span data-stu-id="d1374-121">**IsSameClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-issameclassname)
-   [<span data-ttu-id="d1374-122">**Méthode RemoveAllNamespaces**</span><span class="sxs-lookup"><span data-stu-id="d1374-122">**RemoveAllNamespaces method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallnamespaces)
-   [<span data-ttu-id="d1374-123">**Méthode RemoveAllScopes**</span><span class="sxs-lookup"><span data-stu-id="d1374-123">**RemoveAllScopes method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallscopes)
-   [<span data-ttu-id="d1374-124">**Méthode RemoveNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="d1374-124">**RemoveNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removenamespaceat)
-   [<span data-ttu-id="d1374-125">**Méthode RemoveScope**</span><span class="sxs-lookup"><span data-stu-id="d1374-125">**RemoveScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removescope)
-   [<span data-ttu-id="d1374-126">**Méthode SetClassName**</span><span class="sxs-lookup"><span data-stu-id="d1374-126">**SetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setclassname)
-   [<span data-ttu-id="d1374-127">**Méthode SetNamespaceAt**</span><span class="sxs-lookup"><span data-stu-id="d1374-127">**SetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setnamespaceat)
-   [<span data-ttu-id="d1374-128">**Méthode SetScope**</span><span class="sxs-lookup"><span data-stu-id="d1374-128">**SetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setscope)
-   [<span data-ttu-id="d1374-129">**Méthode SetServer**</span><span class="sxs-lookup"><span data-stu-id="d1374-129">**SetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setserver)
-   [<span data-ttu-id="d1374-130">**SetText (méthode)**</span><span class="sxs-lookup"><span data-stu-id="d1374-130">**SetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-settext)

 

 




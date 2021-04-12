---
description: L’interface IWbemClassObject expose les méthodes suivantes.
ms.assetid: 20BF7775-89D9-4851-8561-EEBA398A0584
ms.tgt_platform: multiple
title: Méthodes IWbemClassObject
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825b3f15f17dca6dd0871bbcae3f531a90c90f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321010"
---
# <a name="iwbemclassobject-methods"></a><span data-ttu-id="5060f-103">Méthodes IWbemClassObject</span><span class="sxs-lookup"><span data-stu-id="5060f-103">IWbemClassObject Methods</span></span>

<span data-ttu-id="5060f-104">L’interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5060f-104">The [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5060f-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5060f-105">In this section</span></span>

-   [<span data-ttu-id="5060f-106">**Méthode BeginEnumeration**</span><span class="sxs-lookup"><span data-stu-id="5060f-106">**BeginEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)
-   [<span data-ttu-id="5060f-107">**Méthode BeginMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="5060f-107">**BeginMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginmethodenumeration)
-   [<span data-ttu-id="5060f-108">**Cloner une méthode**</span><span class="sxs-lookup"><span data-stu-id="5060f-108">**Clone method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)
-   [<span data-ttu-id="5060f-109">**CompareTo (méthode)**</span><span class="sxs-lookup"><span data-stu-id="5060f-109">**CompareTo method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-compareto)
-   [<span data-ttu-id="5060f-110">**Delete (méthode)**</span><span class="sxs-lookup"><span data-stu-id="5060f-110">**Delete method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)
-   [<span data-ttu-id="5060f-111">**Méthode DeleteMethod**</span><span class="sxs-lookup"><span data-stu-id="5060f-111">**DeleteMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-deletemethod)
-   [<span data-ttu-id="5060f-112">**Méthode EndEnumeration**</span><span class="sxs-lookup"><span data-stu-id="5060f-112">**EndEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration)
-   [<span data-ttu-id="5060f-113">**Méthode EndMethodEnumeration**</span><span class="sxs-lookup"><span data-stu-id="5060f-113">**EndMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endmethodenumeration)
-   [<span data-ttu-id="5060f-114">**Méthode d’extraction**</span><span class="sxs-lookup"><span data-stu-id="5060f-114">**Get method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)
-   [<span data-ttu-id="5060f-115">**GetMethod, méthode**</span><span class="sxs-lookup"><span data-stu-id="5060f-115">**GetMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)
-   [<span data-ttu-id="5060f-116">**Méthode GetMethodOrigin**</span><span class="sxs-lookup"><span data-stu-id="5060f-116">**GetMethodOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodorigin)
-   [<span data-ttu-id="5060f-117">**Méthode GetMethodQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="5060f-117">**GetMethodQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)
-   [<span data-ttu-id="5060f-118">**Méthode GetNames**</span><span class="sxs-lookup"><span data-stu-id="5060f-118">**GetNames method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getnames)
-   [<span data-ttu-id="5060f-119">**Méthode GetObjectText**</span><span class="sxs-lookup"><span data-stu-id="5060f-119">**GetObjectText method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   [<span data-ttu-id="5060f-120">**Méthode GetPropertyOrigin**</span><span class="sxs-lookup"><span data-stu-id="5060f-120">**GetPropertyOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyorigin)
-   [<span data-ttu-id="5060f-121">**Méthode GetPropertyQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="5060f-121">**GetPropertyQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)
-   [<span data-ttu-id="5060f-122">**Méthode GetQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="5060f-122">**GetQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)
-   [<span data-ttu-id="5060f-123">**Méthode InheritsFrom**</span><span class="sxs-lookup"><span data-stu-id="5060f-123">**InheritsFrom method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-inheritsfrom)
-   [<span data-ttu-id="5060f-124">**Next, méthode**</span><span class="sxs-lookup"><span data-stu-id="5060f-124">**Next method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-next)
-   [<span data-ttu-id="5060f-125">**Méthode NextMethod**</span><span class="sxs-lookup"><span data-stu-id="5060f-125">**NextMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-nextmethod)
-   [<span data-ttu-id="5060f-126">**Méthode put**</span><span class="sxs-lookup"><span data-stu-id="5060f-126">**Put method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
-   [<span data-ttu-id="5060f-127">**Méthode PutMethod**</span><span class="sxs-lookup"><span data-stu-id="5060f-127">**PutMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)
-   [<span data-ttu-id="5060f-128">**Méthode SpawnDerivedClass**</span><span class="sxs-lookup"><span data-stu-id="5060f-128">**SpawnDerivedClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)
-   [<span data-ttu-id="5060f-129">**Méthode SpawnInstance**</span><span class="sxs-lookup"><span data-stu-id="5060f-129">**SpawnInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

 

 




---
description: L’interface IWbemServices expose les méthodes suivantes.
ms.assetid: B4A2048E-6C2F-43E0-97BD-E6D37D8E4657
ms.tgt_platform: multiple
title: IWbemServices, méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a960ec223d16bd9258ba2d9d56518d88beab50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533650"
---
# <a name="iwbemservices-methods"></a><span data-ttu-id="61fdb-103">IWbemServices, méthodes</span><span class="sxs-lookup"><span data-stu-id="61fdb-103">IWbemServices Methods</span></span>

<span data-ttu-id="61fdb-104">L’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="61fdb-104">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61fdb-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="61fdb-105">In this section</span></span>

-   [<span data-ttu-id="61fdb-106">**Méthode CancelAsyncCall**</span><span class="sxs-lookup"><span data-stu-id="61fdb-106">**CancelAsyncCall method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)
-   [<span data-ttu-id="61fdb-107">**Méthode CreateClassEnum**</span><span class="sxs-lookup"><span data-stu-id="61fdb-107">**CreateClassEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)
-   [<span data-ttu-id="61fdb-108">**Méthode CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-108">**CreateClassEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="61fdb-109">**CreateInstanceEnum, méthode**</span><span class="sxs-lookup"><span data-stu-id="61fdb-109">**CreateInstanceEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)
-   [<span data-ttu-id="61fdb-110">**Méthode CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-110">**CreateInstanceEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="61fdb-111">**Méthode DeleteClass**</span><span class="sxs-lookup"><span data-stu-id="61fdb-111">**DeleteClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass)
-   [<span data-ttu-id="61fdb-112">**Méthode DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-112">**DeleteClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)
-   [<span data-ttu-id="61fdb-113">**DeleteInstance, méthode**</span><span class="sxs-lookup"><span data-stu-id="61fdb-113">**DeleteInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)
-   [<span data-ttu-id="61fdb-114">**Méthode DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-114">**DeleteInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="61fdb-115">**ExecMethod, méthode**</span><span class="sxs-lookup"><span data-stu-id="61fdb-115">**ExecMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
-   [<span data-ttu-id="61fdb-116">**ExecMethodAsync, méthode**</span><span class="sxs-lookup"><span data-stu-id="61fdb-116">**ExecMethodAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="61fdb-117">**Méthode ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="61fdb-117">**ExecNotificationQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
-   [<span data-ttu-id="61fdb-118">**Méthode ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-118">**ExecNotificationQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="61fdb-119">**ExecQuery, méthode**</span><span class="sxs-lookup"><span data-stu-id="61fdb-119">**ExecQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   [<span data-ttu-id="61fdb-120">**Méthode ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-120">**ExecQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="61fdb-121">**GetObject, méthode**</span><span class="sxs-lookup"><span data-stu-id="61fdb-121">**GetObject method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)
-   [<span data-ttu-id="61fdb-122">**GetObjectAsync, méthode**</span><span class="sxs-lookup"><span data-stu-id="61fdb-122">**GetObjectAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="61fdb-123">**Méthode OpenNamespace,**</span><span class="sxs-lookup"><span data-stu-id="61fdb-123">**OpenNamespace method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace)
-   [<span data-ttu-id="61fdb-124">**Méthode PutClass**</span><span class="sxs-lookup"><span data-stu-id="61fdb-124">**PutClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
-   [<span data-ttu-id="61fdb-125">**Méthode PutClassAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-125">**PutClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)
-   [<span data-ttu-id="61fdb-126">**Méthode PutInstance**</span><span class="sxs-lookup"><span data-stu-id="61fdb-126">**PutInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)
-   [<span data-ttu-id="61fdb-127">**Méthode PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="61fdb-127">**PutInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)
-   [<span data-ttu-id="61fdb-128">**Méthode QueryObjectSink**</span><span class="sxs-lookup"><span data-stu-id="61fdb-128">**QueryObjectSink method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-queryobjectsink)

 

 




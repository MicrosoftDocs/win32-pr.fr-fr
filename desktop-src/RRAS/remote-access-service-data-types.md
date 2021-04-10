---
title: Types de données du service d’accès à distance (RAS. h)
description: Les types de données suivants sont utilisés par l’API du service d’accès à distance.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942094"
---
# <a name="remote-access-service-data-types"></a><span data-ttu-id="0d698-105">Types de données du service d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="0d698-105">Remote Access Service Data Types</span></span>

<span data-ttu-id="0d698-106">Les types de données suivants sont utilisés par l’API du service d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="0d698-106">The following data types are used by the Remote Access Service API.</span></span>


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

<span data-ttu-id="0d698-107">**RASIPV4ADDR**</span><span class="sxs-lookup"><span data-stu-id="0d698-107">**RASIPV4ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="0d698-108">[**Dans \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) qui contient une adresse IPv4.</span><span class="sxs-lookup"><span data-stu-id="0d698-108">A [**in\_addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) that contains an IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="0d698-109">Pris en charge dans Windows Vista ou les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="0d698-109">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> <dt>

<span data-ttu-id="0d698-110">**RASIPV6ADDR**</span><span class="sxs-lookup"><span data-stu-id="0d698-110">**RASIPV6ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="0d698-111">[**In6 \_ addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) qui contient une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="0d698-111">A [**in6\_addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) that contains an IPv6 address.</span></span>

> [!Note]  
> <span data-ttu-id="0d698-112">Pris en charge dans Windows Vista ou les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="0d698-112">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d698-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d698-113">Requirements</span></span>



| <span data-ttu-id="0d698-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d698-114">Requirement</span></span> | <span data-ttu-id="0d698-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d698-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0d698-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d698-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0d698-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d698-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0d698-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d698-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0d698-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d698-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0d698-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d698-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d698-121"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d698-121"><dt>Ras.h</dt></span></span> </dl> |



 


---
title: TLS_HANDLE
description: Représente un handle vers un serveur de licences Bureau à distance.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740716"
---
# <a name="tls_handle"></a><span data-ttu-id="82975-104">\_handle TLS</span><span class="sxs-lookup"><span data-stu-id="82975-104">TLS\_HANDLE</span></span>

<span data-ttu-id="82975-105">Représente un handle vers un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="82975-105">Represents a handle to a Remote Desktop license server.</span></span> <span data-ttu-id="82975-106">Ce descripteur est retourné par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="82975-106">This handle is returned by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="82975-107">Ce type de données n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="82975-107">This data type has no associated header file.</span></span> <span data-ttu-id="82975-108">Pour l’utiliser, vous devez le définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="82975-108">To use it, you must define it yourself as shown in this topic.</span></span>

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="82975-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82975-109">Requirements</span></span>



| <span data-ttu-id="82975-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82975-110">Requirement</span></span> | <span data-ttu-id="82975-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="82975-111">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="82975-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82975-112">Minimum supported client</span></span><br/> | <span data-ttu-id="82975-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82975-113">Windows Vista</span></span><br/>       |
| <span data-ttu-id="82975-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82975-114">Minimum supported server</span></span><br/> | <span data-ttu-id="82975-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82975-115">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82975-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82975-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82975-117">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="82975-117">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="82975-118">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="82975-118">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

 






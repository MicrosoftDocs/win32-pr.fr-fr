---
description: La \_ structure d’adresse IPX fournit une adresse au niveau du protocole IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Structure de IPX_ADDRESS (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525869"
---
# <a name="ipx_address-structure"></a><span data-ttu-id="dc28a-103">\_Structure d’adresse IPX</span><span class="sxs-lookup"><span data-stu-id="dc28a-103">IPX\_ADDRESS structure</span></span>

<span data-ttu-id="dc28a-104">La structure d' **\_ adresse IPX** fournit une adresse au niveau du protocole IPX.</span><span class="sxs-lookup"><span data-stu-id="dc28a-104">The **IPX\_ADDRESS** structure provides an address at the IPX protocol level.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc28a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc28a-105">Syntax</span></span>


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="dc28a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="dc28a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc28a-107">**Sous-réseau**</span><span class="sxs-lookup"><span data-stu-id="dc28a-107">**Subnet**</span></span>
</dt> <dd>

<span data-ttu-id="dc28a-108">Identificateur du sous-réseau du réseau.</span><span class="sxs-lookup"><span data-stu-id="dc28a-108">Network subnet identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dc28a-109">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="dc28a-109">**Address**</span></span>
</dt> <dd>

<span data-ttu-id="dc28a-110">Identificateur de la carte réseau du sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="dc28a-110">Subnet NIC identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc28a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc28a-111">Requirements</span></span>



| <span data-ttu-id="dc28a-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc28a-112">Requirement</span></span> | <span data-ttu-id="dc28a-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc28a-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc28a-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc28a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dc28a-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc28a-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dc28a-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc28a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dc28a-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc28a-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dc28a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc28a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc28a-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc28a-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 





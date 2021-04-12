---
description: La structure d' \_ adresse IP Vines \_ est une adresse IP sur un réseau Vines.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Structure de VINES_IP_ADDRESS (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319494"
---
# <a name="vines_ip_address-structure"></a><span data-ttu-id="1159c-103">Structure d' \_ adresse IP Vines \_</span><span class="sxs-lookup"><span data-stu-id="1159c-103">VINES\_IP\_ADDRESS structure</span></span>

<span data-ttu-id="1159c-104">La structure d' **\_ \_ adresse IP Vines** est une adresse IP sur un réseau Vines.</span><span class="sxs-lookup"><span data-stu-id="1159c-104">The **VINES\_IP\_ADDRESS** structure is an IP address on a Vines network.</span></span>

## <a name="syntax"></a><span data-ttu-id="1159c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1159c-105">Syntax</span></span>


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="1159c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1159c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1159c-107">**NetID**</span><span class="sxs-lookup"><span data-stu-id="1159c-107">**NetID**</span></span>
</dt> <dd>

<span data-ttu-id="1159c-108">Identificateur d’un ordinateur spécifique sur un sous-réseau spécifique.</span><span class="sxs-lookup"><span data-stu-id="1159c-108">The identifier of a specific machine on a specific subnet.</span></span>

</dd> <dt>

<span data-ttu-id="1159c-109">**SubnetID**</span><span class="sxs-lookup"><span data-stu-id="1159c-109">**SubnetID**</span></span>
</dt> <dd>

<span data-ttu-id="1159c-110">Identificateur d’un sous-réseau spécifique sur l’ensemble du réseau.</span><span class="sxs-lookup"><span data-stu-id="1159c-110">The identifier of a specific subnet on the whole network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1159c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1159c-111">Requirements</span></span>



| <span data-ttu-id="1159c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1159c-112">Requirement</span></span> | <span data-ttu-id="1159c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1159c-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1159c-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1159c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1159c-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1159c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1159c-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1159c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1159c-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1159c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1159c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1159c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1159c-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1159c-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 





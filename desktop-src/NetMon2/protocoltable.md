---
description: La structure PROTOCOLTABLE contient une liste de protocoles.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: PROTOCOLTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541891"
---
# <a name="protocoltable-structure"></a><span data-ttu-id="70d21-103">PROTOCOLTABLE, structure</span><span class="sxs-lookup"><span data-stu-id="70d21-103">PROTOCOLTABLE structure</span></span>

<span data-ttu-id="70d21-104">La structure **PROTOCOLTABLE** contient une liste de protocoles.</span><span class="sxs-lookup"><span data-stu-id="70d21-104">The **PROTOCOLTABLE** structure contains a list of protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d21-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70d21-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a><span data-ttu-id="70d21-106">Membres</span><span class="sxs-lookup"><span data-stu-id="70d21-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="70d21-107">**nProtocols**</span><span class="sxs-lookup"><span data-stu-id="70d21-107">**nProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="70d21-108">Nombre de protocoles activés.</span><span class="sxs-lookup"><span data-stu-id="70d21-108">Number of protocols that are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="70d21-109">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="70d21-109">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="70d21-110">Tableau de handles vers les Protocoles activés.</span><span class="sxs-lookup"><span data-stu-id="70d21-110">Array of handles to enabled protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70d21-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70d21-111">Requirements</span></span>



| <span data-ttu-id="70d21-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70d21-112">Requirement</span></span> | <span data-ttu-id="70d21-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="70d21-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="70d21-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70d21-114">Minimum supported client</span></span><br/> | <span data-ttu-id="70d21-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70d21-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="70d21-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70d21-116">Minimum supported server</span></span><br/> | <span data-ttu-id="70d21-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70d21-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="70d21-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="70d21-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="70d21-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="70d21-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 





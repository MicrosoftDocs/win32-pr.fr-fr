---
description: La structure CONFIGUREDEXPERT associe un expert à ses données de configuration.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: CONFIGUREDEXPERT, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203057"
---
# <a name="configuredexpert-structure"></a><span data-ttu-id="efa73-103">CONFIGUREDEXPERT, structure</span><span class="sxs-lookup"><span data-stu-id="efa73-103">CONFIGUREDEXPERT structure</span></span>

<span data-ttu-id="efa73-104">La structure **CONFIGUREDEXPERT** associe un expert à ses données de configuration.</span><span class="sxs-lookup"><span data-stu-id="efa73-104">The **CONFIGUREDEXPERT** structure associates an expert with its configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efa73-105">Syntax</span></span>


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a><span data-ttu-id="efa73-106">Membres</span><span class="sxs-lookup"><span data-stu-id="efa73-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="efa73-107">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="efa73-107">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="efa73-108">Handle à un expert.</span><span class="sxs-lookup"><span data-stu-id="efa73-108">Handle to an expert.</span></span>

</dd> <dt>

<span data-ttu-id="efa73-109">**StartupFlags**</span><span class="sxs-lookup"><span data-stu-id="efa73-109">**StartupFlags**</span></span>
</dt> <dd>

<span data-ttu-id="efa73-110">Valeurs de l’indicateur de démarrage de l’expert.</span><span class="sxs-lookup"><span data-stu-id="efa73-110">Startup flag values of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="efa73-111">**pConfig**</span><span class="sxs-lookup"><span data-stu-id="efa73-111">**pConfig**</span></span>
</dt> <dd>

<span data-ttu-id="efa73-112">Pointeur vers une structure [**EXPERTCONFIG**](expertconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="efa73-112">Pointer to an [**EXPERTCONFIG**](expertconfig.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efa73-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efa73-113">Requirements</span></span>



| <span data-ttu-id="efa73-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efa73-114">Requirement</span></span> | <span data-ttu-id="efa73-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="efa73-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="efa73-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efa73-116">Minimum supported client</span></span><br/> | <span data-ttu-id="efa73-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efa73-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="efa73-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efa73-118">Minimum supported server</span></span><br/> | <span data-ttu-id="efa73-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efa73-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="efa73-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="efa73-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="efa73-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="efa73-121"><dt>Netmon.h</dt></span></span> </dl> |



 

 





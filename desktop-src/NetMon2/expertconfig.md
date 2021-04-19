---
description: La structure EXPERTCONFIG contient les données de configuration de l’expert. L’expert recouvre le membre RawConfigData avec une structure spécifique à l’expert.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: EXPERTCONFIG, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536961"
---
# <a name="expertconfig-structure"></a><span data-ttu-id="ec1f4-104">EXPERTCONFIG, structure</span><span class="sxs-lookup"><span data-stu-id="ec1f4-104">EXPERTCONFIG structure</span></span>

<span data-ttu-id="ec1f4-105">La structure **EXPERTCONFIG** contient les données de configuration de l’expert.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-105">The **EXPERTCONFIG** structure contains the configuration data of the expert.</span></span> <span data-ttu-id="ec1f4-106">L’expert recouvre le membre **RawConfigData** avec une structure spécifique à l’expert.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-106">The expert overlays the **RawConfigData** member with an expert-specific structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec1f4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec1f4-107">Syntax</span></span>


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a><span data-ttu-id="ec1f4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ec1f4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec1f4-109">**RawConfigLength**</span><span class="sxs-lookup"><span data-stu-id="ec1f4-109">**RawConfigLength**</span></span>
</dt> <dd>

<span data-ttu-id="ec1f4-110">Longueur totale de la structure, y compris les quatre octets utilisés pour le membre.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-110">Total length of the structure, including the four bytes used for the member.</span></span> <span data-ttu-id="ec1f4-111">Moniteur réseau utilise la valeur lors de l’enregistrement et de la lecture de la structure sur un lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-111">Network Monitor uses the value when the structure is saved-to and read-from a disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="ec1f4-112">**RawConfigData**</span><span class="sxs-lookup"><span data-stu-id="ec1f4-112">**RawConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="ec1f4-113">Données de configuration.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-113">Configuration data.</span></span> <span data-ttu-id="ec1f4-114">L’expert doit ajouter les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-114">The expert must add the configuration data.</span></span> <span data-ttu-id="ec1f4-115">Supposons, par exemple, que vous disposiez d’une structure de données similaire à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-115">For example, suppose that you had a data structure that looked like this.</span></span>

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

<span data-ttu-id="ec1f4-116">Notez que **RawConfigLength** garantit le bon fonctionnement de la superposition.</span><span class="sxs-lookup"><span data-stu-id="ec1f4-116">Note that **RawConfigLength** ensures that the overlay works correctly.</span></span> <span data-ttu-id="ec1f4-117">Lorsque vous utilisez les données, votre code peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="ec1f4-117">When you use the data, your code might look like this:</span></span>

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec1f4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec1f4-118">Requirements</span></span>



| <span data-ttu-id="ec1f4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec1f4-119">Requirement</span></span> | <span data-ttu-id="ec1f4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec1f4-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1f4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec1f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1f4-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec1f4-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ec1f4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec1f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1f4-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec1f4-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ec1f4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec1f4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec1f4-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec1f4-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 





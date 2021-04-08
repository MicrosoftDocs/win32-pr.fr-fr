---
title: Énumération MPSCAN_TYPE (MpClient. h)
description: Type d’analyse effectuée.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMPSCAN_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740133"
---
# <a name="mpscan_type-enumeration"></a><span data-ttu-id="c77b3-105">\_Énumération de type MPSCAN</span><span class="sxs-lookup"><span data-stu-id="c77b3-105">MPSCAN\_TYPE enumeration</span></span>

<span data-ttu-id="c77b3-106">Type d’analyse effectuée.</span><span class="sxs-lookup"><span data-stu-id="c77b3-106">Type of scan performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c77b3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c77b3-107">Syntax</span></span>


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c77b3-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c77b3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c77b3-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**\_type MPSCAN \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="c77b3-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**MPSCAN\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-110">À usage interne uniquement</span><span class="sxs-lookup"><span data-stu-id="c77b3-110">Internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="c77b3-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ type \_ rapide**</span><span class="sxs-lookup"><span data-stu-id="c77b3-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN\_TYPE\_QUICK**</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-112">Analyse les processus en cours d’exécution et divers points ASEP dans le système où les programmes malveillants sont généralement masqués.</span><span class="sxs-lookup"><span data-stu-id="c77b3-112">Scans running processes and various ASEP points in the system where malware typically hides.</span></span>

</dd> <dt>

<span data-ttu-id="c77b3-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN \_ type \_ complet**</span><span class="sxs-lookup"><span data-stu-id="c77b3-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN\_TYPE\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-114">Effectue une analyse rapide suivie d’une analyse de tous les lecteurs fixes du système.</span><span class="sxs-lookup"><span data-stu-id="c77b3-114">Performs a quick scan followed by scan of all fixed drives of the system.</span></span>

</dd> <dt>

<span data-ttu-id="c77b3-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_ressource de type MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="c77b3-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN\_TYPE\_RESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-116">Analyse des ressources spécifiques, telles que des fichiers ou des dossiers.</span><span class="sxs-lookup"><span data-stu-id="c77b3-116">Scans specific resources, such as files or folders.</span></span>

</dd> <dt>

<span data-ttu-id="c77b3-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN \_ type \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="c77b3-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="c77b3-118">Valeur maximale possible.</span><span class="sxs-lookup"><span data-stu-id="c77b3-118">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c77b3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c77b3-119">Requirements</span></span>



| <span data-ttu-id="c77b3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c77b3-120">Requirement</span></span> | <span data-ttu-id="c77b3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c77b3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c77b3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c77b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c77b3-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c77b3-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c77b3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c77b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c77b3-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c77b3-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c77b3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c77b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c77b3-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c77b3-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 






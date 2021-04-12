---
title: Structure MPENDOFLIFE_DATA (MpClient. h)
description: '\ 0034 ; Fin de vie \ 0034 ; données de notification.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPENDOFLIFE_DATA
- PMPENDOFLIFE_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104851"
---
# <a name="mpendoflife_data-structure"></a><span data-ttu-id="759a3-105">\_Structure de données MPENDOFLIFE</span><span class="sxs-lookup"><span data-stu-id="759a3-105">MPENDOFLIFE\_DATA structure</span></span>

<span data-ttu-id="759a3-106">Données de notification de « fin de vie ».</span><span class="sxs-lookup"><span data-stu-id="759a3-106">"End of life" notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="759a3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="759a3-107">Syntax</span></span>


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a><span data-ttu-id="759a3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="759a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="759a3-109">**ftSignatureExpiry**</span><span class="sxs-lookup"><span data-stu-id="759a3-109">**ftSignatureExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="759a3-110">Type : **fileTime**</span><span class="sxs-lookup"><span data-stu-id="759a3-110">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="759a3-111">Heure d’expiration de la signature.</span><span class="sxs-lookup"><span data-stu-id="759a3-111">Time when the signature expires.</span></span>

</dd> <dt>

<span data-ttu-id="759a3-112">**ftPlatformExpiry**</span><span class="sxs-lookup"><span data-stu-id="759a3-112">**ftPlatformExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="759a3-113">Type : **fileTime**</span><span class="sxs-lookup"><span data-stu-id="759a3-113">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="759a3-114">Heure d’expiration de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="759a3-114">Time when the platform expires.</span></span>

</dd> <dt>

<span data-ttu-id="759a3-115">**fAdminControlled**</span><span class="sxs-lookup"><span data-stu-id="759a3-115">**fAdminControlled**</span></span>
</dt> <dd>

<span data-ttu-id="759a3-116">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="759a3-116">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="759a3-117">True si l’administrateur contrôlant la stratégie pour l’indication de la notification.</span><span class="sxs-lookup"><span data-stu-id="759a3-117">True if the administrator controlling the policy for showing the notification.</span></span> <span data-ttu-id="759a3-118">Si cette option est définie, l’interface utilisateur n’affiche pas la notification de fin de vie.</span><span class="sxs-lookup"><span data-stu-id="759a3-118">If set, this tells the UI to not show the EOL notification.</span></span>

</dd> <dt>

<span data-ttu-id="759a3-119">**fEndOfLifeImpendingOrPast**</span><span class="sxs-lookup"><span data-stu-id="759a3-119">**fEndOfLifeImpendingOrPast**</span></span>
</dt> <dd>

<span data-ttu-id="759a3-120">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="759a3-120">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="759a3-121">True si la « fin de vie » est en attente ou passée.</span><span class="sxs-lookup"><span data-stu-id="759a3-121">True if "End of Life" is pending or past.</span></span> <span data-ttu-id="759a3-122">Si la valeur est false, l’interface utilisateur et les clients peuvent effacer tout État lié à la EOL.</span><span class="sxs-lookup"><span data-stu-id="759a3-122">If false, UI and clients can clear any EOL related states.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="759a3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="759a3-123">Requirements</span></span>



| <span data-ttu-id="759a3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="759a3-124">Requirement</span></span> | <span data-ttu-id="759a3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="759a3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="759a3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="759a3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="759a3-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="759a3-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="759a3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="759a3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="759a3-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="759a3-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="759a3-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="759a3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="759a3-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="759a3-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 






---
title: Structure MPSAMPLE_DATA (MpClient. h)
description: Données de notification transmises à l’exemple de fonction de rappel de soumission.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSAMPLE_DATA
- PMPSAMPLE_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106297"
---
# <a name="mpsample_data-structure"></a><span data-ttu-id="6fa46-105">\_Structure de données MPSAMPLE</span><span class="sxs-lookup"><span data-stu-id="6fa46-105">MPSAMPLE\_DATA structure</span></span>

<span data-ttu-id="6fa46-106">Données de notification transmises à l’exemple de fonction de rappel de soumission.</span><span class="sxs-lookup"><span data-stu-id="6fa46-106">Notification data passed to the sample submission callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa46-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fa46-107">Syntax</span></span>


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a><span data-ttu-id="6fa46-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6fa46-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fa46-109">**dwSampleIndex**</span><span class="sxs-lookup"><span data-stu-id="6fa46-109">**dwSampleIndex**</span></span>
</dt> <dd>

<span data-ttu-id="6fa46-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6fa46-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6fa46-111">Index de l’exemple d’élément pour lequel l’état d’envoi est signalé.</span><span class="sxs-lookup"><span data-stu-id="6fa46-111">Index of the sample item for which the submission status is reported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fa46-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fa46-112">Requirements</span></span>



| <span data-ttu-id="6fa46-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fa46-113">Requirement</span></span> | <span data-ttu-id="6fa46-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fa46-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa46-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fa46-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa46-116">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fa46-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6fa46-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fa46-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa46-118">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fa46-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fa46-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fa46-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa46-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa46-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 






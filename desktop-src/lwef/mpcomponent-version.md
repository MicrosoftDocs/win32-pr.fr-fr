---
title: Structure MPCOMPONENT_VERSION (MpClient. h)
description: Version et heure de mise à jour pour un composant individuel.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCOMPONENT_VERSION
- PMPCOMPONENT_VERSION des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942074"
---
# <a name="mpcomponent_version-structure"></a><span data-ttu-id="09f09-105">Structure de la version de MPCOMPONENT \_</span><span class="sxs-lookup"><span data-stu-id="09f09-105">MPCOMPONENT\_VERSION structure</span></span>

<span data-ttu-id="09f09-106">Version et heure de mise à jour pour un composant individuel.</span><span class="sxs-lookup"><span data-stu-id="09f09-106">Version and update time for an individual component.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f09-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09f09-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a><span data-ttu-id="09f09-108">Membres</span><span class="sxs-lookup"><span data-stu-id="09f09-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="09f09-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="09f09-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="09f09-110">Type : **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="09f09-110">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="09f09-111">Champ version.</span><span class="sxs-lookup"><span data-stu-id="09f09-111">Version field.</span></span> <span data-ttu-id="09f09-112">Chaque **mot** représente major, minor, Build et revision.</span><span class="sxs-lookup"><span data-stu-id="09f09-112">Each **WORD** represents major, minor, build, and revision.</span></span>

</dd> <dt>

<span data-ttu-id="09f09-113">**UpdateTime**</span><span class="sxs-lookup"><span data-stu-id="09f09-113">**UpdateTime**</span></span>
</dt> <dd>

<span data-ttu-id="09f09-114">Type : **\_ entier ULARGE**</span><span class="sxs-lookup"><span data-stu-id="09f09-114">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="09f09-115">Heure de la dernière mise à jour du composant, au format **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="09f09-115">Last update time of the component, in **FILETIME** format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09f09-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09f09-116">Requirements</span></span>



| <span data-ttu-id="09f09-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09f09-117">Requirement</span></span> | <span data-ttu-id="09f09-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="09f09-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09f09-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09f09-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09f09-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09f09-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="09f09-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09f09-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09f09-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09f09-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09f09-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="09f09-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09f09-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f09-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 






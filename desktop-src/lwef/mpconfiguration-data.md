---
title: Structure MPCONFIGURATION_DATA (MpClient. h)
description: Contient des données sur les modifications de configuration, y compris les anciennes et nouvelles valeurs.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCONFIGURATION_DATA
- PMPCONFIGURATION_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032711"
---
# <a name="mpconfiguration_data-structure"></a><span data-ttu-id="a5392-105">\_Structure de données MPCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="a5392-105">MPCONFIGURATION\_DATA structure</span></span>

<span data-ttu-id="a5392-106">Contient des données sur les modifications de configuration, y compris les anciennes et nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="a5392-106">Contains data about configuration changes, including the old and new values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5392-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5392-107">Syntax</span></span>


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a><span data-ttu-id="a5392-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a5392-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a5392-109">**ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="a5392-109">**ConfigurationName**</span></span>
</dt> <dd>

<span data-ttu-id="a5392-110">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="a5392-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a5392-111">Nom de la configuration qui a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="a5392-111">Name of the configuration that changed.</span></span>

</dd> <dt>

<span data-ttu-id="a5392-112">**DataType**</span><span class="sxs-lookup"><span data-stu-id="a5392-112">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="a5392-113">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a5392-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a5392-114">Type de données utilisé.</span><span class="sxs-lookup"><span data-stu-id="a5392-114">The type of data used.</span></span>

</dd> <dt>

<span data-ttu-id="a5392-115">**PreviousDataSize**</span><span class="sxs-lookup"><span data-stu-id="a5392-115">**PreviousDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="a5392-116">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a5392-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a5392-117">Taille des données précédentes, en octets.</span><span class="sxs-lookup"><span data-stu-id="a5392-117">Size of previous data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a5392-118">**pPreviousData**</span><span class="sxs-lookup"><span data-stu-id="a5392-118">**pPreviousData**</span></span>
</dt> <dd>

<span data-ttu-id="a5392-119">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="a5392-119">Type: \**BYTE\** _</span></span>

</dd> <dd>

<span data-ttu-id="a5392-120">Pointeur vers les données précédentes.</span><span class="sxs-lookup"><span data-stu-id="a5392-120">Pointer to previous data.</span></span>

</dd> <dt>

<span data-ttu-id="a5392-121">_ *CurrentDataSize*\*</span><span class="sxs-lookup"><span data-stu-id="a5392-121">_ *CurrentDataSize*\*</span></span>
</dt> <dd>

<span data-ttu-id="a5392-122">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a5392-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a5392-123">Taille des nouvelles données, en octets.</span><span class="sxs-lookup"><span data-stu-id="a5392-123">Size of new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a5392-124">**pCurrentData**</span><span class="sxs-lookup"><span data-stu-id="a5392-124">**pCurrentData**</span></span>
</dt> <dd>

<span data-ttu-id="a5392-125">Type : **Byte \***</span><span class="sxs-lookup"><span data-stu-id="a5392-125">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="a5392-126">Pointeur vers de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="a5392-126">Pointer to new data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5392-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5392-127">Requirements</span></span>



| <span data-ttu-id="a5392-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5392-128">Requirement</span></span> | <span data-ttu-id="a5392-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5392-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5392-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5392-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a5392-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5392-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a5392-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5392-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a5392-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5392-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5392-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5392-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5392-135"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5392-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 






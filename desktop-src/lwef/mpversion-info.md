---
title: Structure MPVERSION_INFO (MpClient. h)
description: Informations de version pour les composants du gestionnaire de protection contre les programmes malveillants.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPVERSION_INFO
- PMPVERSION_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317394"
---
# <a name="mpversion_info-structure"></a><span data-ttu-id="dc899-105">\_Structure d’informations MPVERSION</span><span class="sxs-lookup"><span data-stu-id="dc899-105">MPVERSION\_INFO structure</span></span>

<span data-ttu-id="dc899-106">Informations de version pour les composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="dc899-106">Version information for the malware protection manager's components.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc899-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc899-107">Syntax</span></span>


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a><span data-ttu-id="dc899-108">Membres</span><span class="sxs-lookup"><span data-stu-id="dc899-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc899-109">**Produit**</span><span class="sxs-lookup"><span data-stu-id="dc899-109">**Product**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-110">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-110">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-111">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="dc899-111">Product version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-112">**Service**</span><span class="sxs-lookup"><span data-stu-id="dc899-112">**Service**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-113">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-113">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-114">Version du composant du service.</span><span class="sxs-lookup"><span data-stu-id="dc899-114">Service component version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-115">**FileSystemFilter**</span><span class="sxs-lookup"><span data-stu-id="dc899-115">**FileSystemFilter**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-116">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-116">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-117">Version du composant filtre du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dc899-117">File system filter component version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-118">**Moteur**</span><span class="sxs-lookup"><span data-stu-id="dc899-118">**Engine**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-119">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-119">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-120">Version du composant moteur.</span><span class="sxs-lookup"><span data-stu-id="dc899-120">Engine component version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-121">**ASSignature**</span><span class="sxs-lookup"><span data-stu-id="dc899-121">**ASSignature**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-122">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-122">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-123">Version du composant de signature anti-espion.</span><span class="sxs-lookup"><span data-stu-id="dc899-123">Antispyware signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-124">**AVSignature**</span><span class="sxs-lookup"><span data-stu-id="dc899-124">**AVSignature**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-125">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-125">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-126">Version du composant de signature antivirus.</span><span class="sxs-lookup"><span data-stu-id="dc899-126">Antivirus signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-127">**NISEngine**</span><span class="sxs-lookup"><span data-stu-id="dc899-127">**NISEngine**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-128">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-128">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-129">Version du moteur NIS.</span><span class="sxs-lookup"><span data-stu-id="dc899-129">NIS engine version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-130">**NISSignature**</span><span class="sxs-lookup"><span data-stu-id="dc899-130">**NISSignature**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-131">Type : **[ **MPCOMPONENT \_ version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="dc899-131">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-132">Version du composant de signature de signature NIS.</span><span class="sxs-lookup"><span data-stu-id="dc899-132">NIS Signature signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="dc899-133">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="dc899-133">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="dc899-134">Type : **[**MPCOMPONENT \_ version**](mpcomponent-version.md) \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="dc899-134">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="dc899-135">Champs réservés.</span><span class="sxs-lookup"><span data-stu-id="dc899-135">Reserved fields.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc899-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc899-136">Requirements</span></span>



| <span data-ttu-id="dc899-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc899-137">Requirement</span></span> | <span data-ttu-id="dc899-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc899-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc899-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc899-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dc899-140">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc899-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dc899-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc899-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dc899-142">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc899-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc899-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc899-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc899-144"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc899-144"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc899-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc899-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc899-146">**VERSION de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="dc899-146">**MPCOMPONENT\_VERSION**</span></span>](mpcomponent-version.md)
</dt> </dl>

 

 






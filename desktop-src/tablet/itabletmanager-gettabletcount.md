---
description: Récupère le nombre de tablettes attachées au système.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'ITabletManager :: GetTabletCount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210614"
---
# <a name="itabletmanagergettabletcount-method"></a><span data-ttu-id="0da27-103">ITabletManager :: GetTabletCount, méthode</span><span class="sxs-lookup"><span data-stu-id="0da27-103">ITabletManager::GetTabletCount method</span></span>

<span data-ttu-id="0da27-104">Récupère le nombre de tablettes attachées au système.</span><span class="sxs-lookup"><span data-stu-id="0da27-104">Retrieves the number of tablets attached to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0da27-105">Syntax</span></span>


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a><span data-ttu-id="0da27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0da27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da27-107">*pcTablets* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0da27-107">*pcTablets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0da27-108">Nombre de tablettes attachées au système.</span><span class="sxs-lookup"><span data-stu-id="0da27-108">The number of tablets attached to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da27-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0da27-109">Return value</span></span>

<span data-ttu-id="0da27-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0da27-110">This method can return one of these values.</span></span>



| <span data-ttu-id="0da27-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0da27-111">Return code</span></span>                                                                            | <span data-ttu-id="0da27-112">Description</span><span class="sxs-lookup"><span data-stu-id="0da27-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0da27-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0da27-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0da27-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0da27-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0da27-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0da27-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0da27-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="0da27-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0da27-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0da27-117">Requirements</span></span>



| <span data-ttu-id="0da27-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0da27-118">Requirement</span></span> | <span data-ttu-id="0da27-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0da27-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0da27-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0da27-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0da27-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0da27-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0da27-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0da27-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0da27-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0da27-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0da27-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0da27-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="0da27-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0da27-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da27-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0da27-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da27-127">**Interface ITabletManager**</span><span class="sxs-lookup"><span data-stu-id="0da27-127">**ITabletManager Interface**</span></span>](itabletmanager.md)
</dt> </dl>

 

 





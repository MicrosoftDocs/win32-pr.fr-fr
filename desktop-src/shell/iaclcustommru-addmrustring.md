---
description: Ajoute une entrée à la liste des derniers fichiers utilisés (MRU).
title: 'IACLCustomMRU :: AddMRUString, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842000"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="c5cff-103">IACLCustomMRU :: AddMRUString, méthode</span><span class="sxs-lookup"><span data-stu-id="c5cff-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="c5cff-104">Ajoute une entrée à la liste des derniers fichiers utilisés (MRU).</span><span class="sxs-lookup"><span data-stu-id="c5cff-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5cff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5cff-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="c5cff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5cff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5cff-107">*pwszEntry* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c5cff-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5cff-108">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c5cff-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="c5cff-109">Pointeur vers une mémoire tampon contenant la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="c5cff-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5cff-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c5cff-110">Return value</span></span>

<span data-ttu-id="c5cff-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c5cff-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c5cff-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c5cff-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5cff-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5cff-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5cff-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c5cff-114">Requirements</span></span>



| <span data-ttu-id="c5cff-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5cff-115">Requirement</span></span> | <span data-ttu-id="c5cff-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5cff-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5cff-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5cff-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c5cff-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5cff-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c5cff-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5cff-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c5cff-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5cff-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





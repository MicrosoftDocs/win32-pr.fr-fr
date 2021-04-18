---
description: Charge une liste de chaînes dans la liste des derniers fichiers utilisés (MRU) à partir du Registre.
title: 'IACLCustomMRU :: Initialize, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991540"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="ff04d-103">IACLCustomMRU :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="ff04d-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="ff04d-104">Charge une liste de chaînes dans la liste des derniers fichiers utilisés (MRU) à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="ff04d-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff04d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff04d-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="ff04d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff04d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff04d-107">*pwszMRURegKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff04d-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff04d-108">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff04d-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ff04d-109">Pointeur vers une mémoire tampon qui contient la clé de registre contenant les chaînes de la liste MRU.</span><span class="sxs-lookup"><span data-stu-id="ff04d-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="ff04d-110">*dwMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff04d-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff04d-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ff04d-111">Type: **DWORD**</span></span>

<span data-ttu-id="ff04d-112">Nombre maximal d’entrées qui peuvent être extraites de *pwszMRURegKey*.</span><span class="sxs-lookup"><span data-stu-id="ff04d-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff04d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff04d-113">Return value</span></span>

<span data-ttu-id="ff04d-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff04d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ff04d-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff04d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff04d-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff04d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff04d-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ff04d-117">Requirements</span></span>



| <span data-ttu-id="ff04d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff04d-118">Requirement</span></span> | <span data-ttu-id="ff04d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff04d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff04d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff04d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff04d-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff04d-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ff04d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff04d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff04d-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff04d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





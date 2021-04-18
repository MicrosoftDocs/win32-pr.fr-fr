---
description: Récupère l’index pour la balise et le type de clé spécifiés à partir de la base de données spécifiée.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483232"
---
# <a name="sdbgetindex-function"></a><span data-ttu-id="fd96b-103">SdbGetIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="fd96b-103">SdbGetIndex function</span></span>

<span data-ttu-id="fd96b-104">Récupère l’index pour la balise et le type de clé spécifiés à partir de la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fd96b-104">Retrieves the index for the specified tag and key type from the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd96b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd96b-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fd96b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd96b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd96b-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd96b-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd96b-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="fd96b-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="fd96b-109">*tWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd96b-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd96b-110">BALIse.</span><span class="sxs-lookup"><span data-stu-id="fd96b-110">The TAG.</span></span>

</dd> <dt>

<span data-ttu-id="fd96b-111">*tKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd96b-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd96b-112">Type de clé.</span><span class="sxs-lookup"><span data-stu-id="fd96b-112">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="fd96b-113">*lpdwFlags* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fd96b-113">*lpdwFlags* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd96b-114">Ce paramètre peut être égal à 0 ou à la **\_ \_ \_ clé unique de l’index SHIMDB** (0x00000001).</span><span class="sxs-lookup"><span data-stu-id="fd96b-114">This parameter can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd96b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd96b-115">Return value</span></span>

<span data-ttu-id="fd96b-116">**TagId** de l’index ou **TagId \_ null**.</span><span class="sxs-lookup"><span data-stu-id="fd96b-116">The **TAGID** of the index or **TAGID\_NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd96b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fd96b-117">Remarks</span></span>

<span data-ttu-id="fd96b-118">L’index résultant peut être utilisé pour les opérations de lecture.</span><span class="sxs-lookup"><span data-stu-id="fd96b-118">The resulting index can be used for read operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd96b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd96b-119">Requirements</span></span>



| <span data-ttu-id="fd96b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd96b-120">Requirement</span></span> | <span data-ttu-id="fd96b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd96b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd96b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd96b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd96b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd96b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fd96b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd96b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd96b-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd96b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fd96b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fd96b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd96b-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd96b-127"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 





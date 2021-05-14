---
description: Contient des informations qui définissent une nouvelle liste des derniers fichiers utilisés (MRU). Utilisé par CreateMRUListW.
title: MRUINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840760"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="362d3-104">MRUINFO, structure</span><span class="sxs-lookup"><span data-stu-id="362d3-104">MRUINFO structure</span></span>

<span data-ttu-id="362d3-105">Contient des informations qui définissent une nouvelle liste des derniers fichiers utilisés (MRU).</span><span class="sxs-lookup"><span data-stu-id="362d3-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="362d3-106">Utilisé par [**CreateMRUListW**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="362d3-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="362d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="362d3-107">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a><span data-ttu-id="362d3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="362d3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="362d3-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="362d3-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="362d3-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="362d3-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="362d3-111">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="362d3-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="362d3-112">**uMax**</span><span class="sxs-lookup"><span data-stu-id="362d3-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="362d3-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="362d3-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="362d3-114">Nombre maximal d’entrées dans la liste des fichiers récents.</span><span class="sxs-lookup"><span data-stu-id="362d3-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="362d3-115">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="362d3-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="362d3-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="362d3-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="362d3-117">Un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="362d3-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="362d3-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINAIRE** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="362d3-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="362d3-119">Les données sont stockées dans le Registre sous forme de données binaires plutôt que de données de chaîne.</span><span class="sxs-lookup"><span data-stu-id="362d3-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="362d3-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="362d3-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="362d3-121">Écrire les modifications apportées à la version des fichiers MRU stockés dans le registre uniquement lors de l’ajout d’un nouvel élément ou lorsque les ressources de la liste MRU sont libérées de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="362d3-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="362d3-122">Notez que la version active des fichiers MRU en mémoire est mise à jour immédiatement en réponse à toute modification de contenu ou de commande.</span><span class="sxs-lookup"><span data-stu-id="362d3-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="362d3-123">**hKey**</span><span class="sxs-lookup"><span data-stu-id="362d3-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="362d3-124">Type : **HKEY**</span><span class="sxs-lookup"><span data-stu-id="362d3-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="362d3-125">Handle vers la clé actuellement ouverte, ou l’une des valeurs prédéfinies suivantes sous lesquelles stocker les données MRU.</span><span class="sxs-lookup"><span data-stu-id="362d3-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="362d3-126">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="362d3-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="362d3-127">**HKEY \_ local \_ machine**</span><span class="sxs-lookup"><span data-stu-id="362d3-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="362d3-128">**lpszSubKey**</span><span class="sxs-lookup"><span data-stu-id="362d3-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="362d3-129">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="362d3-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="362d3-130">Sous-clé dans laquelle stocker les données MRU.</span><span class="sxs-lookup"><span data-stu-id="362d3-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="362d3-131">**lpfnCompare**</span><span class="sxs-lookup"><span data-stu-id="362d3-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="362d3-132">Type : **[ **MRUCMPPROC**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="362d3-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="362d3-133">Pointeur vers une fonction de comparaison de données facultative qui peut être utilisée pour déterminer si un élément est présent dans la liste MRU.</span><span class="sxs-lookup"><span data-stu-id="362d3-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="362d3-134">Cela est utile lorsque la liste MRU a été créée avec l’indicateur **\_ binaire MRU** .</span><span class="sxs-lookup"><span data-stu-id="362d3-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="362d3-135">Si ce membre a la **valeur null**, les fonctions de comparaison de chaînes standard sont utilisées ; pour les données binaires, une comparaison de mémoire directe est utilisée.</span><span class="sxs-lookup"><span data-stu-id="362d3-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="362d3-136">Notes</span><span class="sxs-lookup"><span data-stu-id="362d3-136">Remarks</span></span>

<span data-ttu-id="362d3-137">Cette structure n’est pas définie dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="362d3-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="362d3-138">Vous devez le définir vous-même.</span><span class="sxs-lookup"><span data-stu-id="362d3-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="362d3-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="362d3-139">Requirements</span></span>



| <span data-ttu-id="362d3-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="362d3-140">Requirement</span></span> | <span data-ttu-id="362d3-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="362d3-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="362d3-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="362d3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="362d3-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="362d3-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="362d3-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="362d3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="362d3-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="362d3-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="362d3-146">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="362d3-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="362d3-147">**MRUINFOW** (Unicode) et **MRUINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="362d3-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 





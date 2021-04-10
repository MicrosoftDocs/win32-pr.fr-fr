---
description: Écrit des données binaires à partir du fichier spécifié dans la base de données spécifiée.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: SdbWriteBinaryTagFromFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950528"
---
# <a name="sdbwritebinarytagfromfile-function"></a><span data-ttu-id="0124c-103">SdbWriteBinaryTagFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="0124c-103">SdbWriteBinaryTagFromFile function</span></span>

<span data-ttu-id="0124c-104">Écrit des données binaires à partir du fichier spécifié dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0124c-104">Writes binary data from the specified file to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0124c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0124c-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a><span data-ttu-id="0124c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0124c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0124c-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0124c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0124c-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="0124c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0124c-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0124c-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0124c-110">BALIse pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="0124c-110">The TAG for the entry.</span></span> <span data-ttu-id="0124c-111">Cette BALIse doit être de **type \_ \_ binaire**.</span><span class="sxs-lookup"><span data-stu-id="0124c-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="0124c-112">*pwszPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0124c-112">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0124c-113">Chemin d’accès au fichier qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="0124c-113">The path to the file that contains the data.</span></span> <span data-ttu-id="0124c-114">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="0124c-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0124c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0124c-115">Return value</span></span>

<span data-ttu-id="0124c-116">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="0124c-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0124c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0124c-117">Requirements</span></span>



| <span data-ttu-id="0124c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0124c-118">Requirement</span></span> | <span data-ttu-id="0124c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0124c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0124c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0124c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0124c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0124c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0124c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0124c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0124c-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0124c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0124c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0124c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0124c-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0124c-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0124c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0124c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0124c-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="0124c-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> </dl>

 

 





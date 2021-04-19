---
description: La fonction RemoveFromBlob supprime tout niveau d’entrée d’objet BLOB (propriétaire, catégorie ou balise).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: RemoveFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514418"
---
# <a name="removefromblob-function"></a><span data-ttu-id="5f1a9-103">RemoveFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="5f1a9-103">RemoveFromBlob function</span></span>

<span data-ttu-id="5f1a9-104">La fonction **RemoveFromBlob** supprime tout niveau d’entrée d’objet BLOB (**propriétaire**, **catégorie** ou **balise**).</span><span class="sxs-lookup"><span data-stu-id="5f1a9-104">The **RemoveFromBlob** function deletes any level of BLOB entry (**Owner**, **Category**, or **Tag**).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f1a9-105">Syntax</span></span>


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a><span data-ttu-id="5f1a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f1a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1a9-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f1a9-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f1a9-108">Handle vers l’objet BLOB à partir duquel une entrée est supprimée.</span><span class="sxs-lookup"><span data-stu-id="5f1a9-108">Handle to the BLOB from which an entry is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="5f1a9-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f1a9-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f1a9-110">Pointeur vers le nom du **propriétaire** .</span><span class="sxs-lookup"><span data-stu-id="5f1a9-110">Pointer to the **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="5f1a9-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f1a9-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f1a9-112">Pointeur vers le nom de la **catégorie** .</span><span class="sxs-lookup"><span data-stu-id="5f1a9-112">Pointer to the **Category** name.</span></span> <span data-ttu-id="5f1a9-113">Une valeur de paramètre **null** indique que l’appelant tente de supprimer les informations de **propriétaire** données et toutes ses entrées enfants.</span><span class="sxs-lookup"><span data-stu-id="5f1a9-113">A **NULL** parameter value indicates the caller is attempting to delete the given **Owner** information and all of its child entries.</span></span> <span data-ttu-id="5f1a9-114">Notez que si la valeur du paramètre *pCategoryName* est **null**, le paramètre *pTagName* doit également avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5f1a9-114">Note that if the *pCategoryName* parameter value is **NULL**, the *pTagName* parameter must also be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5f1a9-115">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f1a9-115">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f1a9-116">Pointeur vers le nom de la **balise** .</span><span class="sxs-lookup"><span data-stu-id="5f1a9-116">Pointer to the **Tag** name.</span></span> <span data-ttu-id="5f1a9-117">Une valeur _PTagName_ **null** indique que l’appelant tente de supprimer la **catégorie** donnée et toutes ses entrées enfants.</span><span class="sxs-lookup"><span data-stu-id="5f1a9-117">A **NULL**_pTagName_ value indicates the caller is attempting to delete the given **Category** and all of its child entries.</span></span> <span data-ttu-id="5f1a9-118">Si la valeur du paramètre n’est pas **null**, l’appelant demande uniquement que les entrées de **balise** spécifiées soient supprimées.</span><span class="sxs-lookup"><span data-stu-id="5f1a9-118">If the parameter value is not **NULL**, the caller is asking that only that the specified **Tag** entries be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1a9-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f1a9-119">Return value</span></span>

<span data-ttu-id="5f1a9-120">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5f1a9-120">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5f1a9-121">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5f1a9-121">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1a9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f1a9-122">Requirements</span></span>



| <span data-ttu-id="5f1a9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f1a9-123">Requirement</span></span> | <span data-ttu-id="5f1a9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f1a9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1a9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f1a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1a9-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f1a9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5f1a9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f1a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1a9-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f1a9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f1a9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f1a9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f1a9-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f1a9-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="5f1a9-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f1a9-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f1a9-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f1a9-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f1a9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5f1a9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f1a9-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f1a9-134"><dt>Npptools.dll</dt></span></span> </dl> |



 

 





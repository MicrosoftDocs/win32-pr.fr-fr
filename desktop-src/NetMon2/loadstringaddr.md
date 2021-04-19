---
description: La fonction LoadStringAddr transforme une chaîne (par exemple &\# 0034 ; 157.54.32.45&\# 0034 ;) et crée une adresse DWORD.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: LoadStringAddr, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515879"
---
# <a name="loadstringaddr-function"></a><span data-ttu-id="ddce3-103">LoadStringAddr fonction)</span><span class="sxs-lookup"><span data-stu-id="ddce3-103">LoadStringAddr function</span></span>

<span data-ttu-id="ddce3-104">La fonction **LoadStringAddr** transforme une chaîne (telle que « 157.54.32.45 ») et crée une adresse **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ddce3-104">The **LoadStringAddr** function transforms a string (such as "157.54.32.45") and creates a **DWORD** address.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddce3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddce3-105">Syntax</span></span>


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a><span data-ttu-id="ddce3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddce3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddce3-107">*pAddress*</span><span class="sxs-lookup"><span data-stu-id="ddce3-107">*pAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="ddce3-108">Pointeur vers une **valeur DWORD**.</span><span class="sxs-lookup"><span data-stu-id="ddce3-108">Pointer to a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="ddce3-109">*str*</span><span class="sxs-lookup"><span data-stu-id="ddce3-109">*str*</span></span> 
</dt> <dd>

<span data-ttu-id="ddce3-110">Pointeur désignant une chaîne de caractères avec la représentation x. x de l’adresse IP (par exemple, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="ddce3-110">Pointer to a character string with x.x.x.x representation of an IP address (for example,127.0.0.1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddce3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddce3-111">Return value</span></span>

<span data-ttu-id="ddce3-112">Si la fonction a réussi (le nom de l’adresse a été trouvé); la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="ddce3-112">If the function is successful (the address name was found); the return value is **TRUE**.</span></span>

<span data-ttu-id="ddce3-113">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="ddce3-113">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddce3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddce3-114">Requirements</span></span>



| <span data-ttu-id="ddce3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddce3-115">Requirement</span></span> | <span data-ttu-id="ddce3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddce3-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddce3-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddce3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ddce3-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddce3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ddce3-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddce3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ddce3-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddce3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ddce3-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddce3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddce3-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddce3-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ddce3-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ddce3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddce3-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddce3-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ddce3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ddce3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddce3-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddce3-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





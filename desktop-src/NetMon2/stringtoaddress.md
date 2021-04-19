---
description: La fonction StringToAddress convertit une chaîne en adresse.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: StringToAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534200"
---
# <a name="stringtoaddress-function"></a><span data-ttu-id="ddaa8-103">StringToAddress fonction)</span><span class="sxs-lookup"><span data-stu-id="ddaa8-103">StringToAddress function</span></span>

<span data-ttu-id="ddaa8-104">La fonction **StringToAddress** convertit une chaîne en adresse.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-104">The **StringToAddress** function converts a string to an address.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddaa8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddaa8-105">Syntax</span></span>


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a><span data-ttu-id="ddaa8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddaa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddaa8-107">*lpAddress* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ddaa8-107">*lpAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddaa8-108">Pointeur vers l’adresse vers laquelle la chaîne est convertie.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-108">Pointer to the address the string is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="ddaa8-109">*chaîne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ddaa8-109">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddaa8-110">Chaîne convertie en adresse.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-110">String that is converted to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddaa8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddaa8-111">Return value</span></span>

<span data-ttu-id="ddaa8-112">La valeur de retour est un pointeur vers la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="ddaa8-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddaa8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddaa8-113">Requirements</span></span>



| <span data-ttu-id="ddaa8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddaa8-114">Requirement</span></span> | <span data-ttu-id="ddaa8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddaa8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddaa8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddaa8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ddaa8-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddaa8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ddaa8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddaa8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ddaa8-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddaa8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ddaa8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddaa8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddaa8-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddaa8-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddaa8-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ddaa8-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddaa8-123"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddaa8-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="ddaa8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ddaa8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddaa8-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddaa8-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 





---
description: La fonction AddressToString convertit une adresse en chaîne.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: AddressToString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115879"
---
# <a name="addresstostring-function"></a><span data-ttu-id="963c2-103">AddressToString fonction)</span><span class="sxs-lookup"><span data-stu-id="963c2-103">AddressToString function</span></span>

<span data-ttu-id="963c2-104">La fonction **AddressToString** convertit une adresse en chaîne.</span><span class="sxs-lookup"><span data-stu-id="963c2-104">The **AddressToString** function converts an address into a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="963c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="963c2-105">Syntax</span></span>


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="963c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="963c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963c2-107">*chaîne* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="963c2-107">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="963c2-108">Chaîne dans laquelle l’adresse est convertie.</span><span class="sxs-lookup"><span data-stu-id="963c2-108">String that the address is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="963c2-109">*lpAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="963c2-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="963c2-110">Adresse qui est imprimée.</span><span class="sxs-lookup"><span data-stu-id="963c2-110">The address that is printed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963c2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="963c2-111">Return value</span></span>

<span data-ttu-id="963c2-112">La valeur de retour est un pointeur vers la chaîne convertie.</span><span class="sxs-lookup"><span data-stu-id="963c2-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="963c2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="963c2-113">Requirements</span></span>



| <span data-ttu-id="963c2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="963c2-114">Requirement</span></span> | <span data-ttu-id="963c2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="963c2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="963c2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="963c2-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="963c2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="963c2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="963c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="963c2-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="963c2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="963c2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="963c2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="963c2-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="963c2-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="963c2-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="963c2-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="963c2-123"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="963c2-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="963c2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="963c2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963c2-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="963c2-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 





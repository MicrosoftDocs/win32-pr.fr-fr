---
description: La fonction HTMLValueToUnicode convertit une chaîne HTML FP \_ UTF8 en chaîne Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: HTMLValueToUnicode, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750068"
---
# <a name="htmlvaluetounicode-function"></a><span data-ttu-id="3e8c9-103">HTMLValueToUnicode fonction)</span><span class="sxs-lookup"><span data-stu-id="3e8c9-103">HTMLValueToUnicode function</span></span>

<span data-ttu-id="3e8c9-104">La fonction **HTMLValueToUnicode** convertit une chaîne HTML FP \_ UTF8 en chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="3e8c9-104">The **HTMLValueToUnicode** function converts an HTML CP\_UTF8 string to a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e8c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e8c9-105">Syntax</span></span>


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3e8c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e8c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8c9-107">*pValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3e8c9-107">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e8c9-108">Sur entrée, pointeur vers la chaîne HTML fournie par MCSVC.</span><span class="sxs-lookup"><span data-stu-id="3e8c9-108">On input, pointer to the HTML string supplied by the MCSVC.</span></span>

<span data-ttu-id="3e8c9-109">Sur la sortie, pointeur vers la chaîne Unicode convertie.</span><span class="sxs-lookup"><span data-stu-id="3e8c9-109">On output, pointer to the converted Unicode string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8c9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e8c9-110">Return value</span></span>

<span data-ttu-id="3e8c9-111">La fonction retourne l’équivalent Unicode de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="3e8c9-111">The function returns the Unicode equivalent of the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8c9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e8c9-112">Requirements</span></span>



| <span data-ttu-id="3e8c9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e8c9-113">Requirement</span></span> | <span data-ttu-id="3e8c9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e8c9-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8c9-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e8c9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8c9-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e8c9-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3e8c9-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e8c9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8c9-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e8c9-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3e8c9-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e8c9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e8c9-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e8c9-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3e8c9-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e8c9-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e8c9-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e8c9-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3e8c9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3e8c9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e8c9-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e8c9-124"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





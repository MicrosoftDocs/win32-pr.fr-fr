---
description: Identifie si le style de non-couleur spécifié est souligné.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526377"
---
# <a name="idulimestyle-function"></a><span data-ttu-id="0cbdd-103">IdUlIMEStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-103">IdUlIMEStyle function</span></span>

<span data-ttu-id="0cbdd-104">Identifie si le style de non-couleur spécifié est souligné.</span><span class="sxs-lookup"><span data-stu-id="0cbdd-104">Identifies whether the specified non-color style has underline.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cbdd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cbdd-105">Syntax</span></span>


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="0cbdd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cbdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cbdd-107">*pimestyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0cbdd-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cbdd-108">Une structure **IMESTYLE** retournée par la fonction [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="0cbdd-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cbdd-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cbdd-109">Return value</span></span>

<span data-ttu-id="0cbdd-110">Cette fonction peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0cbdd-110">This function can returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0cbdd-111">**IMESTY \_ UL \_ min** (2002)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-111">**IMESTY\_UL\_MIN** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-112">**IMESTY \_ UL \_ None** (2002)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-112">**IMESTY\_UL\_NONE** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-113">**IMESTY \_ UL \_ simple** (2003)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-113">**IMESTY\_UL\_SINGLE** (2003)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-114">**IMESTY \_ UL \_ pointé** (2005)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-114">**IMESTY\_UL\_DOTTED** (2005)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-115">**IMESTY \_ UL \_ épais** (2006)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-115">**IMESTY\_UL\_THICK** (2006)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-116">**IMESTY \_ UL en \_ minuscule** (2011)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-116">**IMESTY\_UL\_LOWER** (2011)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-117">**IMESTY \_ UL \_ THICKLOWER** (2012)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-117">**IMESTY\_UL\_THICKLOWER** (2012)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-118">**IMESTY \_ UL \_ THICKDITHLOWER** (2013)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-118">**IMESTY\_UL\_THICKDITHLOWER** (2013)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-119">**IMESTY \_ UL \_ DITHLOWER** (2014)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-119">**IMESTY\_UL\_DITHLOWER** (2014)</span></span>
</dt> <dt>

<span data-ttu-id="0cbdd-120">**IMESTY \_ UL \_ Max** (2014)</span><span class="sxs-lookup"><span data-stu-id="0cbdd-120">**IMESTY\_UL\_MAX** (2014)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0cbdd-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0cbdd-121">Remarks</span></span>

<span data-ttu-id="0cbdd-122">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0cbdd-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cbdd-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cbdd-123">Requirements</span></span>



| <span data-ttu-id="0cbdd-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cbdd-124">Requirement</span></span> | <span data-ttu-id="0cbdd-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cbdd-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cbdd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0cbdd-126">DLL</span></span><br/> | <dl> <span data-ttu-id="0cbdd-127"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cbdd-127"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cbdd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cbdd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbdd-129">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="0cbdd-129">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 

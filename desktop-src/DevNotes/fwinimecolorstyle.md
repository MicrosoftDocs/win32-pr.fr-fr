---
description: Spécifie si la couleur spécifiée est une couleur Windows.
ms.assetid: 0d2b2039-938c-4f9d-8ddc-9eb711f55009
title: FWinIMEColorStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FWinIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 28731672f5f1aff385f9051ba8b641b7cdcdf83c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523945"
---
# <a name="fwinimecolorstyle-function"></a><span data-ttu-id="e470d-103">FWinIMEColorStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="e470d-103">FWinIMEColorStyle function</span></span>

<span data-ttu-id="e470d-104">Spécifie si la couleur spécifiée est une couleur Windows.</span><span class="sxs-lookup"><span data-stu-id="e470d-104">Specifies whether the specified color is a Windows color.</span></span>

## <a name="syntax"></a><span data-ttu-id="e470d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e470d-105">Syntax</span></span>


```C++
BOOL __cdecl FWinIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="e470d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e470d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e470d-107">*pcolorstyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e470d-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e470d-108">Une structure **IMECOLORSTY** retournée à partir d’une fonction [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="e470d-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e470d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e470d-109">Return value</span></span>

<span data-ttu-id="e470d-110">Retourne la **valeur true** lorsque la couleur est une couleur Windows.</span><span class="sxs-lookup"><span data-stu-id="e470d-110">Returns **TRUE** when the color is a Windows color.</span></span>

## <a name="remarks"></a><span data-ttu-id="e470d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e470d-111">Remarks</span></span>

<span data-ttu-id="e470d-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e470d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e470d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e470d-113">Requirements</span></span>



| <span data-ttu-id="e470d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e470d-114">Requirement</span></span> | <span data-ttu-id="e470d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e470d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e470d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e470d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="e470d-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e470d-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e470d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e470d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e470d-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="e470d-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="e470d-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="e470d-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 

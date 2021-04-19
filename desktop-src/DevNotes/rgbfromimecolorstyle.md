---
description: Convertit une structure IMECOLORSTY en une structure COLORREF.
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: RGBFromIMEColorStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525146"
---
# <a name="rgbfromimecolorstyle-function"></a><span data-ttu-id="441e3-103">RGBFromIMEColorStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="441e3-103">RGBFromIMEColorStyle function</span></span>

<span data-ttu-id="441e3-104">Convertit une structure **IMECOLORSTY** en une structure [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="441e3-104">Converts an **IMECOLORSTY** structure to a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="441e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="441e3-105">Syntax</span></span>


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="441e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="441e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441e3-107">*pcolorstyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="441e3-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="441e3-108">Une structure **IMECOLORSTY** retournée à partir d’une fonction [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="441e3-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="441e3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="441e3-109">Return value</span></span>

<span data-ttu-id="441e3-110">Retourne une structure [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="441e3-110">Returns a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="441e3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="441e3-111">Remarks</span></span>

<span data-ttu-id="441e3-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="441e3-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="441e3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="441e3-113">Requirements</span></span>



| <span data-ttu-id="441e3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="441e3-114">Requirement</span></span> | <span data-ttu-id="441e3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="441e3-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="441e3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="441e3-116">DLL</span></span><br/> | <dl> <span data-ttu-id="441e3-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="441e3-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441e3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="441e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441e3-119">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="441e3-119">**COLORREF**</span></span>](../gdi/colorref.md)
</dt> <dt>

[<span data-ttu-id="441e3-120">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="441e3-120">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="441e3-121">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="441e3-121">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 

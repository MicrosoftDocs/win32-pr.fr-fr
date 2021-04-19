---
description: Spécifie si la couleur spécifiée est une couleur RVB.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: FRGBIMEColorStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: df11a2ad972791eaf7049bdef5fa927aaa4119da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524019"
---
# <a name="frgbimecolorstyle-function"></a><span data-ttu-id="1ecc8-103">FRGBIMEColorStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="1ecc8-103">FRGBIMEColorStyle function</span></span>

<span data-ttu-id="1ecc8-104">Spécifie si la couleur spécifiée est une couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-104">Specifies whether the specified color is an RGB color.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ecc8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ecc8-105">Syntax</span></span>


```C++
BOOL __cdecl FRGBIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="1ecc8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ecc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ecc8-107">*pcolorstyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ecc8-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ecc8-108">Une structure **IMECOLORSTY** retournée à partir d’une fonction [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="1ecc8-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ecc8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ecc8-109">Return value</span></span>

<span data-ttu-id="1ecc8-110">Retourne la **valeur true** lorsque la couleur est une couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="1ecc8-110">Returns **TRUE** when the color is an RGB color.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ecc8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1ecc8-111">Remarks</span></span>

<span data-ttu-id="1ecc8-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1ecc8-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ecc8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ecc8-113">Requirements</span></span>



| <span data-ttu-id="1ecc8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ecc8-114">Requirement</span></span> | <span data-ttu-id="1ecc8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ecc8-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecc8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1ecc8-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1ecc8-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc8-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ecc8-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ecc8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecc8-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="1ecc8-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="1ecc8-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="1ecc8-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 

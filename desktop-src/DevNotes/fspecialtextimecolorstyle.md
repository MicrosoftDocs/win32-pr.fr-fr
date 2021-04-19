---
description: Spécifie si la couleur spécifiée est une couleur de texte spéciale.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: FSpecialTextIMEColorStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543598"
---
# <a name="fspecialtextimecolorstyle-function"></a><span data-ttu-id="0d0b0-103">FSpecialTextIMEColorStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="0d0b0-103">FSpecialTextIMEColorStyle function</span></span>

<span data-ttu-id="0d0b0-104">Spécifie si la couleur spécifiée est une couleur de texte spéciale.</span><span class="sxs-lookup"><span data-stu-id="0d0b0-104">Specifies whether the specified color is a special text color.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d0b0-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="0d0b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d0b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d0b0-107">*pcolorstyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d0b0-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0b0-108">Une structure **IMECOLORSTY** retournée à partir d’une fonction [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="0d0b0-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d0b0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d0b0-109">Return value</span></span>

<span data-ttu-id="0d0b0-110">Retourne la **valeur true** lorsque la couleur est une couleur de texte spéciale.</span><span class="sxs-lookup"><span data-stu-id="0d0b0-110">Returns **TRUE** when the color is a special text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0b0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0d0b0-111">Remarks</span></span>

<span data-ttu-id="0d0b0-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0d0b0-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0b0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d0b0-113">Requirements</span></span>



| <span data-ttu-id="0d0b0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d0b0-114">Requirement</span></span> | <span data-ttu-id="0d0b0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d0b0-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0b0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0d0b0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0d0b0-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d0b0-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d0b0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d0b0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0b0-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="0d0b0-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="0d0b0-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="0d0b0-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 

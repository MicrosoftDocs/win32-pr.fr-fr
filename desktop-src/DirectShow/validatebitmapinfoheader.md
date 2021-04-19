---
description: La fonction ValidateBitmapInfoHeader vérifie une structure BITMAPINFOHEADER pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: ValidateBitmapInfoHeader, fonction (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530030"
---
# <a name="validatebitmapinfoheader-function"></a><span data-ttu-id="f5666-103">ValidateBitmapInfoHeader fonction)</span><span class="sxs-lookup"><span data-stu-id="f5666-103">ValidateBitmapInfoHeader function</span></span>

<span data-ttu-id="f5666-104">La `ValidateBitmapInfoHeader` fonction vérifie une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.</span><span class="sxs-lookup"><span data-stu-id="f5666-104">The `ValidateBitmapInfoHeader` function checks a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="f5666-105">Cette fonction ne garantit pas que la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) est valide ou que le code qui utilise la structure est sécurisé.</span><span class="sxs-lookup"><span data-stu-id="f5666-105">This function does not guarantee that the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f5666-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5666-106">Syntax</span></span>


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="f5666-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5666-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5666-108">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="f5666-108">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="f5666-109">Pointeur vers la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) à valider.</span><span class="sxs-lookup"><span data-stu-id="f5666-109">Pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure to validate.</span></span>

</dd> <dt>

<span data-ttu-id="f5666-110">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="f5666-110">*cbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f5666-111">Taille du bloc de mémoire qui contient la structure, en octets.</span><span class="sxs-lookup"><span data-stu-id="f5666-111">Size of the memory block that holds the structure, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5666-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5666-112">Return value</span></span>

<span data-ttu-id="f5666-113">Retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="f5666-113">Returns a Boolean value.</span></span> <span data-ttu-id="f5666-114">Si la valeur est **false**, la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f5666-114">If the value is **FALSE**, the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5666-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f5666-115">Remarks</span></span>

<span data-ttu-id="f5666-116">Cette fonction protège contre les erreurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5666-116">This function guards against the following errors:</span></span>

-   <span data-ttu-id="f5666-117">Débordement arithmétique dans la taille de la structure ou taille de structure non valide.</span><span class="sxs-lookup"><span data-stu-id="f5666-117">Arithmetic overflow in the structure size or an invalid structure size.</span></span>
-   <span data-ttu-id="f5666-118">Valeur non valide pour le membre **biClrUsed** .</span><span class="sxs-lookup"><span data-stu-id="f5666-118">Invalid value for the **biClrUsed** member.</span></span>
-   <span data-ttu-id="f5666-119">Débordement arithmétique dans la taille de l’image (**biSizeImage**).</span><span class="sxs-lookup"><span data-stu-id="f5666-119">Arithmetic overflow in the image size (**biSizeImage**).</span></span>
-   <span data-ttu-id="f5666-120">Valeurs non valides pour la taille de l’image (**biSizeImage**) pour les formats RVB.</span><span class="sxs-lookup"><span data-stu-id="f5666-120">Invalid values for the image size (**biSizeImage**) for RGB formats.</span></span>

<span data-ttu-id="f5666-121">La fonction ne vérifie pas si la structure décrit un format vidéo valide.</span><span class="sxs-lookup"><span data-stu-id="f5666-121">The function does not check whether the structure describes a valid video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5666-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5666-122">Requirements</span></span>



| <span data-ttu-id="f5666-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5666-123">Requirement</span></span> | <span data-ttu-id="f5666-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5666-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5666-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5666-125">Header</span></span><br/> | <dl> <span data-ttu-id="f5666-126"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5666-126"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5666-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5666-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5666-128">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="f5666-128">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 





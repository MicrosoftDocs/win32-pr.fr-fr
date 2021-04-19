---
description: Spécifie si un style sans couleur a un style de soulignement.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: FUlIMEStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: a49090d2ca192dfd3ec6d0064b92bd2233af79c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528696"
---
# <a name="fulimestyle-function"></a><span data-ttu-id="33e0d-103">FUlIMEStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="33e0d-103">FUlIMEStyle function</span></span>

<span data-ttu-id="33e0d-104">Spécifie si un style sans couleur a un style de soulignement.</span><span class="sxs-lookup"><span data-stu-id="33e0d-104">Specifies whether a non-color style has an underline style.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33e0d-105">Syntax</span></span>


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="33e0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33e0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e0d-107">*pimestyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33e0d-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e0d-108">Une structure **IMESTYLE** retournée par la fonction [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="33e0d-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e0d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33e0d-109">Return value</span></span>

<span data-ttu-id="33e0d-110">TRUE si le style a un style de soulignement.</span><span class="sxs-lookup"><span data-stu-id="33e0d-110">TRUE if the style has an underline style.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e0d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="33e0d-111">Remarks</span></span>

<span data-ttu-id="33e0d-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="33e0d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e0d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33e0d-113">Requirements</span></span>



| <span data-ttu-id="33e0d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33e0d-114">Requirement</span></span> | <span data-ttu-id="33e0d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="33e0d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33e0d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="33e0d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="33e0d-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33e0d-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e0d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33e0d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e0d-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="33e0d-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 

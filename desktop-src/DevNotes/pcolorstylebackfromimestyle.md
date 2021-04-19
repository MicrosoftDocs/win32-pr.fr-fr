---
description: Récupère le style de couleur d’arrière-plan du style spécifié.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: PColorStyleBackFromIMEStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 33ff9072fc5e850654f932817cd4ecf0e9372aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530321"
---
# <a name="pcolorstylebackfromimestyle-function"></a><span data-ttu-id="8c31a-103">PColorStyleBackFromIMEStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="8c31a-103">PColorStyleBackFromIMEStyle function</span></span>

<span data-ttu-id="8c31a-104">Récupère le style de couleur d’arrière-plan du style spécifié.</span><span class="sxs-lookup"><span data-stu-id="8c31a-104">Retrieves the background color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c31a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c31a-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="8c31a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c31a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c31a-107">*pimestyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c31a-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c31a-108">Une structure **IMESTYLE** retournée par la fonction [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="8c31a-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c31a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c31a-109">Return value</span></span>

<span data-ttu-id="8c31a-110">Pointeur vers une structure **IMECOLORSTY** qui représente le style de couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8c31a-110">Pointer to an **IMECOLORSTY** structure representing the background color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c31a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8c31a-111">Remarks</span></span>

<span data-ttu-id="8c31a-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8c31a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="8c31a-113">La structure **IMECOLORSTY** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c31a-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a><span data-ttu-id="8c31a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c31a-114">Requirements</span></span>



| <span data-ttu-id="8c31a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c31a-115">Requirement</span></span> | <span data-ttu-id="8c31a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c31a-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c31a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8c31a-117">DLL</span></span><br/> | <dl> <span data-ttu-id="8c31a-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c31a-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c31a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c31a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c31a-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="8c31a-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 

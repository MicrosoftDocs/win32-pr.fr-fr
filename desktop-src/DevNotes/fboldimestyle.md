---
description: Spécifie si un style sans couleur a le style gras.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: FBoldIMEStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539301"
---
# <a name="fboldimestyle-function"></a><span data-ttu-id="711d7-103">FBoldIMEStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="711d7-103">FBoldIMEStyle function</span></span>

<span data-ttu-id="711d7-104">Spécifie si un style sans couleur a le style gras.</span><span class="sxs-lookup"><span data-stu-id="711d7-104">Specifies whether a non-color style has the bold style.</span></span>

## <a name="syntax"></a><span data-ttu-id="711d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="711d7-105">Syntax</span></span>


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="711d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="711d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711d7-107">*pimestyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="711d7-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711d7-108">Une structure **IMESTYLE** retournée par la fonction [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="711d7-108">An **IMESTYLE** structure returned from the [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711d7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="711d7-109">Return value</span></span>

<span data-ttu-id="711d7-110">**True** si le style est en gras.</span><span class="sxs-lookup"><span data-stu-id="711d7-110">**TRUE** if the style has the bold style.</span></span>

## <a name="remarks"></a><span data-ttu-id="711d7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="711d7-111">Remarks</span></span>

<span data-ttu-id="711d7-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="711d7-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="711d7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="711d7-113">Requirements</span></span>



| <span data-ttu-id="711d7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="711d7-114">Requirement</span></span> | <span data-ttu-id="711d7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="711d7-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="711d7-116">DLL</span><span class="sxs-lookup"><span data-stu-id="711d7-116">DLL</span></span><br/> | <dl> <span data-ttu-id="711d7-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711d7-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="711d7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="711d7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711d7-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="711d7-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 

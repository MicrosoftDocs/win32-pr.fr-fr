---
description: Spécifie si un style sans couleur a le style italique.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: FItalicIMEStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527323"
---
# <a name="fitalicimestyle-function"></a><span data-ttu-id="ffc2c-103">FItalicIMEStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="ffc2c-103">FItalicIMEStyle function</span></span>

<span data-ttu-id="ffc2c-104">Spécifie si un style sans couleur a le style italique.</span><span class="sxs-lookup"><span data-stu-id="ffc2c-104">Specifies whether a non-color style has the italic style.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffc2c-105">Syntax</span></span>


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="ffc2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffc2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffc2c-107">*pimestyle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffc2c-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc2c-108">Une structure **IMESTYLE** retournée par la fonction [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc2c-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffc2c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffc2c-109">Return value</span></span>

<span data-ttu-id="ffc2c-110">**True** si le style a le style Italic.</span><span class="sxs-lookup"><span data-stu-id="ffc2c-110">**TRUE** if the style has the italic style.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffc2c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ffc2c-111">Remarks</span></span>

<span data-ttu-id="ffc2c-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ffc2c-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffc2c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffc2c-113">Requirements</span></span>



| <span data-ttu-id="ffc2c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffc2c-114">Requirement</span></span> | <span data-ttu-id="ffc2c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffc2c-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc2c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ffc2c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ffc2c-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2c-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffc2c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffc2c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc2c-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="ffc2c-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 

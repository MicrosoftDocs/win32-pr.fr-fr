---
description: Initialise le partage IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: FInitIMEShare fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521617"
---
# <a name="finitimeshare-function"></a><span data-ttu-id="47475-103">FInitIMEShare fonction)</span><span class="sxs-lookup"><span data-stu-id="47475-103">FInitIMEShare function</span></span>

<span data-ttu-id="47475-104">Initialise le partage IME.</span><span class="sxs-lookup"><span data-stu-id="47475-104">Initializes IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="47475-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47475-105">Syntax</span></span>


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="47475-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47475-106">Parameters</span></span>

<span data-ttu-id="47475-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="47475-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47475-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47475-108">Return value</span></span>

<span data-ttu-id="47475-109">La fonction retourne **true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="47475-109">The function returns **TRUE** on success or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="47475-110">Notes</span><span class="sxs-lookup"><span data-stu-id="47475-110">Remarks</span></span>

<span data-ttu-id="47475-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="47475-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="47475-112">Cette fonction doit être appelée avant d’appeler toute autre fonction de partage IME.</span><span class="sxs-lookup"><span data-stu-id="47475-112">This function should be called before any other IME Share functions are called.</span></span>

## <a name="requirements"></a><span data-ttu-id="47475-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47475-113">Requirements</span></span>



| <span data-ttu-id="47475-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47475-114">Requirement</span></span> | <span data-ttu-id="47475-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47475-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47475-116">DLL</span><span class="sxs-lookup"><span data-stu-id="47475-116">DLL</span></span><br/> | <dl> <span data-ttu-id="47475-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47475-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47475-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47475-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47475-119">**EndIMEShare**</span><span class="sxs-lookup"><span data-stu-id="47475-119">**EndIMEShare**</span></span>](endimeshare.md)
</dt> </dl>

 

 

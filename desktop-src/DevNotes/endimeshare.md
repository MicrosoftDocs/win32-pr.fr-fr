---
description: Met fin au partage IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: EndIMEShare fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523025"
---
# <a name="endimeshare-function"></a><span data-ttu-id="3fc2e-103">EndIMEShare fonction)</span><span class="sxs-lookup"><span data-stu-id="3fc2e-103">EndIMEShare function</span></span>

<span data-ttu-id="3fc2e-104">Met fin au partage IME.</span><span class="sxs-lookup"><span data-stu-id="3fc2e-104">Terminates IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fc2e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fc2e-105">Syntax</span></span>


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="3fc2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fc2e-106">Parameters</span></span>

<span data-ttu-id="3fc2e-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3fc2e-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3fc2e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fc2e-108">Return value</span></span>

<span data-ttu-id="3fc2e-109">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3fc2e-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc2e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3fc2e-110">Remarks</span></span>

<span data-ttu-id="3fc2e-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3fc2e-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="3fc2e-112">Cette fonction doit être appelée après l’appel de la dernière fonction de partage IME.</span><span class="sxs-lookup"><span data-stu-id="3fc2e-112">This function should be called after the last IME Share function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc2e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fc2e-113">Requirements</span></span>



| <span data-ttu-id="3fc2e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fc2e-114">Requirement</span></span> | <span data-ttu-id="3fc2e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fc2e-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc2e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3fc2e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="3fc2e-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fc2e-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc2e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fc2e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc2e-119">**FInitIMEShare**</span><span class="sxs-lookup"><span data-stu-id="3fc2e-119">**FInitIMEShare**</span></span>](finitimeshare.md)
</dt> </dl>

 

 

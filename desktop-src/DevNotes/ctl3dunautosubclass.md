---
description: Désactive le sous-classement automatique.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Ctl3dUnAutoSubclass fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540040"
---
# <a name="ctl3dunautosubclass-function"></a><span data-ttu-id="40d4b-103">Ctl3dUnAutoSubclass fonction)</span><span class="sxs-lookup"><span data-stu-id="40d4b-103">Ctl3dUnAutoSubclass function</span></span>

<span data-ttu-id="40d4b-104">Désactive le sous-classement automatique.</span><span class="sxs-lookup"><span data-stu-id="40d4b-104">Turns off automatic subclassing.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d4b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40d4b-105">Syntax</span></span>


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a><span data-ttu-id="40d4b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40d4b-106">Parameters</span></span>

<span data-ttu-id="40d4b-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="40d4b-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40d4b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40d4b-108">Return value</span></span>

<span data-ttu-id="40d4b-109">Retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="40d4b-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d4b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="40d4b-110">Remarks</span></span>

<span data-ttu-id="40d4b-111">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="40d4b-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="40d4b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40d4b-112">Requirements</span></span>



| <span data-ttu-id="40d4b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40d4b-113">Requirement</span></span> | <span data-ttu-id="40d4b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="40d4b-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40d4b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="40d4b-115">DLL</span></span><br/> | <dl> <span data-ttu-id="40d4b-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d4b-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 

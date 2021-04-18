---
description: Ferme un handle de recherche.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540610"
---
# <a name="cscfindclose-function"></a><span data-ttu-id="7173b-103">CSCFindClose fonction)</span><span class="sxs-lookup"><span data-stu-id="7173b-103">CSCFindClose function</span></span>

<span data-ttu-id="7173b-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="7173b-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="7173b-105">Ferme un handle de recherche.</span><span class="sxs-lookup"><span data-stu-id="7173b-105">Closes a search handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="7173b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7173b-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a><span data-ttu-id="7173b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7173b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7173b-108">*hFind* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7173b-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7173b-109">Un handle de recherche retourné par la fonction [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="7173b-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7173b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7173b-110">Return value</span></span>

<span data-ttu-id="7173b-111">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="7173b-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7173b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7173b-112">Remarks</span></span>

<span data-ttu-id="7173b-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7173b-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7173b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7173b-114">Requirements</span></span>



| <span data-ttu-id="7173b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7173b-115">Requirement</span></span> | <span data-ttu-id="7173b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7173b-116">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7173b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7173b-117">DLL</span></span><br/> | <dl> <span data-ttu-id="7173b-118"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7173b-118"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7173b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7173b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7173b-120">**CSCFindFirstFileW**</span><span class="sxs-lookup"><span data-stu-id="7173b-120">**CSCFindFirstFileW**</span></span>](cscfindfirstfilew.md)
</dt> </dl>

 

 

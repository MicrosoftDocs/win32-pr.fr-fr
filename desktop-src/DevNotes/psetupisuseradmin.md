---
description: Indique si l’utilisateur actuel est un administrateur.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: pSetupIsUserAdmin fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534810"
---
# <a name="psetupisuseradmin-function"></a><span data-ttu-id="474fc-103">pSetupIsUserAdmin fonction)</span><span class="sxs-lookup"><span data-stu-id="474fc-103">pSetupIsUserAdmin function</span></span>

<span data-ttu-id="474fc-104">\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="474fc-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="474fc-105">Indique si l’utilisateur actuel est un administrateur.</span><span class="sxs-lookup"><span data-stu-id="474fc-105">Indicates whether the current user is an administrator.</span></span>

## <a name="syntax"></a><span data-ttu-id="474fc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="474fc-106">Syntax</span></span>


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a><span data-ttu-id="474fc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="474fc-107">Parameters</span></span>

<span data-ttu-id="474fc-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="474fc-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="474fc-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="474fc-109">Return value</span></span>

<span data-ttu-id="474fc-110">**True** si l’utilisateur actuel est un administrateur, sinon **false**.</span><span class="sxs-lookup"><span data-stu-id="474fc-110">**TRUE** if the current user is an administrator, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="474fc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="474fc-111">Remarks</span></span>

<span data-ttu-id="474fc-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="474fc-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="474fc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="474fc-113">Requirements</span></span>



| <span data-ttu-id="474fc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="474fc-114">Requirement</span></span> | <span data-ttu-id="474fc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="474fc-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="474fc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="474fc-116">DLL</span></span><br/> | <dl> <span data-ttu-id="474fc-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="474fc-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 

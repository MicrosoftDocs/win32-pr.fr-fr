---
description: Détermine si Fichiers hors connexion est activé.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: CSCIsCSCEnabled fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537818"
---
# <a name="csciscscenabled-function"></a><span data-ttu-id="28817-103">CSCIsCSCEnabled fonction)</span><span class="sxs-lookup"><span data-stu-id="28817-103">CSCIsCSCEnabled function</span></span>

<span data-ttu-id="28817-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="28817-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="28817-105">Détermine si Fichiers hors connexion est activé.</span><span class="sxs-lookup"><span data-stu-id="28817-105">Determines whether Offline Files is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="28817-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28817-106">Syntax</span></span>


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="28817-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28817-107">Parameters</span></span>

<span data-ttu-id="28817-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="28817-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28817-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28817-109">Return value</span></span>

<span data-ttu-id="28817-110">Cette fonction retourne la **valeur true** si fichiers hors connexion est activé et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="28817-110">This function returns **TRUE** if Offline Files is enabled and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="28817-111">Notes</span><span class="sxs-lookup"><span data-stu-id="28817-111">Remarks</span></span>

<span data-ttu-id="28817-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="28817-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="28817-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28817-113">Requirements</span></span>



| <span data-ttu-id="28817-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28817-114">Requirement</span></span> | <span data-ttu-id="28817-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="28817-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28817-116">DLL</span><span class="sxs-lookup"><span data-stu-id="28817-116">DLL</span></span><br/> | <dl> <span data-ttu-id="28817-117"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28817-117"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28817-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28817-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28817-119">**CSCQueryDatabaseStatus**</span><span class="sxs-lookup"><span data-stu-id="28817-119">**CSCQueryDatabaseStatus**</span></span>](cscquerydatabasestatus.md)
</dt> </dl>

 

 

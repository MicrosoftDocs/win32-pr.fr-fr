---
description: Recharge les paramètres de couleur à partir du Registre.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545458"
---
# <a name="frefreshstyle-function"></a><span data-ttu-id="703e7-103">FRefreshStyle fonction)</span><span class="sxs-lookup"><span data-stu-id="703e7-103">FRefreshStyle function</span></span>

<span data-ttu-id="703e7-104">Recharge les paramètres de couleur à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="703e7-104">Reloads color settings from registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="703e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="703e7-105">Syntax</span></span>


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a><span data-ttu-id="703e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="703e7-106">Parameters</span></span>

<span data-ttu-id="703e7-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="703e7-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="703e7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="703e7-108">Return value</span></span>

<span data-ttu-id="703e7-109">Retourne la valeur TRUE en cas de réussite ; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="703e7-109">Returns TRUE on success; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="703e7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="703e7-110">Remarks</span></span>

<span data-ttu-id="703e7-111">Cette fonction n’est pas associée à une bibliothèque d’importation ou un fichier d’en-tête ; elle doit être appelée à l’aide des fonctions [**LoadLibrary**](-loadlibrary.md) et [**GetProcAddress**](-getprocaddress-.md) .</span><span class="sxs-lookup"><span data-stu-id="703e7-111">This function is not associated with an import library or header file; it must be called using the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="703e7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="703e7-112">Requirements</span></span>



| <span data-ttu-id="703e7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="703e7-113">Requirement</span></span> | <span data-ttu-id="703e7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="703e7-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="703e7-115">DLL</span><span class="sxs-lookup"><span data-stu-id="703e7-115">DLL</span></span><br/> | <dl> <span data-ttu-id="703e7-116"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="703e7-116"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="703e7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="703e7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="703e7-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="703e7-118">**GetProcAddress**</span></span>](-getprocaddress-.md)
</dt> <dt>

[<span data-ttu-id="703e7-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="703e7-119">**LoadLibrary**</span></span>](-loadlibrary.md)
</dt> </dl>

 

 





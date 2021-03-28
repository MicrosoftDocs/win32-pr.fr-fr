---
description: Cette fonction active ou désactive la prise en charge des caractères définis par l’utilisateur final (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972687"
---
# <a name="enableeudc-function"></a><span data-ttu-id="3a418-103">EnableEUDC fonction)</span><span class="sxs-lookup"><span data-stu-id="3a418-103">EnableEUDC function</span></span>

<span data-ttu-id="3a418-104">Cette fonction active ou désactive la prise en charge des caractères définis par l’utilisateur final (EUDC).</span><span class="sxs-lookup"><span data-stu-id="3a418-104">This function enables or disables support for end-user-defined characters (EUDC).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a418-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a418-105">Syntax</span></span>


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a><span data-ttu-id="3a418-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a418-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a418-107">*fEnableEUDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a418-107">*fEnableEUDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a418-108">Valeur booléenne qui a la valeur **true** pour activer EUDC et la valeur **false** pour désactiver EUDC.</span><span class="sxs-lookup"><span data-stu-id="3a418-108">Boolean that is set to **TRUE** to enable EUDC, and to **FALSE** to disable EUDC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a418-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a418-109">Return value</span></span>

<span data-ttu-id="3a418-110">Si la fonction réussit, la valeur de retour est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3a418-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="3a418-111">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="3a418-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a418-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3a418-112">Remarks</span></span>

<span data-ttu-id="3a418-113">Si EUDC est désactivé, toute tentative d’affichage des caractères EUDC entraîne des glyphes manquants ou incorrects.</span><span class="sxs-lookup"><span data-stu-id="3a418-113">If EUDC is disabled, trying to display EUDC characters will result in missing or bad glyphs.</span></span>

<span data-ttu-id="3a418-114">Pendant la session multisession, cette fonction affecte uniquement la session active.</span><span class="sxs-lookup"><span data-stu-id="3a418-114">During multi-session, this function affects the current session only.</span></span>

<span data-ttu-id="3a418-115">Il est recommandé d’utiliser cette fonction avec Windows XP SP2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3a418-115">It is recommended that you use this function with Windows XP SP2 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a418-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a418-116">Requirements</span></span>



| <span data-ttu-id="3a418-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a418-117">Requirement</span></span> | <span data-ttu-id="3a418-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a418-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a418-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a418-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3a418-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a418-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3a418-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a418-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3a418-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a418-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3a418-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a418-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a418-124"><dt>GDI32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a418-124"><dt>Gdi32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3a418-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3a418-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a418-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a418-126"><dt>Gdi32.dll</dt></span></span> </dl> |



 

 





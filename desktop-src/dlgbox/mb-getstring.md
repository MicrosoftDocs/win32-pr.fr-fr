---
title: MB_GetString fonction (User. h)
description: Retourne des chaînes pour les boutons de boîte de message standard.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Boîtes de dialogue de MB_GetString fonction
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541597"
---
# <a name="mb_getstring-function"></a><span data-ttu-id="86563-104">\_Fonction GetString de MB</span><span class="sxs-lookup"><span data-stu-id="86563-104">MB\_GetString function</span></span>

<span data-ttu-id="86563-105">Retourne des chaînes pour les boutons de boîte de message standard.</span><span class="sxs-lookup"><span data-stu-id="86563-105">Returns strings for standard message box buttons.</span></span>

## <a name="syntax"></a><span data-ttu-id="86563-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86563-106">Syntax</span></span>


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a><span data-ttu-id="86563-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86563-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86563-108">*wBtn*</span><span class="sxs-lookup"><span data-stu-id="86563-108">*wBtn*</span></span> 
</dt> <dd>

<span data-ttu-id="86563-109">ID de la chaîne à retourner.</span><span class="sxs-lookup"><span data-stu-id="86563-109">The id of the string to return.</span></span> <span data-ttu-id="86563-110">Celles-ci sont identifiées par les valeurs d’ID de commande de la boîte de dialogue répertoriées dans winuser. h.</span><span class="sxs-lookup"><span data-stu-id="86563-110">These are identified by the Dialog Box Command ID values listed in winuser.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86563-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86563-111">Return value</span></span>

<span data-ttu-id="86563-112">Chaîne, ou NULL si introuvable.</span><span class="sxs-lookup"><span data-stu-id="86563-112">The string, or NULL if not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="86563-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86563-113">Requirements</span></span>



| <span data-ttu-id="86563-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86563-114">Requirement</span></span> | <span data-ttu-id="86563-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="86563-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86563-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="86563-116">Header</span></span><br/>  | <dl> <span data-ttu-id="86563-117"><dt>User. h</dt></span><span class="sxs-lookup"><span data-stu-id="86563-117"><dt>User.h</dt></span></span> </dl>     |
| <span data-ttu-id="86563-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86563-118">Library</span></span><br/> | <dl> <span data-ttu-id="86563-119"><dt>User32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86563-119"><dt>User32.lib</dt></span></span> </dl> |
| <span data-ttu-id="86563-120">DLL</span><span class="sxs-lookup"><span data-stu-id="86563-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="86563-121"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86563-121"><dt>User32.dll</dt></span></span> </dl> |



 

 






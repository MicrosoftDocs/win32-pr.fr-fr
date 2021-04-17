---
description: Récupère le nom complet de la BALIse spécifiée.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483121"
---
# <a name="sdbtagtostring-function"></a><span data-ttu-id="d85ea-103">SdbTagToString fonction)</span><span class="sxs-lookup"><span data-stu-id="d85ea-103">SdbTagToString function</span></span>

<span data-ttu-id="d85ea-104">Récupère le nom complet de la BALIse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d85ea-104">Retrieves the display name of the specified TAG.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d85ea-105">Syntax</span></span>


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a><span data-ttu-id="d85ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d85ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d85ea-107">*balise* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d85ea-107">*tag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d85ea-108">BALIse.</span><span class="sxs-lookup"><span data-stu-id="d85ea-108">The TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d85ea-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d85ea-109">Return value</span></span>

<span data-ttu-id="d85ea-110">La fonction retourne un pointeur vers la chaîne se terminant par null ou « InvalidTag ».</span><span class="sxs-lookup"><span data-stu-id="d85ea-110">The function returns a pointer to the null-terminated string or "InvalidTag".</span></span>

## <a name="requirements"></a><span data-ttu-id="d85ea-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d85ea-111">Requirements</span></span>



| <span data-ttu-id="d85ea-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d85ea-112">Requirement</span></span> | <span data-ttu-id="d85ea-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d85ea-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d85ea-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d85ea-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d85ea-115">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d85ea-115">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d85ea-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d85ea-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d85ea-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d85ea-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d85ea-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d85ea-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d85ea-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d85ea-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d85ea-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d85ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85ea-121">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d85ea-121">**TAG**</span></span>](tag.md)
</dt> </dl>

 

 





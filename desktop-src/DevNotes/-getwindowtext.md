---
description: Récupère le texte de la barre de titre de la fenêtre spécifiée.
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: _GetWindowText fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 61c84c8a5f00ad97b8a76ef4139b20b74f1be085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545383"
---
# <a name="_getwindowtext-function"></a><span data-ttu-id="3d1e6-103">\_GetWindowText, fonction</span><span class="sxs-lookup"><span data-stu-id="3d1e6-103">\_GetWindowText function</span></span>

<span data-ttu-id="3d1e6-104">\[Cette fonction est un wrapper sur la fonction **GetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="3d1e6-104">\[This function is a wrapper over the **GetWindowText** function.</span></span> <span data-ttu-id="3d1e6-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3d1e6-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="3d1e6-106">Les applications doivent appeler **GetWindowText** directement.\]</span><span class="sxs-lookup"><span data-stu-id="3d1e6-106">Applications should call **GetWindowText** directly.\]</span></span>

<span data-ttu-id="3d1e6-107">Récupère le texte de la barre de titre de la fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3d1e6-107">Retrieves the text from the specified window's title bar.</span></span> <span data-ttu-id="3d1e6-108">Consultez [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="3d1e6-108">See [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1e6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d1e6-109">Syntax</span></span>


```C++
int _GetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="3d1e6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d1e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d1e6-111">*...*</span><span class="sxs-lookup"><span data-stu-id="3d1e6-111">*...*</span></span> 
<span data-ttu-id="3d1e6-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3d1e6-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3d1e6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d1e6-113">Requirements</span></span>



| <span data-ttu-id="3d1e6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d1e6-114">Requirement</span></span> | <span data-ttu-id="3d1e6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d1e6-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1e6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3d1e6-116">DLL</span></span><br/> | <dl> <span data-ttu-id="3d1e6-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d1e6-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1e6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d1e6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1e6-119">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="3d1e6-119">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 

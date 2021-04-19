---
description: Modifie le texte de la barre de titre de la fenêtre spécifiée (le cas échéant).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: _SetWindowText fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537645"
---
# <a name="_setwindowtext-function"></a><span data-ttu-id="94d73-103">\_SetWindowText fonction)</span><span class="sxs-lookup"><span data-stu-id="94d73-103">\_SetWindowText function</span></span>

<span data-ttu-id="94d73-104">\[Cette fonction est un wrapper sur la fonction **SetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="94d73-104">\[This function is a wrapper over the **SetWindowText** function.</span></span> <span data-ttu-id="94d73-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="94d73-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="94d73-106">Les applications doivent appeler **SetWindowText** directement.\]</span><span class="sxs-lookup"><span data-stu-id="94d73-106">Applications should call **SetWindowText** directly.\]</span></span>

<span data-ttu-id="94d73-107">Modifie le texte de la barre de titre de la fenêtre spécifiée (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="94d73-107">Changes the text of the specified window's title bar (if it has one).</span></span> <span data-ttu-id="94d73-108">Consultez [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="94d73-108">See [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="94d73-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94d73-109">Syntax</span></span>


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="94d73-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94d73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d73-111">*...*</span><span class="sxs-lookup"><span data-stu-id="94d73-111">*...*</span></span> 
<span data-ttu-id="94d73-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="94d73-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="94d73-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94d73-113">Requirements</span></span>



| <span data-ttu-id="94d73-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94d73-114">Requirement</span></span> | <span data-ttu-id="94d73-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="94d73-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d73-116">DLL</span><span class="sxs-lookup"><span data-stu-id="94d73-116">DLL</span></span><br/> | <dl> <span data-ttu-id="94d73-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94d73-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d73-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94d73-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d73-119">**SetWindowText**</span><span class="sxs-lookup"><span data-stu-id="94d73-119">**SetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 

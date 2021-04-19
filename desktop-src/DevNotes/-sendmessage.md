---
description: Envoie le message spécifié à une fenêtre ou à des fenêtres.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523511"
---
# <a name="_sendmessage-function"></a><span data-ttu-id="09ce0-103">\_SendMessage, fonction</span><span class="sxs-lookup"><span data-stu-id="09ce0-103">\_SendMessage function</span></span>

<span data-ttu-id="09ce0-104">\[Cette fonction est un wrapper sur la fonction **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="09ce0-104">\[This function is a wrapper over the **SendMessage** function.</span></span> <span data-ttu-id="09ce0-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="09ce0-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="09ce0-106">Les applications doivent appeler **SendMessage** directement.\]</span><span class="sxs-lookup"><span data-stu-id="09ce0-106">Applications should call **SendMessage** directly.\]</span></span>

<span data-ttu-id="09ce0-107">Envoie le message spécifié à une fenêtre ou à des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="09ce0-107">Sends the specified message to a window or windows.</span></span> <span data-ttu-id="09ce0-108">Consultez [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="09ce0-108">See [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="09ce0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09ce0-109">Syntax</span></span>


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="09ce0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09ce0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09ce0-111">*...*</span><span class="sxs-lookup"><span data-stu-id="09ce0-111">*...*</span></span> 
<span data-ttu-id="09ce0-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="09ce0-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="09ce0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09ce0-113">Requirements</span></span>



| <span data-ttu-id="09ce0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09ce0-114">Requirement</span></span> | <span data-ttu-id="09ce0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="09ce0-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09ce0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="09ce0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="09ce0-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09ce0-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ce0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09ce0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ce0-119">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="09ce0-119">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 

---
description: Distribue les messages entrants envoyés, vérifie la file d’attente de messages de thread pour un message publié et récupère le message (le cas échéant).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532779"
---
# <a name="_peekmessage-function"></a><span data-ttu-id="1cc6d-103">\_PeekMessage, fonction</span><span class="sxs-lookup"><span data-stu-id="1cc6d-103">\_PeekMessage function</span></span>

<span data-ttu-id="1cc6d-104">\[Cette fonction est un wrapper sur la fonction **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="1cc6d-104">\[This function is a wrapper over the **PeekMessage** function.</span></span> <span data-ttu-id="1cc6d-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="1cc6d-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="1cc6d-106">Les applications doivent appeler **PeekMessage** directement.\]</span><span class="sxs-lookup"><span data-stu-id="1cc6d-106">Applications should call **PeekMessage** directly.\]</span></span>

<span data-ttu-id="1cc6d-107">Distribue les messages entrants envoyés, vérifie la file d’attente de messages de thread pour un message publié et récupère le message (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="1cc6d-107">Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).</span></span> <span data-ttu-id="1cc6d-108">Consultez [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="1cc6d-108">See [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc6d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cc6d-109">Syntax</span></span>


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="1cc6d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cc6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc6d-111">*...*</span><span class="sxs-lookup"><span data-stu-id="1cc6d-111">*...*</span></span> 
<span data-ttu-id="1cc6d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1cc6d-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1cc6d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cc6d-113">Requirements</span></span>



| <span data-ttu-id="1cc6d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cc6d-114">Requirement</span></span> | <span data-ttu-id="1cc6d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cc6d-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc6d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1cc6d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1cc6d-117"><dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc6d-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc6d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cc6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc6d-119">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="1cc6d-119">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 

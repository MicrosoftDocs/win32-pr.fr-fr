---
description: La fonction DestroyProtocol détruit le protocole créé par la fonction CreateProtocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: DestroyProtocol, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202726"
---
# <a name="destroyprotocol-function"></a><span data-ttu-id="bcbc5-103">DestroyProtocol fonction)</span><span class="sxs-lookup"><span data-stu-id="bcbc5-103">DestroyProtocol function</span></span>

<span data-ttu-id="bcbc5-104">La fonction **DestroyProtocol** détruit le protocole créé par la fonction **CreateProtocol** .</span><span class="sxs-lookup"><span data-stu-id="bcbc5-104">The **DestroyProtocol** function destroys the protocol that the **CreateProtocol** function creates.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcbc5-105">Syntax</span></span>


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="bcbc5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcbc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcbc5-107">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcbc5-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbc5-108">Handle du protocole à détruire.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-108">Handle to the protocol to be destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcbc5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcbc5-109">Return value</span></span>

<span data-ttu-id="bcbc5-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbc5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bcbc5-111">Remarks</span></span>

<span data-ttu-id="bcbc5-112">La DLL de l’analyseur appelle la fonction **DestroyProtocol** lors de son implémentation de [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="bcbc5-112">The parser DLL calls the **DestroyProtocol** function during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="bcbc5-113">**DestroyProtocol** est appelé quand le système d’exploitation va décharger la dll.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-113">**DestroyProtocol** is called when the operating system is going to unload the DLL.</span></span>



| <span data-ttu-id="bcbc5-114">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="bcbc5-114">For information on</span></span>                                        | <span data-ttu-id="bcbc5-115">Consultez</span><span class="sxs-lookup"><span data-stu-id="bcbc5-115">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bcbc5-116">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-116">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="bcbc5-117">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="bcbc5-117">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="bcbc5-118">L’implémentation de **DllMain** comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-118">How to implement **DllMain** includes an example.</span></span>         | [<span data-ttu-id="bcbc5-119">Implémentation de DllMain</span><span class="sxs-lookup"><span data-stu-id="bcbc5-119">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="bcbc5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcbc5-120">Requirements</span></span>



| <span data-ttu-id="bcbc5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcbc5-121">Requirement</span></span> | <span data-ttu-id="bcbc5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcbc5-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbc5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcbc5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbc5-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcbc5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bcbc5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcbc5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbc5-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcbc5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bcbc5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcbc5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcbc5-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcbc5-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bcbc5-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bcbc5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="bcbc5-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcbc5-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bcbc5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bcbc5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcbc5-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcbc5-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbc5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcbc5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbc5-134">DllMain</span><span class="sxs-lookup"><span data-stu-id="bcbc5-134">DllMain</span></span>](dllmain-parser.md)
</dt> </dl>

 

 





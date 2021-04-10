---
description: La fonction CreateProtocol notifie Moniteur réseau qu’un analyseur de protocole spécifique existe.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: CreateProtocol, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115742"
---
# <a name="createprotocol-function"></a><span data-ttu-id="72921-103">CreateProtocol fonction)</span><span class="sxs-lookup"><span data-stu-id="72921-103">CreateProtocol function</span></span>

<span data-ttu-id="72921-104">La fonction **CreateProtocol** notifie Moniteur réseau qu’un analyseur de protocole spécifique existe.</span><span class="sxs-lookup"><span data-stu-id="72921-104">The **CreateProtocol** function notifies Network Monitor that a specific protocol parser exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="72921-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72921-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a><span data-ttu-id="72921-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72921-107">*ProtocolName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72921-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72921-108">Nom du protocole détecté par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="72921-108">Name of the protocol the parser will detect.</span></span>

</dd> <dt>

<span data-ttu-id="72921-109">*lpEntryPoints* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72921-109">*lpEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72921-110">Structure [ENTRYPOINTS](entrypoints.md) qui contient les autres points d’entrée de la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="72921-110">An [ENTRYPOINTS](entrypoints.md) structure that contains the remaining parser DLL entry points.</span></span> <span data-ttu-id="72921-111">Consultez la section Notes pour obtenir la liste des fonctions d’exportation auxquelles chaque point d’entrée fait référence.</span><span class="sxs-lookup"><span data-stu-id="72921-111">See Remarks for a list of the export functions that each entry point references.</span></span> <span data-ttu-id="72921-112">Les points d’entrée doivent être fournis dans l’ordre spécifié par la structure **ENTRYPOINTS** .</span><span class="sxs-lookup"><span data-stu-id="72921-112">Entry points must be provided in the order that the **ENTRYPOINTS** structure specifies.</span></span>

</dd> <dt>

<span data-ttu-id="72921-113">*cbEntryPoints* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72921-113">*cbEntryPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72921-114">Taille de la structure **ENTRYPOINTS** .</span><span class="sxs-lookup"><span data-stu-id="72921-114">The size of the **ENTRYPOINTS** structure.</span></span> <span data-ttu-id="72921-115">Moniteur réseau fournit une \_ macro de taille ENTRYPOINTS que vous pouvez utiliser pour spécifier la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="72921-115">Network Monitor provides an ENTRYPOINTS\_SIZE macro that you can use to specify the size of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72921-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72921-116">Return value</span></span>

<span data-ttu-id="72921-117">Si la fonction réussit, la valeur de retour est un handle vers le protocole.</span><span class="sxs-lookup"><span data-stu-id="72921-117">If the function is successful, the return value is a handle to the protocol.</span></span>

<span data-ttu-id="72921-118">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="72921-118">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="72921-119">Notes</span><span class="sxs-lookup"><span data-stu-id="72921-119">Remarks</span></span>

<span data-ttu-id="72921-120">La DLL de l’analyseur appelle **CreateProtocol** pendant son implémentation de [DllMain](dllmain-parser.md).</span><span class="sxs-lookup"><span data-stu-id="72921-120">The parser DLL calls **CreateProtocol** during its implementation of [DllMain](dllmain-parser.md).</span></span> <span data-ttu-id="72921-121">La fonction **CreateProtocol** est appelée quand le système d’exploitation charge la dll de l’analyseur pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="72921-121">The **CreateProtocol** function is called when the operating system loads the parser DLL for the first time.</span></span>

<span data-ttu-id="72921-122">Les points d’entrée référencés dans le paramètre *lpEntryPoints* incluent des pointeurs vers les fonctions d’exportation suivantes qui doivent être fournies dans l’ordre présenté ici.</span><span class="sxs-lookup"><span data-stu-id="72921-122">The entry points referenced in the *lpEntryPoints* parameter include pointers to the following export functions that must be provided in the order presented here.</span></span>

-   [<span data-ttu-id="72921-123">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="72921-123">Register</span></span>](register-parser.md)
-   [<span data-ttu-id="72921-124">Désinscrire</span><span class="sxs-lookup"><span data-stu-id="72921-124">Deregister</span></span>](deregister.md)
-   [<span data-ttu-id="72921-125">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="72921-125">RecognizeFrame</span></span>](recognizeframe.md)
-   [<span data-ttu-id="72921-126">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="72921-126">AttachProperties</span></span>](attachproperties.md)
-   [<span data-ttu-id="72921-127">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="72921-127">FormatProperties</span></span>](formatproperties.md)



| <span data-ttu-id="72921-128">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="72921-128">For information on</span></span>                                                                                 | <span data-ttu-id="72921-129">Consultez</span><span class="sxs-lookup"><span data-stu-id="72921-129">See</span></span>                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="72921-130">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="72921-130">What parsers are, and how they work with Network Monitor.</span></span>                                          | [<span data-ttu-id="72921-131">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="72921-131">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="72921-132">La procédure d’implémentation de **DllMain** comprend un exemple d’appel de **CreateProtocol** dans **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="72921-132">How to implement **DllMain** includes an example of calling **CreateProtocol** within **DllMain**.</span></span> | [<span data-ttu-id="72921-133">Implémentation de DllMain</span><span class="sxs-lookup"><span data-stu-id="72921-133">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="72921-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72921-134">Requirements</span></span>



| <span data-ttu-id="72921-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72921-135">Requirement</span></span> | <span data-ttu-id="72921-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="72921-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72921-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72921-137">Minimum supported client</span></span><br/> | <span data-ttu-id="72921-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72921-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="72921-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72921-139">Minimum supported server</span></span><br/> | <span data-ttu-id="72921-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72921-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="72921-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="72921-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="72921-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="72921-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="72921-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72921-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="72921-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72921-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="72921-145">DLL</span><span class="sxs-lookup"><span data-stu-id="72921-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72921-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72921-146"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72921-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72921-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72921-148">DllMain</span><span class="sxs-lookup"><span data-stu-id="72921-148">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 


---
description: La fonction d’exportation DllMain de l’analyseur identifie l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour l’analyseur. DllMain doit être implémenté dans toutes les dll de l’analyseur.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Fonction de rappel de l’analyseur DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538906"
---
# <a name="dllmain-parser-callback-function"></a><span data-ttu-id="1f343-104">Fonction de rappel de l’analyseur DllMain</span><span class="sxs-lookup"><span data-stu-id="1f343-104">DllMain Parser callback function</span></span>

<span data-ttu-id="1f343-105">La fonction d’exportation **DllMain** de l’analyseur identifie l’existence de l’analyseur et libère les ressources que Moniteur réseau utilise pour l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="1f343-105">The **DllMain** export function for the parser identifies the existence of the parser, and releases resources that Network Monitor uses for the parser.</span></span> <span data-ttu-id="1f343-106">**DllMain** doit être implémenté dans toutes les dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="1f343-106">**DllMain** must be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f343-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f343-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="1f343-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f343-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f343-109">*HINSTANCE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f343-109">*hInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f343-110">Handle vers une instance de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="1f343-110">Handle to an instance of the parser.</span></span>

</dd> <dt>

<span data-ttu-id="1f343-111">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f343-111">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f343-112">Indicateur pour déterminer la raison pour laquelle la fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="1f343-112">Indicator to determine why the function is called.</span></span> <span data-ttu-id="1f343-113">Pour obtenir la liste de tous les indicateurs possibles, consultez [DllMain](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="1f343-113">For a list of all possible flags, see [DllMain](/windows/desktop/Dlls/dllmain).</span></span> <span data-ttu-id="1f343-114">L’implémentation de l’analyseur doit traiter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f343-114">The parser implementation must process the following values.</span></span>



| <span data-ttu-id="1f343-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f343-115">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="1f343-116">Signification</span><span class="sxs-lookup"><span data-stu-id="1f343-116">Meaning</span></span>                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <span data-ttu-id="1f343-117"><dt>**\_attachement du processus dll \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f343-117"><dt>**DLL\_PROCESS\_ATTACH**</dt></span></span> </dl> | <span data-ttu-id="1f343-118">Quand **DllMain** est appelée pour la première fois, la dll doit appeler [CreateProtocol](createprotocol.md) pour fournir des informations à Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="1f343-118">When **DllMain** is called for the first time, the DLL must call [CreateProtocol](createprotocol.md) to provide information to Network Monitor.</span></span> <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <span data-ttu-id="1f343-119"><dt>**\_détachement de processus dll \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f343-119"><dt>**DLL\_PROCESS\_DETACH**</dt></span></span> </dl> | <span data-ttu-id="1f343-120">Quand **DllMain** est appelée pour la dernière fois, la dll doit appeler [DestroyProtocol](destroyprotocol.md) pour libérer les ressources utilisées par la dll.</span><span class="sxs-lookup"><span data-stu-id="1f343-120">When **DllMain** is called for the last time, the DLL must call [DestroyProtocol](destroyprotocol.md) to release the resources that the DLL uses.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="1f343-121">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="1f343-121">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="1f343-122">Non utilisé maintenant.</span><span class="sxs-lookup"><span data-stu-id="1f343-122">Not used now.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f343-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f343-123">Return value</span></span>

<span data-ttu-id="1f343-124">La DLL de l’analyseur retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1f343-124">The parser DLL always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f343-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1f343-125">Remarks</span></span>

<span data-ttu-id="1f343-126">Le système d’exploitation appelle **DllMain** pour charger et décharger la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="1f343-126">The operating system calls **DllMain** to load and unload the parser DLL.</span></span> <span data-ttu-id="1f343-127">Cette fonction est basée sur la fonction [DllMain](/windows/desktop/Dlls/dllmain) de la bibliothèque de liens dynamiques.</span><span class="sxs-lookup"><span data-stu-id="1f343-127">This function is based on the dynamic-link library [DllMain](/windows/desktop/Dlls/dllmain) function.</span></span>

<span data-ttu-id="1f343-128">Vous pouvez également utiliser l’implémentation de **DllMain** pour stocker une instance d’un analyseur pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1f343-128">You can also use the implementation of **DllMain** to store an instance of a parser for use in the future.</span></span> <span data-ttu-id="1f343-129">Par exemple, vous pouvez stocker une instance de DLL de l’analyseur, puis l’utiliser pour un appel système à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="1f343-129">For example, you can store a parser DLL instance, and then use it for a system call in the future.</span></span>



| <span data-ttu-id="1f343-130">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="1f343-130">For information on</span></span>                                        | <span data-ttu-id="1f343-131">Consultez</span><span class="sxs-lookup"><span data-stu-id="1f343-131">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1f343-132">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="1f343-132">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="1f343-133">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="1f343-133">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="1f343-134">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="1f343-134">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="1f343-135">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="1f343-135">Parser DLL Architecture</span></span>](parser-dll-architecture.md)  |
| <span data-ttu-id="1f343-136">L’implémentation de **DllMain**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="1f343-136">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="1f343-137">Implémentation de DllMain</span><span class="sxs-lookup"><span data-stu-id="1f343-137">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="1f343-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f343-138">Requirements</span></span>



| <span data-ttu-id="1f343-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f343-139">Requirement</span></span> | <span data-ttu-id="1f343-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f343-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f343-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f343-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1f343-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f343-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1f343-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f343-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1f343-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f343-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1f343-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f343-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f343-146"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f343-146"><dt>Process.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f343-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f343-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f343-148">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="1f343-148">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="1f343-149">DestroyProtocol</span><span class="sxs-lookup"><span data-stu-id="1f343-149">DestroyProtocol</span></span>](destroyprotocol.md)
</dt> <dt>

[<span data-ttu-id="1f343-150">DllMain</span><span class="sxs-lookup"><span data-stu-id="1f343-150">DllMain</span></span>](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 


---
description: La structure ENTRYPOINTS définit les points d’entrée pour les fonctions d’exportation que Moniteur réseau utilise pour exécuter l’analyseur.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: ENTRYPOINTS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950980"
---
# <a name="entrypoints-structure"></a><span data-ttu-id="e2c0b-103">ENTRYPOINTS, structure</span><span class="sxs-lookup"><span data-stu-id="e2c0b-103">ENTRYPOINTS structure</span></span>

<span data-ttu-id="e2c0b-104">La structure **ENTRYPOINTS** définit les points d’entrée pour les fonctions d’exportation que Moniteur réseau utilise pour exécuter l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="e2c0b-104">The **ENTRYPOINTS** structure defines the entry points to the export functions that Network Monitor uses to operate the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c0b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2c0b-105">Syntax</span></span>


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a><span data-ttu-id="e2c0b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e2c0b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2c0b-107">**S’inscrire**</span><span class="sxs-lookup"><span data-stu-id="e2c0b-107">**Register**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0b-108">Pointeur vers l’implémentation de la fonction d' [*expert d’inscription*](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="e2c0b-108">Pointer to the implementation of the [*Register expert*](register-expert.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0b-109">**Désinscrire**</span><span class="sxs-lookup"><span data-stu-id="e2c0b-109">**Deregister**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0b-110">Pointeur vers l’implémentation de la fonction de [**désinscription**](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="e2c0b-110">Pointer to the implementation of the [**Deregister**](deregister.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0b-111">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="e2c0b-111">**RecognizeFrame**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0b-112">Pointeur vers l’implémentation de la fonction d’exportation [**RecognizeFrame**](recognizeframe.md) .</span><span class="sxs-lookup"><span data-stu-id="e2c0b-112">Pointer to the implementation of the [**RecognizeFrame**](recognizeframe.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0b-113">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="e2c0b-113">**AttachProperties**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0b-114">Pointeur vers l’implémentation de la fonction d’exportation [**AttachProperties**](attachproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="e2c0b-114">Pointer to the implementation of the [**AttachProperties**](attachproperties.md) export function.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0b-115">**FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="e2c0b-115">**FormatProperties**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0b-116">Pointeur vers l’implémentation de la fonction d’exportation [**FormatProperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="e2c0b-116">Pointer to the implementation of the [**FormatProperties**](formatproperties.md) export function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2c0b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e2c0b-117">Remarks</span></span>

<span data-ttu-id="e2c0b-118">La fonction **CreateProtocol** utilise la structure **ENTRYPOINTS** pour fournir des pointeurs vers Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e2c0b-118">The **CreateProtocol** function uses the **ENTRYPOINTS** structure to provide pointers to Network Monitor.</span></span> <span data-ttu-id="e2c0b-119">Les pointeurs doivent être spécifiés dans l’ordre identifié dans la section membres précédents.</span><span class="sxs-lookup"><span data-stu-id="e2c0b-119">The pointers must be specified in the order identified in the previous Members section.</span></span>

<span data-ttu-id="e2c0b-120">La fonction [**FormatProperties**](formatproperties.md) n’a pas besoin d’être implémentée si Moniteur réseau n’affichera jamais les données de protocole.</span><span class="sxs-lookup"><span data-stu-id="e2c0b-120">The [**FormatProperties**](formatproperties.md) function does not need to be implemented if Network Monitor will never display the protocol data.</span></span> <span data-ttu-id="e2c0b-121">Par exemple, **FormatProperties** n’a pas besoin d’être implémenté si une application d’exportation utilise la sortie de l’analyseur, et moniteur réseau n’affiche pas la sortie.</span><span class="sxs-lookup"><span data-stu-id="e2c0b-121">For example, **FormatProperties** does not need to be implemented if an export application uses the output from the parser, and Network Monitor does not display the output.</span></span>



| <span data-ttu-id="e2c0b-122">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="e2c0b-122">For information on</span></span>                                        | <span data-ttu-id="e2c0b-123">Consultez</span><span class="sxs-lookup"><span data-stu-id="e2c0b-123">See</span></span>                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e2c0b-124">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="e2c0b-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="e2c0b-125">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="e2c0b-125">Parsers</span></span>](parsers.md)                                  |
| <span data-ttu-id="e2c0b-126">L’implémentation de **DllMain**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="e2c0b-126">How to implement **DllMain**  includes an example.</span></span>        | [<span data-ttu-id="e2c0b-127">Implémentation de DllMain</span><span class="sxs-lookup"><span data-stu-id="e2c0b-127">Implementing DllMain</span></span>](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a><span data-ttu-id="e2c0b-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2c0b-128">Requirements</span></span>



| <span data-ttu-id="e2c0b-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2c0b-129">Requirement</span></span> | <span data-ttu-id="e2c0b-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2c0b-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c0b-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2c0b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c0b-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2c0b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e2c0b-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2c0b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c0b-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2c0b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e2c0b-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2c0b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2c0b-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c0b-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2c0b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2c0b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c0b-138">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="e2c0b-138">AttachProperties</span></span>](attachproperties.md)
</dt> <dt>

[<span data-ttu-id="e2c0b-139">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="e2c0b-139">CreateProtocol</span></span>](createprotocol.md)
</dt> <dt>

[<span data-ttu-id="e2c0b-140">Désinscrire</span><span class="sxs-lookup"><span data-stu-id="e2c0b-140">Deregister</span></span>](deregister.md)
</dt> <dt>

[<span data-ttu-id="e2c0b-141">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="e2c0b-141">FormatProperties</span></span>](formatproperties.md)
</dt> <dt>

[<span data-ttu-id="e2c0b-142">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="e2c0b-142">RecognizeFrame</span></span>](recognizeframe.md)
</dt> <dt>

[<span data-ttu-id="e2c0b-143">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="e2c0b-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 





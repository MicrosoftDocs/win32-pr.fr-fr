---
description: La \_ structure PARSERINFO de PF définit un analyseur à la fois. Dans la \_ structure PARSERINFO de PF, un analyseur est défini par les informations relatives au protocole détecté par l’analyseur.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Structure de PF_PARSERINFO (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519409"
---
# <a name="pf_parserinfo-structure"></a><span data-ttu-id="a9122-104">PF \_ PARSERINFO, structure</span><span class="sxs-lookup"><span data-stu-id="a9122-104">PF\_PARSERINFO structure</span></span>

<span data-ttu-id="a9122-105">La **structure \_ PARSERINFO de PF** définit un analyseur à la fois.</span><span class="sxs-lookup"><span data-stu-id="a9122-105">The **PF\_PARSERINFO** structure defines one parser at a time.</span></span> <span data-ttu-id="a9122-106">Dans la **structure \_ PARSERINFO de PF** , un analyseur est défini par les informations relatives au protocole détecté par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="a9122-106">In the **PF\_PARSERINFO** structure, a parser is defined by the information about the protocol that the parser detects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9122-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9122-107">Syntax</span></span>


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a><span data-ttu-id="a9122-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a9122-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9122-109">**szProtocolName**</span><span class="sxs-lookup"><span data-stu-id="a9122-109">**szProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="a9122-110">Nom du protocole détecté par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="a9122-110">Name of the protocol that the parser detects.</span></span>

</dd> <dt>

<span data-ttu-id="a9122-111">**szComment**</span><span class="sxs-lookup"><span data-stu-id="a9122-111">**szComment**</span></span>
</dt> <dd>

<span data-ttu-id="a9122-112">Brève description du protocole.</span><span class="sxs-lookup"><span data-stu-id="a9122-112">Brief description of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a9122-113">**szHelpFile**</span><span class="sxs-lookup"><span data-stu-id="a9122-113">**szHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="a9122-114">Nom du fichier d’aide de protocole, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a9122-114">Name of the protocol Help file, if any.</span></span>

</dd> <dt>

<span data-ttu-id="a9122-115">**pWhoCanPrecedeMe**</span><span class="sxs-lookup"><span data-stu-id="a9122-115">**pWhoCanPrecedeMe**</span></span>
</dt> <dd>

<span data-ttu-id="a9122-116">Pointeur vers une [structure \_ FOLLOWSET de PF](pf-followset.md) qui répertorie les protocoles qui peuvent précéder le protocole décrit par la structure **\_ PARSERINFO de PF** .</span><span class="sxs-lookup"><span data-stu-id="a9122-116">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocols that can precede the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="a9122-117">Moniteur réseau ajoute le protocole de l’analyseur au [*jeu suivant*](f.md) de tous les protocoles de l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="a9122-117">Network Monitor adds the parser protocol to the [*follow set*](f.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="a9122-118">**pWhoCanFollowMe**</span><span class="sxs-lookup"><span data-stu-id="a9122-118">**pWhoCanFollowMe**</span></span>
</dt> <dd>

<span data-ttu-id="a9122-119">Pointeur vers une [structure \_ FOLLOWSET de PF](pf-followset.md) qui répertorie le protocole qui peut suivre le protocole décrit par la structure **\_ PARSERINFO de PF** .</span><span class="sxs-lookup"><span data-stu-id="a9122-119">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocol that can follow the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="a9122-120">Moniteur réseau ajoute les protocoles de l’ensemble à l' [*ensemble suivant*](f.md) du protocole de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="a9122-120">Network Monitor adds the protocols of the set to the [*follow set*](f.md) of the parser protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a9122-121">**pWhoHandsOffToMe**</span><span class="sxs-lookup"><span data-stu-id="a9122-121">**pWhoHandsOffToMe**</span></span>
</dt> <dd>

<span data-ttu-id="a9122-122">Pointeur vers une [structure \_ HANDOFFSET de PF](pf-handoffset.md) qui transmet le protocole décrit par la structure **\_ PARSERINFO de PF** .</span><span class="sxs-lookup"><span data-stu-id="a9122-122">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that hands-off to the protocol that the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="a9122-123">Moniteur réseau ajoute le protocole de l’analyseur aux [*jeux de remise*](h.md) de tous les protocoles de l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="a9122-123">Network Monitor adds the parser protocol to the [*handoff sets*](h.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="a9122-124">**pWhoDoIHandOffTo**</span><span class="sxs-lookup"><span data-stu-id="a9122-124">**pWhoDoIHandOffTo**</span></span>
</dt> <dd>

<span data-ttu-id="a9122-125">Pointeur vers une [structure \_ HANDOFFSET de PF](pf-handoffset.md) qui répertorie les protocoles que le protocole d’analyseur transmet.</span><span class="sxs-lookup"><span data-stu-id="a9122-125">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that lists the protocols that the parser protocol hands off to.</span></span> <span data-ttu-id="a9122-126">Moniteur réseau ajoute les protocoles de cet ensemble au [*jeu de remise*](h.md) du protocole d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="a9122-126">Network Monitor adds the protocols of this set to the [*handoff set*](h.md) of the parser protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9122-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a9122-127">Remarks</span></span>

<span data-ttu-id="a9122-128">La **structure \_ PARSERINFO PF** est utilisée dans la **structure \_ PARSERDLLINFO de PF** pour fournir une description d’un analyseur.</span><span class="sxs-lookup"><span data-stu-id="a9122-128">The **PF\_PARSERINFO** structure is used in the **PF\_PARSERDLLINFO** structure to provide a description of a parser.</span></span> <span data-ttu-id="a9122-129">Moniteur réseau utilise la description de l’analyseur pour mettre à jour le fichier [*Parser.ini*](p.md) et les fichiers ini des analyseurs qui précèdent et suivent le protocole décrit dans la structure **\_ PARSERINFO de PF** .</span><span class="sxs-lookup"><span data-stu-id="a9122-129">Network Monitor uses the parser description to update the [*Parser.ini*](p.md) file, and the INI files of the parsers that precede and follow the protocol described in the **PF\_PARSERINFO** structure.</span></span>

<span data-ttu-id="a9122-130">Un jeu suivant spécifie les protocoles qui suivent un protocole.</span><span class="sxs-lookup"><span data-stu-id="a9122-130">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="a9122-131">Moniteur réseau utilise un jeu de suivi lorsque l’analyseur ne parvient pas à identifier le protocole suivant à partir des données dans une instance de protocole.</span><span class="sxs-lookup"><span data-stu-id="a9122-131">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="a9122-132">Un jeu de suivi est stocké dans le fichier [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="a9122-132">A follow set is stored in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="a9122-133">Lorsque l’analyseur est installé pour la première fois, Moniteur réseau met à jour l’ensemble des protocoles de l’analyseur répertoriés dans **pWhoCanPrecedeMe** et **pWhoCanFollowMe**.</span><span class="sxs-lookup"><span data-stu-id="a9122-133">When the parser is installed for the first time, Network Monitor updates the follow set of the parser protocols that are listed in **pWhoCanPrecedeMe** and **pWhoCanFollowMe**.</span></span>

<span data-ttu-id="a9122-134">Un jeu de remise spécifie les protocoles qui suivent un protocole.</span><span class="sxs-lookup"><span data-stu-id="a9122-134">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="a9122-135">L’analyseur utilise un jeu de remise uniquement lorsque l’analyseur peut identifier le protocole suivant à partir des données dans une instance de protocole.</span><span class="sxs-lookup"><span data-stu-id="a9122-135">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="a9122-136">Un jeu de remise est stocké dans les fichiers INI de chaque analyseur.</span><span class="sxs-lookup"><span data-stu-id="a9122-136">A handoff set is stored in the INI files of each parser.</span></span> <span data-ttu-id="a9122-137">Lorsque l’analyseur est installé pour la première fois, Moniteur réseau met à jour le jeu de remise des protocoles de l’analyseur qui sont répertoriés dans **pWhoHandsOffToMe** et **pWhoDoIHandOffTo**.</span><span class="sxs-lookup"><span data-stu-id="a9122-137">When the parser is installed for the first time, Network Monitor updates the handoff set of the parser protocols that are listed in **pWhoHandsOffToMe** and **pWhoDoIHandOffTo**.</span></span>



| <span data-ttu-id="a9122-138">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="a9122-138">For information on</span></span>                                               | <span data-ttu-id="a9122-139">Consultez</span><span class="sxs-lookup"><span data-stu-id="a9122-139">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a9122-140">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="a9122-140">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="a9122-141">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="a9122-141">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="a9122-142">Les jeux d’éléments suivants contiennent.</span><span class="sxs-lookup"><span data-stu-id="a9122-142">What follow sets contain.</span></span>                                        | [<span data-ttu-id="a9122-143">Spécification d’un jeu de suivi</span><span class="sxs-lookup"><span data-stu-id="a9122-143">Specifying a Follow Set</span></span>](specifying-a-follow-set.md)                       |
| <span data-ttu-id="a9122-144">Ce que contiennent les jeux de remise.</span><span class="sxs-lookup"><span data-stu-id="a9122-144">What handoff sets contain.</span></span>                                       | [<span data-ttu-id="a9122-145">Spécification d’un jeu de remise</span><span class="sxs-lookup"><span data-stu-id="a9122-145">Specifying a Handoff Set</span></span>](specifying-a-handoff-set.md)                     |
| <span data-ttu-id="a9122-146">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="a9122-146">What entry points are included in the parser DLL.</span></span>                | [<span data-ttu-id="a9122-147">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="a9122-147">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="a9122-148">L’implémentation de **ParserAutoInstallInfo**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="a9122-148">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="a9122-149">Implémentation de ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="a9122-149">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="a9122-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9122-150">Requirements</span></span>



| <span data-ttu-id="a9122-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9122-151">Requirement</span></span> | <span data-ttu-id="a9122-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9122-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a9122-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9122-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a9122-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9122-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a9122-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9122-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a9122-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9122-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a9122-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9122-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9122-158"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9122-158"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9122-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9122-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9122-160">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="a9122-160">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> <dt>

[<span data-ttu-id="a9122-161">\_FOLLOWSET PF</span><span class="sxs-lookup"><span data-stu-id="a9122-161">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> <dt>

[<span data-ttu-id="a9122-162">\_HANDOFFSET PF</span><span class="sxs-lookup"><span data-stu-id="a9122-162">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> <dt>

[<span data-ttu-id="a9122-163">\_PARSERDLLINFO PF</span><span class="sxs-lookup"><span data-stu-id="a9122-163">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 





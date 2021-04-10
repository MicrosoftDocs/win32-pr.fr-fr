---
description: La \_ structure PARSERDLLINFO PF définit les analyseurs situés dans la dll de l’analyseur.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: Structure de PF_PARSERDLLINFO (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952391"
---
# <a name="pf_parserdllinfo-structure"></a><span data-ttu-id="517c8-103">PF \_ PARSERDLLINFO, structure</span><span class="sxs-lookup"><span data-stu-id="517c8-103">PF\_PARSERDLLINFO structure</span></span>

<span data-ttu-id="517c8-104">La **structure \_ PARSERDLLINFO PF** définit les analyseurs situés dans la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="517c8-104">The **PF\_PARSERDLLINFO** structure defines the parsers located in the parser DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="517c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="517c8-105">Syntax</span></span>


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a><span data-ttu-id="517c8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="517c8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="517c8-107">**nParsers**</span><span class="sxs-lookup"><span data-stu-id="517c8-107">**nParsers**</span></span>
</dt> <dd>

<span data-ttu-id="517c8-108">Nombre d’analyseurs dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="517c8-108">Number of parsers in the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="517c8-109">**ParserInfo**</span><span class="sxs-lookup"><span data-stu-id="517c8-109">**ParserInfo**</span></span>
</dt> <dd>

<span data-ttu-id="517c8-110">Tableau de [structures \_ PARSERINFO PF](pf-parserinfo.md) qui décrivent chaque analyseur dans la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="517c8-110">Array of [PF\_PARSERINFO](pf-parserinfo.md) structures that describe each parser in the parser DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="517c8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="517c8-111">Remarks</span></span>

<span data-ttu-id="517c8-112">La **structure \_ PARSERDLLINFO PF** est retournée par la fonction d’exportation [ParserAutoInstallInfo](parserautoinstallinfo.md) qui est implémentée dans la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="517c8-112">The **PF\_PARSERDLLINFO** structure is returned by the [ParserAutoInstallInfo](parserautoinstallinfo.md) export function that is implemented in the parser DLL.</span></span> <span data-ttu-id="517c8-113">La fonction **ParserAutoInstallInfo** identifie le nombre d’analyseurs dans la dll et utilise un tableau de structures [ \_ PARSERINFO PF](pf-parserinfo.md) pour décrire chaque analyseur.</span><span class="sxs-lookup"><span data-stu-id="517c8-113">The **ParserAutoInstallInfo** function identifies the number of parsers in the DLL, and uses an array of [PF\_PARSERINFO](pf-parserinfo.md) structures to describe each parser.</span></span>

<span data-ttu-id="517c8-114">La \_ structure PARSERDLLINFO de PF doit être allouée à l’aide de **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="517c8-114">The PF\_PARSERDLLINFO structure must be allocated using **HeapAlloc**.</span></span>



| <span data-ttu-id="517c8-115">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="517c8-115">For information on</span></span>                                               | <span data-ttu-id="517c8-116">Consultez</span><span class="sxs-lookup"><span data-stu-id="517c8-116">See</span></span>                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="517c8-117">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="517c8-117">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="517c8-118">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="517c8-118">Parsers</span></span>](parsers.md)                                                      |
| <span data-ttu-id="517c8-119">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="517c8-119">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="517c8-120">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="517c8-120">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                      |
| <span data-ttu-id="517c8-121">L’implémentation de **ParserAutoInstallInfo**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="517c8-121">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="517c8-122">Implémentation de ParserAutoIstallInfo</span><span class="sxs-lookup"><span data-stu-id="517c8-122">Implementing ParserAutoIstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="517c8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="517c8-123">Requirements</span></span>



| <span data-ttu-id="517c8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="517c8-124">Requirement</span></span> | <span data-ttu-id="517c8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="517c8-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="517c8-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="517c8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="517c8-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="517c8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="517c8-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="517c8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="517c8-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="517c8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="517c8-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="517c8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="517c8-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="517c8-131"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="517c8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="517c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="517c8-133">\_PARSERINFO PF</span><span class="sxs-lookup"><span data-stu-id="517c8-133">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="517c8-134">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="517c8-134">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> </dl>

 

 





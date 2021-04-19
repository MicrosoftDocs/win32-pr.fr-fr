---
description: Représente des informations sur un frame sur la pile des appels.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallStackFrame, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544550"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span data-ttu-id="8e1e9-103"><span id="vspixengine.callstackframe"></span>CallStackFrame, structure</span><span class="sxs-lookup"><span data-stu-id="8e1e9-103"><span id="vspixengine.callstackframe"></span>CallStackFrame structure</span></span>

<span data-ttu-id="8e1e9-104">Représente des informations sur un frame sur la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-104">Represents information about a frame on the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e1e9-105">Syntax</span></span>


```C++
} CallStackFrame;
```

## <a name="members"></a><span data-ttu-id="8e1e9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8e1e9-106">Members</span></span>

<span data-ttu-id="8e1e9-107">**functionName**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-107">**functionName**</span></span>  
<span data-ttu-id="8e1e9-108">Chaîne COM contenant le nom de la fonction associée.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-108">A COM string containing the name of the associated function.</span></span>

<span data-ttu-id="8e1e9-109">**sourceFile**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-109">**sourceFile**</span></span>  
<span data-ttu-id="8e1e9-110">Chaîne COM contenant le chemin d’accès du fichier source associé.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-110">A COM string containing the filepath of the associated source file.</span></span>

<span data-ttu-id="8e1e9-111">**NomModule**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-111">**moduleName**</span></span>  
<span data-ttu-id="8e1e9-112">Chaîne COM contenant le nom du module de code associé.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-112">A COM string containing the name of the associated code module.</span></span>

<span data-ttu-id="8e1e9-113">**lineNumber**</span><span class="sxs-lookup"><span data-stu-id="8e1e9-113">**lineNumber**</span></span>  
<span data-ttu-id="8e1e9-114">Numéro de ligne associé.</span><span class="sxs-lookup"><span data-stu-id="8e1e9-114">The associated line number.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1e9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e1e9-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e1e9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e1e9-116">Header</span></span></p></td><td><span data-ttu-id="8e1e9-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8e1e9-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




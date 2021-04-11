---
description: Représente une étape de pipeline, y compris les détails du nuanceur utilisé.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PipeLineStage, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950123"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span data-ttu-id="9b4eb-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage, structure</span><span class="sxs-lookup"><span data-stu-id="9b4eb-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage structure</span></span>

<span data-ttu-id="9b4eb-104">Représente une étape de pipeline, y compris les détails du nuanceur utilisé.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-104">Represents a pipeline stage, including details of the shader used.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b4eb-105">Syntax</span></span>


```C++
} PipeLineStage;
```

## <a name="members"></a><span data-ttu-id="9b4eb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9b4eb-106">Members</span></span>

<span data-ttu-id="9b4eb-107">**StageId**</span><span class="sxs-lookup"><span data-stu-id="9b4eb-107">**StageId**</span></span>  
<span data-ttu-id="9b4eb-108">ID de l’étape de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-108">The ID of the pipeline stage.</span></span>

<span data-ttu-id="9b4eb-109">**Débogable**</span><span class="sxs-lookup"><span data-stu-id="9b4eb-109">**Debuggable**</span></span>  
<span data-ttu-id="9b4eb-110">true si l’étape de pipeline prend en charge le débogage ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-110">true if the pipeline stage supports debugging; otherwise, false.</span></span>

<span data-ttu-id="9b4eb-111">**StageName**</span><span class="sxs-lookup"><span data-stu-id="9b4eb-111">**StageName**</span></span>  
<span data-ttu-id="9b4eb-112">Chaîne COM contenant le nom de l’étape de pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-112">A COM string containing the name of the pipeline stage.</span></span>

<span data-ttu-id="9b4eb-113">**GuaranteedOutput**</span><span class="sxs-lookup"><span data-stu-id="9b4eb-113">**GuaranteedOutput**</span></span>  
<span data-ttu-id="9b4eb-114">true si l’étape de pipeline a toujours une sortie de pipeline ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-114">true if the pipeline stage always has pipeline output; otherwise, false.</span></span>

<span data-ttu-id="9b4eb-115">**DebugEntryPoint**</span><span class="sxs-lookup"><span data-stu-id="9b4eb-115">**DebugEntryPoint**</span></span>  
<span data-ttu-id="9b4eb-116">Chaîne COM contenant le nom du point d’entrée du nuanceur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-116">A COM string containing the name of the shader entry point, if there is one.</span></span>

<span data-ttu-id="9b4eb-117">**ShaderFile**</span><span class="sxs-lookup"><span data-stu-id="9b4eb-117">**ShaderFile**</span></span>  
<span data-ttu-id="9b4eb-118">Chaîne COM contenant le chemin d’accès du fichier source du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-118">A COM string containing the filepath of the shader source file.</span></span>

<span data-ttu-id="9b4eb-119">**ShaderByteStreamPtr**</span><span class="sxs-lookup"><span data-stu-id="9b4eb-119">**ShaderByteStreamPtr**</span></span>  
<span data-ttu-id="9b4eb-120">FILEPTR pour le flux d’octets du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-120">A FILEPTR for the shader byte stream.</span></span> <span data-ttu-id="9b4eb-121">Cette valeur est retournée pour déboguer.</span><span class="sxs-lookup"><span data-stu-id="9b4eb-121">This is passed back in order to debug.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b4eb-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b4eb-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9b4eb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b4eb-123">Header</span></span></p></td><td><span data-ttu-id="9b4eb-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9b4eb-124">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




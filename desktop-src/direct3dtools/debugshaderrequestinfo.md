---
description: Représente des informations sur une demande de débogueur de nuanceur.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DebugShaderRequestInfo, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521588"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span data-ttu-id="3b3cb-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo, structure</span><span class="sxs-lookup"><span data-stu-id="3b3cb-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo structure</span></span>

<span data-ttu-id="3b3cb-104">Représente des informations sur une demande de débogueur de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-104">Represents information about a shader debugger request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b3cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b3cb-105">Syntax</span></span>


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a><span data-ttu-id="3b3cb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3b3cb-106">Members</span></span>

<span data-ttu-id="3b3cb-107">**mode**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-107">**stage**</span></span>  
<span data-ttu-id="3b3cb-108">Étape de pipeline à déboguer.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-108">The pipeline stage to debug.</span></span>

<span data-ttu-id="3b3cb-109">**1001**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-109">**eventID**</span></span>  
<span data-ttu-id="3b3cb-110">ID de l’événement Graphics à déboguer.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-110">The ID of the graphics event to debug.</span></span>

<span data-ttu-id="3b3cb-111">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-111">**frameNumber**</span></span>  
<span data-ttu-id="3b3cb-112">Frame à déboguer.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-112">The frame to debug.</span></span>

<span data-ttu-id="3b3cb-113">**vertex**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-113">**vertex**</span></span>  
<span data-ttu-id="3b3cb-114">Vertex à déboguer.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-114">The vertex to debug.</span></span>

<span data-ttu-id="3b3cb-115">**pixellisé**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-115">**pixel**</span></span>  
<span data-ttu-id="3b3cb-116">Pixel à déboguer.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-116">The pixel to debug.</span></span>

<span data-ttu-id="3b3cb-117">**groupCoordinates**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-117">**groupCoordinates**</span></span>  
<span data-ttu-id="3b3cb-118">Coordonnées du groupe à déboguer.</span><span class="sxs-lookup"><span data-stu-id="3b3cb-118">The coordinates of the group to debug.</span></span>

<span data-ttu-id="3b3cb-119">**threadCoordinates**</span><span class="sxs-lookup"><span data-stu-id="3b3cb-119">**threadCoordinates**</span></span>  
<span data-ttu-id="3b3cb-120">Coordonnées du thread à déboguer</span><span class="sxs-lookup"><span data-stu-id="3b3cb-120">The coordinates of the thread to debug</span></span>

## <a name="requirements"></a><span data-ttu-id="3b3cb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b3cb-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3b3cb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b3cb-122">Header</span></span></p></td><td><span data-ttu-id="3b3cb-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3b3cb-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




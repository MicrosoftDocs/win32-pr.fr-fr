---
description: Représente des informations sur le serveur de symboles de débogage.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SymbolServerInfo, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108938"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span data-ttu-id="d5977-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo, structure</span><span class="sxs-lookup"><span data-stu-id="d5977-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo structure</span></span>

<span data-ttu-id="d5977-104">Représente des informations sur le serveur de symboles de débogage.</span><span class="sxs-lookup"><span data-stu-id="d5977-104">Represents information about the debug symbol server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5977-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5977-105">Syntax</span></span>


```C++
} SymbolServerInfo;
```

## <a name="members"></a><span data-ttu-id="d5977-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d5977-106">Members</span></span>

<span data-ttu-id="d5977-107">**symbolPath**</span><span class="sxs-lookup"><span data-stu-id="d5977-107">**symbolPath**</span></span>  
<span data-ttu-id="d5977-108">Chaîne COM contenant le chemin d’accès du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="d5977-108">A COM string containing the path of the symbol server.</span></span>

<span data-ttu-id="d5977-109">**symbolCacheDir**</span><span class="sxs-lookup"><span data-stu-id="d5977-109">**symbolCacheDir**</span></span>  
<span data-ttu-id="d5977-110">Chaîne COM contenant le répertoire de cache du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="d5977-110">A COM string containing the cache directory of the symbol server.</span></span>

<span data-ttu-id="d5977-111">**publicSymbolServerName**</span><span class="sxs-lookup"><span data-stu-id="d5977-111">**publicSymbolServerName**</span></span>  
<span data-ttu-id="d5977-112">Chaîne COM contenant le nom public du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="d5977-112">A COM string containing the public name of the symbol server.</span></span>

<span data-ttu-id="d5977-113">**symbolExcludeList**</span><span class="sxs-lookup"><span data-stu-id="d5977-113">**symbolExcludeList**</span></span>  
<span data-ttu-id="d5977-114">Chaîne COM qui spécifie la liste de symboles à exclure.</span><span class="sxs-lookup"><span data-stu-id="d5977-114">A COM string that specifies the list of symbols to exclude.</span></span>

<span data-ttu-id="d5977-115">**symbolIncludeList**</span><span class="sxs-lookup"><span data-stu-id="d5977-115">**symbolIncludeList**</span></span>  
<span data-ttu-id="d5977-116">Chaîne COM qui spécifie la liste de symboles à inclure.</span><span class="sxs-lookup"><span data-stu-id="d5977-116">A COM string that specifies the list of symbols to include.</span></span>

<span data-ttu-id="d5977-117">**useExcludeList**</span><span class="sxs-lookup"><span data-stu-id="d5977-117">**useExcludeList**</span></span>  
<span data-ttu-id="d5977-118">true si la liste d’exclusion est ignorée ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="d5977-118">true if the exclude list is ignored; otherwise, false.</span></span>

<span data-ttu-id="d5977-119">**useMSSymbolServer**</span><span class="sxs-lookup"><span data-stu-id="d5977-119">**useMSSymbolServer**</span></span>  
<span data-ttu-id="d5977-120">true si vous utilisez le serveur de symboles Microsoft ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="d5977-120">true if using Microsoft symbol server; otherwise, false.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5977-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5977-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d5977-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5977-122">Header</span></span></p></td><td><span data-ttu-id="d5977-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d5977-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




---
description: Avant de commencer à développer une application de services HTTP Microsoft Windows (WinHTTP), vous devez d’abord déterminer s’il faut utiliser l’API C/C++ ou l’interface COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Choix d’une interface WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544902"
---
# <a name="choosing-a-winhttp-interface"></a><span data-ttu-id="ac0f8-103">Choix d’une interface WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ac0f8-103">Choosing a WinHTTP Interface</span></span>

<span data-ttu-id="ac0f8-104">Avant de commencer à développer une application de services HTTP Microsoft Windows (WinHTTP), vous devez d’abord déterminer s’il faut utiliser l’API C/C++ ou l’interface COM.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-104">Before you begin to develop a Microsoft Windows HTTP Services (WinHTTP) application, you must first decide whether to use the C/C++ API or the COM interface.</span></span> <span data-ttu-id="ac0f8-105">Le tableau suivant récapitule les avantages et les inconvénients associés à chacune de ces approches.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-105">The following table summarizes the advantages and disadvantages associated with each of these approaches.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ac0f8-106">API C/C++</span><span class="sxs-lookup"><span data-stu-id="ac0f8-106">C/C++ API</span></span></th>
<th><span data-ttu-id="ac0f8-107">Interface COM</span><span class="sxs-lookup"><span data-stu-id="ac0f8-107">COM interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac0f8-108">Avantages</span><span class="sxs-lookup"><span data-stu-id="ac0f8-108">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="ac0f8-109">Les réponses peuvent être traitées par segments, ce qui est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-109">Responses can be processed in chunks, which is more efficient.</span></span></li>
<li><span data-ttu-id="ac0f8-110">Les opérations de publication peuvent également être traitées par segments, accélérant ainsi le temps de traitement.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-110">POST operations can also be processed in chunks, speeding processing time.</span></span></li>
<li><span data-ttu-id="ac0f8-111">Prise en charge d’AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-111">AutoProxy support.</span></span></li>
<li><span data-ttu-id="ac0f8-112">Accès à l’ensemble complet des fonctionnalités de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-112">Access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="ac0f8-113">Les données binaires peuvent être facilement gérées.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-113">Binary data can easily be handled.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ac0f8-114">La création d’une application est simple et requiert moins de lignes de code que l’API C/C++.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-114">Creating an application is easy and requires fewer lines of code than the C/C++ API.</span></span></li>
<li><span data-ttu-id="ac0f8-115">L’interface peut être utilisée par les langages de script.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-115">The interface can be used by scripting languages.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac0f8-116">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="ac0f8-116">Disadvantages</span></span></td>
<td><ul>
<li><span data-ttu-id="ac0f8-117">Le traitement est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-117">Processing is more complex.</span></span></li>
<li><span data-ttu-id="ac0f8-118">L’API C/C++ requiert davantage d’étapes que l’interface COM pour effectuer les mêmes actions.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-118">The C/C++ API requires more steps than the COM interface to perform the same actions.</span></span></li>
<li><span data-ttu-id="ac0f8-119">La configuration d’une demande nécessite davantage de code.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-119">Setting up a request takes more code.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ac0f8-120">L’interface COM ne permet pas d’accéder à l’ensemble complet des fonctionnalités de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-120">The COM interface does not provide access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="ac0f8-121">Il est difficile de gérer les types de données binaires dans certains langages de script, tels que VBScript et JScript.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-121">It is difficult to handle binary data types in some scripting languages, such as VBScript and JScript.</span></span></li>
<li><span data-ttu-id="ac0f8-122">L’interface COM ne prend pas en charge le proxy AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-122">The COM interface does not support AutoProxy.</span></span></li>
<li><span data-ttu-id="ac0f8-123">Les applications doivent utiliser le modèle de APARTMENT_THREADED COM.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-123">Applications must use the COM APARTMENT_THREADED model.</span></span></li>
<li><span data-ttu-id="ac0f8-124">Avant qu’une réponse puisse commencer à être traitée, toute la réponse doit d’abord être reçue et mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ac0f8-124">Before a response can begin being processed, the entire response must first be received and buffered.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 




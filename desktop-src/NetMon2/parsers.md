---
description: Un analyseur est le composant Moniteur réseau qui inspecte les données dans une capture différée et transmet des informations de protocole spécifiques à l’application qui appelle l’analyseur. Un analyseur est passif, car il fonctionne uniquement quand Moniteur réseau ou un expert l’appelle.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861990"
---
# <a name="parser"></a><span data-ttu-id="ce4b6-104">Parser</span><span class="sxs-lookup"><span data-stu-id="ce4b6-104">Parser</span></span>

<span data-ttu-id="ce4b6-105">Un analyseur est le composant Moniteur réseau qui inspecte les données dans une [*capture différée*](d.md)et transmet des informations de protocole spécifiques à l’application qui appelle l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-105">A parser is the Network Monitor component that inspects data in a [*delayed capture*](d.md), and passes specific protocol information to the application that calls the parser.</span></span> <span data-ttu-id="ce4b6-106">Un analyseur est passif, car il fonctionne uniquement quand Moniteur réseau ou un [*expert*](e.md) l’appelle.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-106">A parser is passive because it works only when Network Monitor or an [*expert*](e.md) call it.</span></span>

<span data-ttu-id="ce4b6-107">Chaque analyseur identifie un protocole, et en général, un analyseur est implémenté dans sa propre DLL d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-107">Each parser identifies one protocol, and typically, a parser is implemented within its own parser DLL.</span></span> <span data-ttu-id="ce4b6-108">Toutefois, une DLL d’analyseur peut contenir plusieurs analyseurs, ce qui signifie qu’une DLL peut être utilisée pour détecter plusieurs protocoles.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-108">However, a parser DLL can contain multiple parsers which means that one DLL can be used to detect more than one protocol.</span></span>

<span data-ttu-id="ce4b6-109">Les données transmises à un analyseur sont extraites d’une [*capture différée*](d.md)et transmises à l’analyseur image par image.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-109">The data passed to a parser is taken from a [*delayed capture*](d.md), and passed to the parser on a frame-by-frame basis.</span></span> <span data-ttu-id="ce4b6-110">Vous ne pouvez pas analyser une capture en temps réel.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-110">You cannot parse a real-time capture.</span></span>

<span data-ttu-id="ce4b6-111">Pour analyser les données dans un frame, l’analyseur doit reconnaître l’instance de protocole, identifier les propriétés qui existent dans l’instance de protocole et attacher une définition de propriété à chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-111">To parse the data in a frame, the parser must recognize the protocol instance, identify the properties that exist in the protocol instance, and attach a property definition to each property.</span></span> <span data-ttu-id="ce4b6-112">N’oubliez pas que le frame contient uniquement un flux de données.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-112">Be aware that the frame contains only a stream of data.</span></span> <span data-ttu-id="ce4b6-113">Le frame ne contient pas de données indiquant les protocoles ou les propriétés de protocole que les données représentent.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-113">The frame does not contain data that indicates which protocols or protocol properties the data represents.</span></span>

<span data-ttu-id="ce4b6-114">L’illustration suivante montre un frame qui contient une instance d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-114">The following illustration shows a frame that contains an instance of a protocol.</span></span>

![Frame qui contient une instance de protocole](images/parser1.png)

<span data-ttu-id="ce4b6-116">Si Moniteur réseau affiche des données analysées dans l’interface utilisateur, l’analyseur doit mettre en forme les données.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-116">If Network Monitor is going to display parsed data in the UI, the parser must format the data.</span></span> <span data-ttu-id="ce4b6-117">Toutefois, certains experts utilisent la sortie de l’analyseur par programme et n’affichent pas la sortie dans l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-117">However, some experts use the parser output programmatically, and do not display the output in the Network Monitor UI.</span></span> <span data-ttu-id="ce4b6-118">Les données affichées incluent à la fois les données définies par l’analyseur et les données de la capture.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-118">Displayed data includes both parser-defined data, and the data in the capture.</span></span> <span data-ttu-id="ce4b6-119">Par exemple, l’analyseur fournit en général à la fois un nom pour une propriété qui est affichée et les données de la capture qui est associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-119">For example, the parser typically provides both a name for a property that is displayed, and the data in the capture that is associated with the property.</span></span>



| <span data-ttu-id="ce4b6-120">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="ce4b6-120">For information about</span></span>                                         | <span data-ttu-id="ce4b6-121">Consultez</span><span class="sxs-lookup"><span data-stu-id="ce4b6-121">See</span></span>                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ce4b6-122">Les points d’entrée doivent être implémentés dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-122">Which entry points must be implemented within the parser DLL.</span></span> | [<span data-ttu-id="ce4b6-123">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="ce4b6-123">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                 |
| <span data-ttu-id="ce4b6-124">Comment implémenter les fonctions d’exportation de DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-124">How to implement parser DLL export functions.</span></span>                 | [<span data-ttu-id="ce4b6-125">Écriture d’un analyseur de protocole</span><span class="sxs-lookup"><span data-stu-id="ce4b6-125">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="ce4b6-126">Les fonctions et les analyseurs de structures qui utilisent.</span><span class="sxs-lookup"><span data-stu-id="ce4b6-126">Which functions and structures parsers use.</span></span>                   | [<span data-ttu-id="ce4b6-127">Structures et fonctions de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="ce4b6-127">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 




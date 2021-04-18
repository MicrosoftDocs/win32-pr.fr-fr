---
description: La valeur logique d’une propriété qui a été définie est true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Utilisation des propriétés dans les instructions conditionnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512978"
---
# <a name="using-properties-in-conditional-statements"></a><span data-ttu-id="15db6-103">Utilisation des propriétés dans les instructions conditionnelles</span><span class="sxs-lookup"><span data-stu-id="15db6-103">Using Properties in Conditional Statements</span></span>

<span data-ttu-id="15db6-104">La valeur logique d’une propriété qui a été définie est true.</span><span class="sxs-lookup"><span data-stu-id="15db6-104">The logical value of a property that has been set is True.</span></span> <span data-ttu-id="15db6-105">Pour déterminer si une propriété est définie sans réellement obtenir sa valeur, testez l’expression logique « MyProperty » ou « non-MyProperty ».</span><span class="sxs-lookup"><span data-stu-id="15db6-105">To determine whether a property is set without actually getting its value, test the logical expression "MyProperty" or "Not MyProperty".</span></span> <span data-ttu-id="15db6-106">Lorsque la propriété MyProperty est définie, la première évaluation prend la valeur true et la dernière la valeur false.</span><span class="sxs-lookup"><span data-stu-id="15db6-106">When the property MyProperty is set, the former evaluates as True and the latter as False.</span></span>

<span data-ttu-id="15db6-107">Une ou plusieurs propriétés peuvent être combinées avec des opérateurs pour former des expressions logiques utilisées dans des instructions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="15db6-107">One or more properties can be combined with operators to form logical expressions used in a conditional statements.</span></span> <span data-ttu-id="15db6-108">Pour plus d’informations sur les opérateurs qui peuvent être utilisés dans les instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="15db6-108">For more information about the operators that can be used in conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="15db6-109">Une instruction conditionnelle utilisant des propriétés peut être entrée dans la colonne condition de la [table condition](condition-table.md) pour modifier l’état de sélection d’une entrée dans la [table des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="15db6-109">A conditional statement using properties can be entered into the Condition column of the [Condition table](condition-table.md) to modify the selection state of any entry in the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="15db6-110">Les instructions conditionnelles avec une ou plusieurs propriétés sont couramment utilisées dans la colonne condition des tables de base de données.</span><span class="sxs-lookup"><span data-stu-id="15db6-110">Conditional statements with one or more properties are commonly used in the Condition column of database tables.</span></span>

<span data-ttu-id="15db6-111">Les tables suivantes ont chacune une colonne pour les expressions conditionnelles :</span><span class="sxs-lookup"><span data-stu-id="15db6-111">The following tables each have a column for conditional expressions:</span></span>

-   [<span data-ttu-id="15db6-112">Table de conditions</span><span class="sxs-lookup"><span data-stu-id="15db6-112">Condition table</span></span>](condition-table.md)
-   [<span data-ttu-id="15db6-113">Table ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="15db6-113">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="15db6-114">Table LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="15db6-114">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="15db6-115">Table InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="15db6-115">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="15db6-116">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="15db6-116">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="15db6-117">Table ControlCondition</span><span class="sxs-lookup"><span data-stu-id="15db6-117">ControlCondition table</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="15db6-118">Table AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="15db6-118">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="15db6-119">Table AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="15db6-119">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="15db6-120">Table AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="15db6-120">AdminUISequence table</span></span>](adminuisequence-table.md)

<span data-ttu-id="15db6-121">Notez que les six tables de séquences d’action comportent des champs pour une condition.</span><span class="sxs-lookup"><span data-stu-id="15db6-121">Note that the six action sequence tables have fields for a condition.</span></span> <span data-ttu-id="15db6-122">Si l’expression conditionnelle de ce champ a la valeur false, le programme d’installation ignore cette action.</span><span class="sxs-lookup"><span data-stu-id="15db6-122">If the conditional expression in this field evaluates to False, the installer skips that action.</span></span>

<span data-ttu-id="15db6-123">Si vous définissez une [propriété privée](private-properties.md) dans la séquence d’interface utilisateur en créant une action personnalisée dans l’une des tables de séquence de l’interface utilisateur, cette propriété n’est pas définie dans la séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="15db6-123">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="15db6-124">Pour définir la propriété dans la séquence d’exécution, vous devez également placer une action personnalisée dans une table de séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="15db6-124">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="15db6-125">Vous pouvez également faire de la propriété une [propriété publique](public-properties.md) et l’inclure dans la propriété [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="15db6-125">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="15db6-126">Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md) ou [utilisation de propriétés](using-properties.md).</span><span class="sxs-lookup"><span data-stu-id="15db6-126">For more information, see [Using a Sequence Table](using-a-sequence-table.md) or [Using Properties](using-properties.md).</span></span>

 

 




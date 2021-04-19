---
description: Les actions personnalisées écrites en JScript ou Visual Basic, Scripting Edition (VBScript) peuvent appeler une fonction facultative. Ces fonctions doivent retourner l’une des valeurs indiquées dans le tableau suivant.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valeurs de retour des actions personnalisées JScript et VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524545"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a><span data-ttu-id="078f3-104">Valeurs de retour des actions personnalisées JScript et VBScript</span><span class="sxs-lookup"><span data-stu-id="078f3-104">Return Values of JScript and VBScript Custom Actions</span></span>

<span data-ttu-id="078f3-105">Les actions personnalisées écrites en JScript ou Visual Basic, Scripting Edition (VBScript) peuvent appeler une fonction facultative.</span><span class="sxs-lookup"><span data-stu-id="078f3-105">Custom actions written in JScript or Visual Basic, Scripting Edition (VBScript) can call an optional function.</span></span> <span data-ttu-id="078f3-106">Ces fonctions doivent retourner l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="078f3-106">These functions must return one of the values shown in the following table.</span></span>



| <span data-ttu-id="078f3-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="078f3-107">Return value</span></span>              | <span data-ttu-id="078f3-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="078f3-108">Value</span></span>        | <span data-ttu-id="078f3-109">Description</span><span class="sxs-lookup"><span data-stu-id="078f3-109">Description</span></span>                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="078f3-110">msiDoActionStatusNoAction</span><span class="sxs-lookup"><span data-stu-id="078f3-110">msiDoActionStatusNoAction</span></span> | <span data-ttu-id="078f3-111">0</span><span class="sxs-lookup"><span data-stu-id="078f3-111">0</span></span>            | <span data-ttu-id="078f3-112">Action non exécutée.</span><span class="sxs-lookup"><span data-stu-id="078f3-112">Action not executed.</span></span>                                                                                       |
| <span data-ttu-id="078f3-113">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="078f3-113">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="078f3-114">IDOK = 1</span><span class="sxs-lookup"><span data-stu-id="078f3-114">IDOK = 1</span></span>     | <span data-ttu-id="078f3-115">Action terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="078f3-115">Action completed successfully.</span></span>                                                                             |
| <span data-ttu-id="078f3-116">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="078f3-116">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="078f3-117">IDCANCEL = 2</span><span class="sxs-lookup"><span data-stu-id="078f3-117">IDCANCEL = 2</span></span> | <span data-ttu-id="078f3-118">Arrêt prématuré par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="078f3-118">Premature termination by user.</span></span>                                                                             |
| <span data-ttu-id="078f3-119">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="078f3-119">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="078f3-120">IDABORT = 3</span><span class="sxs-lookup"><span data-stu-id="078f3-120">IDABORT = 3</span></span>  | <span data-ttu-id="078f3-121">Erreur irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="078f3-121">Unrecoverable error.</span></span> <span data-ttu-id="078f3-122">Retourné en cas d’erreur lors de l’analyse ou de l’exécution du script JScript ou VBScript.</span><span class="sxs-lookup"><span data-stu-id="078f3-122">Returned if there is an error during parsing or execution of the JScript or VBScript.</span></span> |
| <span data-ttu-id="078f3-123">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="078f3-123">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="078f3-124">IDRETRY = 4</span><span class="sxs-lookup"><span data-stu-id="078f3-124">IDRETRY = 4</span></span>  | <span data-ttu-id="078f3-125">Séquence suspendue à reprendre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="078f3-125">Suspended sequence to be resumed later.</span></span>                                                                    |
| <span data-ttu-id="078f3-126">msiDoActionStatusFinished</span><span class="sxs-lookup"><span data-stu-id="078f3-126">msiDoActionStatusFinished</span></span> | <span data-ttu-id="078f3-127">IDIGNORE = 5</span><span class="sxs-lookup"><span data-stu-id="078f3-127">IDIGNORE = 5</span></span> | <span data-ttu-id="078f3-128">Ignorer les actions restantes.</span><span class="sxs-lookup"><span data-stu-id="078f3-128">Skip remaining actions.</span></span> <span data-ttu-id="078f3-129">N’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="078f3-129">Not an error.</span></span>                                                                      |



 

<span data-ttu-id="078f3-130">Notez que Windows Installer traduit les valeurs de retour de toutes les actions lorsqu’il écrit la valeur de retour dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="078f3-130">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="078f3-131">Par exemple, si la valeur de retour de l’action apparaît comme 1 (un) dans le fichier journal, cela signifie que l’action a retourné msiDoActionStatusSuccess.</span><span class="sxs-lookup"><span data-stu-id="078f3-131">For example, if the action return value appears as 1 (one) in the log file, this means that the action returned msiDoActionStatusSuccess.</span></span> <span data-ttu-id="078f3-132">Pour plus d’informations sur cette traduction, consultez [journalisation des valeurs de retour d’action](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="078f3-132">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="078f3-133">Pour retourner une valeur autre que la réussite à partir d’une action personnalisée de script, vous devez utiliser une cible de fonction pour l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="078f3-133">To return a value other than success from a script custom action, you must use a function target for the custom action.</span></span> <span data-ttu-id="078f3-134">La fonction cible est spécifiée dans la colonne cible de la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="078f3-134">The target function is specified in the Target column of the [CustomAction Table](customaction-table.md).</span></span>

<span data-ttu-id="078f3-135">L’exemple de script suivant montre comment retourner la réussite ou l’échec d’une action personnalisée VBScript.</span><span class="sxs-lookup"><span data-stu-id="078f3-135">The following script example shows you how to return success or failure from a VBScript custom action.</span></span>


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



<span data-ttu-id="078f3-136">Si ce VBScript était incorporé dans la [table binaire](binary-table.md) du package d’installation comme MyCA.vbs, l’entrée de la [table CustomAction](customaction-table.md) du script serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="078f3-136">If this VBScript were embedded in the [Binary table](binary-table.md) of the installation package as MyCA.vbs, the [CustomAction Table](customaction-table.md) entry for the script would be the following:</span></span>



| <span data-ttu-id="078f3-137">Action</span><span class="sxs-lookup"><span data-stu-id="078f3-137">Action</span></span>         | <span data-ttu-id="078f3-138">Type</span><span class="sxs-lookup"><span data-stu-id="078f3-138">Type</span></span> | <span data-ttu-id="078f3-139">Source</span><span class="sxs-lookup"><span data-stu-id="078f3-139">Source</span></span>   | <span data-ttu-id="078f3-140">Cible</span><span class="sxs-lookup"><span data-stu-id="078f3-140">Target</span></span>       |
|----------------|------|----------|--------------|
| <span data-ttu-id="078f3-141">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="078f3-141">MyCustomAction</span></span> | <span data-ttu-id="078f3-142">6</span><span class="sxs-lookup"><span data-stu-id="078f3-142">6</span></span>    | <span data-ttu-id="078f3-143">MyCA.vbs</span><span class="sxs-lookup"><span data-stu-id="078f3-143">MyCA.vbs</span></span> | <span data-ttu-id="078f3-144">MyVBScriptCA</span><span class="sxs-lookup"><span data-stu-id="078f3-144">MyVBScriptCA</span></span> |



 

 

 




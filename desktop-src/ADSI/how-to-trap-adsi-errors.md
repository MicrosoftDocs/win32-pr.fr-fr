---
title: Interruption des erreurs ADSI
description: VBScript offre une seule façon d’intercepter les erreurs de gestion des erreurs en ligne.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa36b3e9b1027e1733009d58a572a0b27c7ef0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510386"
---
# <a name="how-to-trap-adsi-errors"></a><span data-ttu-id="2deb6-103">Interruption des erreurs ADSI</span><span class="sxs-lookup"><span data-stu-id="2deb6-103">How to Trap ADSI Errors</span></span>

<span data-ttu-id="2deb6-104">VBScript offre une seule façon d’intercepter les erreurs : la gestion des erreurs en ligne.</span><span class="sxs-lookup"><span data-stu-id="2deb6-104">VBScript only offers one way to trap errors: inline error handling.</span></span> <span data-ttu-id="2deb6-105">Un gestionnaire d’erreurs Inline commence par l’instruction **On Error Resume Next** .</span><span class="sxs-lookup"><span data-stu-id="2deb6-105">An inline error handler begins with the **On Error Resume Next** statement.</span></span> <span data-ttu-id="2deb6-106">Étant donné que **en cas d’erreur, Resume Next** empêchera toute erreur d’arrêter l’exécution du script jusqu’à ce que la fin de l’étendue à partir de laquelle en cas de reprise de l' **erreur suivante** soit appelée, vous devez vérifier la valeur de **Err** à chaque point après l’instruction **On Error Resume Next** où vous vous attendez à ce qu’une erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="2deb6-106">Since **On Error Resume Next** will prevent any errors from stopping execution of the script until the end of the scope from which **On Error Resume Next** is called, you must check the value of **Err** at every point after the **On Error Resume Next** statement where you expect an error might occur.</span></span> <span data-ttu-id="2deb6-107">L’exemple suivant illustre la gestion des erreurs inline dans un script ADSI :</span><span class="sxs-lookup"><span data-stu-id="2deb6-107">The following example demonstrates inline error handling in an ADSI script:</span></span>


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



<span data-ttu-id="2deb6-108">Après chaque emplacement où le script est susceptible de rencontrer une erreur, il existe une instruction **If Err** .</span><span class="sxs-lookup"><span data-stu-id="2deb6-108">After each location where the script is likely to encounter an error, there is an **If Err** statement.</span></span> <span data-ttu-id="2deb6-109">L’objet **Err** contient le code d’erreur de la dernière erreur qui s’est produite pendant l’exécution du script. Si aucune erreur ne s’est produite, **Err** a toujours la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="2deb6-109">The **Err** object contains the error code of the last error that occurred during execution of the script; if no error has occurred, **Err** will always be zero (0).</span></span> <span data-ttu-id="2deb6-110">Dans l’exemple précédent, une erreur entraîne l’interruption de l’exécution de la sous-routine **AdsiErr** , qui vérifie la valeur de **Err. Number** pour les erreurs attendues.</span><span class="sxs-lookup"><span data-stu-id="2deb6-110">In the previous example, an error will cause execution to jump to the **AdsiErr** subroutine, which checks the value of **Err.Number** for expected errors.</span></span> <span data-ttu-id="2deb6-111">Au lieu de détourner avec un message d’erreur énigmatique, le script vous donnera une explication plus efficace pour la raison de l’arrêt de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2deb6-111">Instead of dying with a cryptic error message, the script will give a somewhat better explanation for why it stopped running.</span></span>

<span data-ttu-id="2deb6-112">N’oubliez pas que dans l’étendue dans laquelle la **fonction de reprise** après l’erreur est appelée, toute erreur qui se produit après l’appel **suivant de l’erreur de reprise** sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="2deb6-112">Remember that within the scope in which **On Error Resume Next** is called, any error that occurs after the **On Error Resume Next** call will be ignored.</span></span> <span data-ttu-id="2deb6-113">Cela peut en fait compliquer le débogage d’un script si vous oubliez de vérifier la valeur de **Err** dans les emplacements appropriés.</span><span class="sxs-lookup"><span data-stu-id="2deb6-113">This can actually make a script harder to debug if you forget to check the value of **Err** in appropriate locations.</span></span> <span data-ttu-id="2deb6-114">Chaque fois que vous vous attendez à ce qu’une erreur soit probable, veillez à vérifier la valeur de **Err**.</span><span class="sxs-lookup"><span data-stu-id="2deb6-114">Wherever you expect an error to be likely, be sure to check the value of **Err**.</span></span>

<span data-ttu-id="2deb6-115">(Lorsque vous déboguez initialement le script, vous pouvez simplement laisser le script arrêter son exécution et afficher le numéro de ligne incriminé sur une erreur, puis ajouter les gestionnaires d’erreurs une fois que le déroulement du programme de base est correct.)</span><span class="sxs-lookup"><span data-stu-id="2deb6-115">(When you are initially debugging the script you may want to simply let the script halt its execution and display the offending line number on an error, then add the error handlers after the basic program flow is correct.)</span></span>

 

 





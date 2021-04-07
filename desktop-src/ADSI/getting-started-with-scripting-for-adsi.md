---
title: Prise en main avec l’écriture de scripts pour ADSI
description: L’écriture de scripts est utile pour les administrateurs système qui souhaitent créer des scripts batch pour les tâches fréquemment utilisées.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Prise en main avec l’écriture de scripts pour ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a85a9ea110ca80f45c3a0f0f1917e8d25c08ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939589"
---
# <a name="getting-started-with-scripting-for-adsi"></a><span data-ttu-id="e497d-104">Prise en main avec l’écriture de scripts pour ADSI</span><span class="sxs-lookup"><span data-stu-id="e497d-104">Getting Started with Scripting for ADSI</span></span>

<span data-ttu-id="e497d-105">L’écriture de scripts est utile pour les administrateurs système qui souhaitent créer des scripts batch pour les tâches fréquemment utilisées.</span><span class="sxs-lookup"><span data-stu-id="e497d-105">Scripting is useful for system administrators who want to create batch scripts for frequently used tasks.</span></span>

<span data-ttu-id="e497d-106">Pour démarrer l’écriture de scripts avec ADSI, vous devez disposer d’un ordinateur exécutant Windows ou d’une session ouverte sur un domaine qui contient des données pour les comptes d’ordinateur dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="e497d-106">To start scripting with ADSI, you must have a computer that runs Windows or be logged on to a domain that contains data for computer accounts in the directory.</span></span>

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a><span data-ttu-id="e497d-107">Exemple de script simple : recherche de noms et d’emplacements de comptes d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="e497d-107">A Simple Scripting Sample: Finding Names and Locations of Computer Accounts</span></span>

<span data-ttu-id="e497d-108">Créez un nouveau fichier texte à l’aide d’un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="e497d-108">Create a new text file using a text editor.</span></span> <span data-ttu-id="e497d-109">L’exemple de code suivant montre comment rechercher des noms et des emplacements de comptes d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e497d-109">The following code example shows how to find names and locations of computer accounts.</span></span>


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



<span data-ttu-id="e497d-110">Enregistrez le fichier en tant que First.vbs.</span><span class="sxs-lookup"><span data-stu-id="e497d-110">Save the file as First.vbs.</span></span> <span data-ttu-id="e497d-111">Modifiez la ligne qui commence par « objCommand. CommandText » pour modifier le chemin d’accès à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="e497d-111">Modify the line that begins with "objCommand.CommandText" to change the path to your domain.</span></span> <span data-ttu-id="e497d-112">À l’invite de commandes, tapez **cscript First.vbs** pour une ligne de commande ou First.vbs pour les scripts Windows.</span><span class="sxs-lookup"><span data-stu-id="e497d-112">At the command prompt, type **cscript First.vbs** for a command line or First.vbs for Windows scripting.</span></span> <span data-ttu-id="e497d-113">Les résultats doivent être retournés dans l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="e497d-113">The results should be returned in the command prompt.</span></span>

<span data-ttu-id="e497d-114">Pour plus d’informations sur l’écriture de scripts pour ADSI, consultez [Active Directory des scripts d’interfaces de service](adsi-scripting-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="e497d-114">For more information about scripting for ADSI, see [Active Directory Service Interfaces Scripting](adsi-scripting-tutorial.md).</span></span>

 

 





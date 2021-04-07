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
# <a name="getting-started-with-scripting-for-adsi"></a>Prise en main avec l’écriture de scripts pour ADSI

L’écriture de scripts est utile pour les administrateurs système qui souhaitent créer des scripts batch pour les tâches fréquemment utilisées.

Pour démarrer l’écriture de scripts avec ADSI, vous devez disposer d’un ordinateur exécutant Windows ou d’une session ouverte sur un domaine qui contient des données pour les comptes d’ordinateur dans l’annuaire.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Exemple de script simple : recherche de noms et d’emplacements de comptes d’ordinateurs

Créez un nouveau fichier texte à l’aide d’un éditeur de texte. L’exemple de code suivant montre comment rechercher des noms et des emplacements de comptes d’ordinateur.


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



Enregistrez le fichier en tant que First.vbs. Modifiez la ligne qui commence par « objCommand. CommandText » pour modifier le chemin d’accès à votre domaine. À l’invite de commandes, tapez **cscript First.vbs** pour une ligne de commande ou First.vbs pour les scripts Windows. Les résultats doivent être retournés dans l’invite de commandes.

Pour plus d’informations sur l’écriture de scripts pour ADSI, consultez [Active Directory des scripts d’interfaces de service](adsi-scripting-tutorial.md).

 

 





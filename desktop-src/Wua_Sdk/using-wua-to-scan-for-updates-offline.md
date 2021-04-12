---
description: Windows Update Agent (WUA) peut être utilisé pour analyser les ordinateurs à la recherche de mises à jour de sécurité sans se connecter à Windows Update ou à un serveur Windows Server Update Services (WSUS), ce qui permet d’analyser les ordinateurs qui ne sont pas connectés à Internet pour rechercher les mises à jour de sécurité. L’analyse hors connexion des mises à jour nécessite le téléchargement d’un fichier signé, Wsusscn2.cab, à partir de Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Utilisation de WUA pour rechercher des mises à jour hors connexion
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318065"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>Utilisation de WUA pour rechercher des mises à jour hors connexion

Windows Update Agent (WUA) peut être utilisé pour analyser les ordinateurs à la recherche de mises à jour de sécurité sans se connecter à Windows Update ou à un serveur Windows Server Update Services (WSUS), ce qui permet d’analyser les ordinateurs qui ne sont pas connectés à Internet pour rechercher les mises à jour de sécurité.

L’analyse hors connexion des mises à jour nécessite le téléchargement d’un fichier signé, Wsusscn2.cab, à partir de Windows Update.

Le fichier Wsusscn2.cab est un fichier CAB signé par Microsoft. Ce fichier contient des informations sur les mises à jour liées à la sécurité publiées par Microsoft. Les ordinateurs qui ne sont pas connectés à Internet peuvent être analysés pour déterminer si ces mises à jour liées à la sécurité sont présentes ou requises. Le fichier Wsusscn2.cab ne contient pas les mises à jour de sécurité elles-mêmes. vous devez donc vous procurer et installer les mises à jour de sécurité nécessaires par d’autres moyens. Les nouvelles versions du fichier Wsusscn2.cab sont publiées régulièrement à mesure que des mises à jour liées à la sécurité sont publiées, supprimées ou révisées sur le site Windows Update. Le dernier fichier de Wsusscn2.cab est disponible en téléchargement à l’emplacement suivant : [télécharger Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

Une fois que vous avez téléchargé la dernière Wsusscn2.cab, le fichier peut être fourni à la méthode [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) , et l’API WUA peut être utilisée pour rechercher les mises à jour de sécurité sur l’ordinateur hors connexion. WUA vérifie que le Wsusscn2.cab est signé par un certificat Microsoft valide avant d’exécuter une analyse hors connexion.

> [!NOTE]
> Conformément à notre [initiative SHA-1](https://aka.ms/sha1deprecation), le fichier Wsusscn2.cab n’est plus une double signature à l’aide de SHA-1 et de la suite SHA-2 des algorithmes de hachage (plus particulièrement sha-256). Ce fichier est maintenant signé à l’aide de SHA-256 uniquement. Les administrateurs qui vérifient les signatures numériques de ce fichier doivent à présent attendre uniquement des signatures SHA-256 uniques.

## <a name="example"></a>Exemple

L’exemple suivant utilise le fichier Wsusscn2.cab pour analyser un ordinateur et afficher les mises à jour manquantes.

> [!IMPORTANT]
> Ce script est destiné à illustrer l’utilisation des API d’agent Windows Update et fournit un exemple de la façon dont les développeurs peuvent utiliser ces API pour résoudre les problèmes. Ce script n’est pas conçu comme un code de production, et le script lui-même n’est pas pris en charge par Microsoft (bien que les API de l’agent de Windows Update sous-jacent soient prises en charge).

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 




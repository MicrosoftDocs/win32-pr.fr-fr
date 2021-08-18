---
title: utilisation des applets de commande WMI Windows PowerShell pour gérer BITS Compact Server
description: Windows PowerShell fournit un mécanisme simple pour se connecter à Windows Management Instrumentation (WMI) sur un ordinateur distant et gérer le serveur Compact Service de transfert intelligent en arrière-plan (BITS).
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e82401e80b5e49b7d2b964ec910d15d70aea7ce9c782a0173bef97aa8b3a5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021077"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>utilisation des applets de commande WMI Windows PowerShell pour gérer BITS Compact Server

Windows PowerShell fournit un mécanisme simple pour se connecter à Windows Management Instrumentation (WMI) sur un ordinateur distant et gérer le serveur Compact Service de transfert intelligent en arrière-plan (BITS). BITS Compact Server est un composant serveur facultatif qui doit être installé séparément. Pour plus d’informations sur l’installation de Compact Server, consultez la documentation de [bits Compact Server](bits-compact-server.md) .

1.  Connecter au fournisseur BITS.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    L’applet de commande [obtient-Credential](/previous-versions//dd315327(v=technet.10)) demande les informations d’identification de l’utilisateur pour se connecter à l’ordinateur distant et assigne les informations d’identification à l’objet $CRED.

    Les objets retournés par l’applet de commande [obten-WmiObject](/previous-versions//dd315295(v=technet.10)) sont assignés à la variable $BCS. Dans l’exemple précédent, l’applet de commande [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)) récupère la classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) dans l' \\ \\ espace de noms Microsoft bits racine de Server1. Les méthodes statiques exposées par la classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) peuvent être appelées sur l’objet $BCS. Pour plus d’informations sur la gestion à distance BITS, consultez la rubrique classes du fournisseur [bits](/previous-versions/windows/desktop/bitsprov/bits-provider) et du [fournisseur bits]( /previous-versions//dd904507(v=vs.85)).

    > [!Note]  
    > Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne.

     

2.  Créez un groupe d’URL sur le serveur.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    La https://Server1:80/testurlgroup chaîne de préfixe d’URL "" est assignée à la variable $URLGroup. La variable $URLGroup est transmise à la méthode [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , qui crée le groupe d’URL sur Server1.

    Vous pouvez spécifier un autre groupe d’URL. Le groupe d’URL doit être conforme à une chaîne de préfixe d’URL valide. Pour plus d’informations sur les préfixes d’URL, consultez [chaînes URLPrefix](../http/urlprefix-strings.md).

3.  Hébergez un fichier sur le groupe d’URL.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    L’instance BITSCompactServerUrlGroup retournée par l’applet de commande [« obtient-WmiObject »](/previous-versions//dd315295(v=technet.10)) est assignée à la variable $bcsObj. La méthode [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) est appelée pour le $bcsObj avec le suffixe d’URL « url.txt », le \\ \\ \\ \\ chemin d’accès source « c : Temp1.txt » pour le fichier et une chaîne de descripteur de sécurité vide en tant que paramètres. Le suffixe « url.txt » est ajouté au préfixe du groupe d’URL. Les clients peuvent télécharger le fichier à partir de l’adresse suivante : https://Server1:80/testurlgroup/url.txt .

4.  Nettoyez l’URL et le groupe d’URL.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    La méthode de **suppression System. Object** supprime l’objet $bcsObj.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[Fournisseur BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Classes du fournisseur BITS]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 
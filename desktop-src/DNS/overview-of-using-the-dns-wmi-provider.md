---
title: Vue d’ensemble de l’utilisation du fournisseur WMI DNS
description: Les étapes générales suivantes vous permettent de commencer à créer votre propre script ou programme qui utilise le fournisseur WMI DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9188e14e0a0b1f73380434be0d4298b0748da12f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029494"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>Vue d’ensemble de l’utilisation du fournisseur WMI DNS

Les étapes générales suivantes vous permettent de commencer à créer votre propre script ou programme qui utilise le fournisseur WMI DNS.

**Pour créer un script ou un programme à l’aide du fournisseur WMI DNS**

1.  Connectez-vous au fournisseur WMI DNS.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > L’espace de noms pour le fournisseur WMI DNS sera toujours « racine \\ MicrosoftDNS ».

     

2.  Obtenir une instance de serveur DNS.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  En fonction de l’action de type que vous souhaitez effectuer, récupérez une zone DNS ou une instance d’enregistrement.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Effectuez les actions souhaitées :
    -   Exécuter une méthode
    -   Afficher une propriété
    -   Modifier une propriété (doit avoir un accès en lecture/écriture)

 

 





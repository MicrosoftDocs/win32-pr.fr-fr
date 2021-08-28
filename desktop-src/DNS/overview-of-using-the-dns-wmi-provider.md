---
title: Vue d’ensemble de l’utilisation du fournisseur WMI DNS
description: Les étapes générales suivantes vous permettent de commencer à créer votre propre script ou programme qui utilise le fournisseur WMI DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9eaa50e4ed1a237ed5b42abd4375ab301a2106498e929e42993cd634ca9ba18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077029"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>Vue d’ensemble de l’utilisation du fournisseur WMI DNS

Les étapes générales suivantes vous permettent de commencer à créer votre propre script ou programme qui utilise le fournisseur WMI DNS.

**Pour créer un script ou un programme à l’aide du fournisseur WMI DNS**

1.  Connecter au fournisseur WMI DNS.
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

 

 





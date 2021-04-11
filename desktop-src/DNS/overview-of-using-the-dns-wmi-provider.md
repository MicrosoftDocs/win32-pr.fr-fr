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
# <a name="overview-of-using-the-dns-wmi-provider"></a><span data-ttu-id="d93cd-103">Vue d’ensemble de l’utilisation du fournisseur WMI DNS</span><span class="sxs-lookup"><span data-stu-id="d93cd-103">Overview of Using the DNS WMI Provider</span></span>

<span data-ttu-id="d93cd-104">Les étapes générales suivantes vous permettent de commencer à créer votre propre script ou programme qui utilise le fournisseur WMI DNS.</span><span class="sxs-lookup"><span data-stu-id="d93cd-104">The following general steps get you started in creating your own script or program that makes use of the DNS WMI Provider.</span></span>

<span data-ttu-id="d93cd-105">**Pour créer un script ou un programme à l’aide du fournisseur WMI DNS**</span><span class="sxs-lookup"><span data-stu-id="d93cd-105">**To create a script or program using the DNS WMI Provider**</span></span>

1.  <span data-ttu-id="d93cd-106">Connectez-vous au fournisseur WMI DNS.</span><span class="sxs-lookup"><span data-stu-id="d93cd-106">Connect to the DNS WMI Provider.</span></span>
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > <span data-ttu-id="d93cd-107">L’espace de noms pour le fournisseur WMI DNS sera toujours « racine \\ MicrosoftDNS ».</span><span class="sxs-lookup"><span data-stu-id="d93cd-107">The name space for the DNS WMI Provider will always be "root\\microsoftdns".</span></span>

     

2.  <span data-ttu-id="d93cd-108">Obtenir une instance de serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="d93cd-108">Get a DNS Server instance.</span></span>
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  <span data-ttu-id="d93cd-109">En fonction de l’action de type que vous souhaitez effectuer, récupérez une zone DNS ou une instance d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d93cd-109">Depending on the type action you want to perform, get a DNS zone or record instance.</span></span>
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  <span data-ttu-id="d93cd-110">Effectuez les actions souhaitées :</span><span class="sxs-lookup"><span data-stu-id="d93cd-110">Perform the desired actions:</span></span>
    -   <span data-ttu-id="d93cd-111">Exécuter une méthode</span><span class="sxs-lookup"><span data-stu-id="d93cd-111">Execute a method</span></span>
    -   <span data-ttu-id="d93cd-112">Afficher une propriété</span><span class="sxs-lookup"><span data-stu-id="d93cd-112">Display a property</span></span>
    -   <span data-ttu-id="d93cd-113">Modifier une propriété (doit avoir un accès en lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="d93cd-113">Modify a property (must have Read/Write access)</span></span>

 

 





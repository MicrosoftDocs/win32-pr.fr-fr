---
title: Utilisation de l’API du serveur des Services de déploiement Windows
description: dans les environnements où la solution standard Windows Deployment Services (WDS) ne peut pas être utilisée, le serveur wds expose une API qui permet aux développeurs d’écrire des plug-ins, appelés fournisseurs, pour gérer les demandes de l’environnement d’exécution de prédémarrage (PXE).
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Windows services de déploiement Windows les services de déploiement, à l’aide de l’API serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ce7516e5279fecdfeecfa90edd8e3a0dad265562fa5ea59336367dbe157c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999569"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Utilisation de l’API du serveur des Services de déploiement Windows

dans les environnements où la solution standard Windows Deployment Services (WDS) ne peut pas être utilisée, le serveur wds expose une API qui permet aux développeurs d’écrire des plug-ins, appelés fournisseurs, pour gérer les demandes de l’environnement d’exécution de prédémarrage (PXE). Les développeurs doivent respecter les consignes suivantes lors de l’écriture de fournisseurs PXE pour WDS.

## <a name="install-the-wds-role-on-the-server"></a>Installer le rôle WDS sur le serveur

-   Windows Services de déploiement (WDS) est la version révisée des services d’installation à distance (RIS), vous aurez besoin du rôle serveur WDS pour implémenter le serveur et les fournisseurs PXE WDS.
-   WDS remplace RIS comme composant standard à partir de Windows server 2008 et Windows server 2003 avec Service Pack 2 (SP2).
-   vous devez mettre à jour le serveur RIS vers WDS sur Windows server 2003 avec Service Pack 1 (SP1). vous pouvez installer le rôle serveur WDS avec le [Kit d’installation automatisée (Windows AIK) (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="register-providers"></a>Inscrire des fournisseurs

-   Enregistrez la bibliothèque de liens dynamiques (DLL) du fournisseur pendant son installation et insérez le fournisseur dans la liste ordonnée des fournisseurs inscrits.
    > [!Note]  
    > Lorsque vous installez un fournisseur nouveau ou modifié, vous devrez redémarrer le service PXE WDS pour que les modifications prennent effet.

     

-   Utilisez la fonction [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) pour inscrire le fournisseur et l’ajouter à la liste. Utilisez la fonction [**PxeProviderUnRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) pour annuler l’inscription d’un fournisseur inscrit et le supprimer de la liste.
-   Spécifiez la séquence du fournisseur dans la liste triée. L’index d’un fournisseur dans la liste ne peut pas être garanti, car un autre fournisseur peut être inscrit plus tard. Pour insérer le fournisseur dans la liste avant ou après un autre fournisseur inscrit, utilisez d’abord la fonction [**PxeProviderQueryIndex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) pour obtenir l’index du fournisseur inscrit, puis enregistrez le nouveau fournisseur tout en spécifiant une valeur d’index plus grande ou plus petite.
-   L’installation peut stocker les informations de configuration du fournisseur sous la clé de Registre retournée lors de l’inscription du fournisseur. L’adresse de la clé de Registre est reçue par le *phProviderKey* de [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister). Le fournisseur reçoit un descripteur de cette même clé que le paramètre *hProviderKey* pour son rappel [*PxeProviderInitialize*](pxeproviderinitialize.md) . Le fournisseur doit stocker l’adresse de cette clé.
-   Installez toujours la bibliothèque de liens dynamiques (DLL) du fournisseur dans le dossier Program Files du serveur.

## <a name="initialize"></a>Initialiser

-   Incluez une DLL qui exporte la fonction de rappel [*PxeProviderInitialize*](pxeproviderinitialize.md) dans le fournisseur. Chaque fournisseur requiert un rappel *PxeProviderInitialize* . Lorsque WDS charge un fournisseur, il appelle la fonction *PxeProviderInitialize* du fournisseur et passe un handle à la même clé que celle utilisée pour stocker les informations de configuration pendant l’inscription du fournisseur.
-   Lorsque le rappel [*PxeProviderInitialize*](pxeproviderinitialize.md) retourne et réussit, le fournisseur doit être entièrement initialisé et prêt à traiter les demandes.
-   Inscrivez chaque rappel dans le fournisseur pendant le traitement de la fonction [*PxeProviderInitialize*](pxeproviderinitialize.md) . Les rappels doivent être inscrits avec la fonction [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) .
-   Initialiser toutes les ressources internes du fournisseur dans le traitement de sa fonction [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="shutdown"></a>Éteindre

-   Implémentez le rappel [*PxeProviderShutdown*](pxeprovidershutdown.md) . Chaque fournisseur doit avoir un rappel *PxeProviderShutdown*.
-   La fonction de rappel [*PxeProviderShutdown*](pxeprovidershutdown.md) doit arrêter complètement le fournisseur et libérer toutes ses ressources.
-   Une fois le rappel [*PxeProviderShutdown*](pxeprovidershutdown.md) retourné, le descripteur *hProvider* passé à la fonction [*PxeProviderInitialize*](pxeproviderinitialize.md) n’est plus valide et ne doit pas être utilisé pour appeler WDS.
-   Inscrivez le rappel [*PxeProviderShutdown*](pxeprovidershutdown.md) en appelant la fonction [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec **l' \_ \_ arrêt du rappel PXE** pendant le traitement du rappel [*PxeProviderInitialize*](pxeproviderinitialize.md) . N’appelez pas le rappel *PxeProviderShutdown* en cas d’échec de la fonction *PxeProviderInitialize* .

## <a name="handle-request-packet"></a>Traiter le paquet de demande

Implémentez le rappel [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) pour le fournisseur. Chaque fournisseur doit avoir un rappel *PxeProviderRecvRequest* . Lorsque WDS reçoit une demande, il appelle le rappel *PxeProviderRecvRequest* pour le premier fournisseur dans la liste des fournisseurs inscrits.

-   Si le fournisseur traitera cette demande de manière synchrone, la fonction [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) doit retourner une valeur **de \_ succès d’erreur**. Si et seulement si le fournisseur traitera cette demande de manière asynchrone, le rappel *PxeProviderRecvRequest* doit retourner des **\_ e/s d’erreur \_ en attente** et appeler la fonction [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) lorsque la requête a été traitée.
-   Le rappel [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) et la fonction [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) renvoient l’adresse d’une énumération d' **\_ \_ action de démarrage PXE** qui décrit l’action effectuée par le fournisseur pour traiter la demande.

    Un fournisseur peut gérer une requête de quatre façons :

    -   Le fournisseur répond au client avec un paquet de réponse DHCP standard qui contient un chemin d’accès au programme de démarrage réseau. Le renvoi de la valeur du **\_ \_ NBP PXE BA** pour l’énumération signifie que le fournisseur a réussi à traiter le paquet de demande et a terminé la demande en envoyant un paquet de réponse en appelant les fonctions [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) et [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   Le fournisseur répond au client avec un paquet de réponse personnalisé qui n’est pas conforme au protocole DHCP. Si vous renvoyez la valeur **\_ \_ personnalisée PXE BA** pour l’énumération, le fournisseur a réussi à traiter le paquet de demande et a terminé la demande en envoyant un paquet de réponse personnalisé en appelant les fonctions [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) et [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   Le fournisseur détermine que la requête doit être ignorée. Le renvoi de la valeur d' **\_ \_ ignore PXE BA** pour l’énumération signifie que le fournisseur a libéré toutes les ressources associées à la demande et que la demande n’est pas transmise au fournisseur suivant dans la liste des fournisseurs inscrits. Les fournisseurs peuvent utiliser cette option s’ils détectent qu’un paquet de demande n’est pas valide.
    -   Le fournisseur refuse de traiter la demande. Le retour de la valeur de **\_ \_ rejet PXE BA** pour l’énumération indique au système de transmettre la demande au fournisseur suivant dans la liste des fournisseurs inscrits. S’il s’agit du dernier fournisseur dans la liste, cela libère toutes les ressources associées à la demande et la demande est ignorée.
    -   Inscrivez le rappel [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) en appelant la fonction [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec **la \_ \_ \_ demande de rappel PXE** lors du traitement du rappel [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="generate-response-packet"></a>Générer un paquet de réponse

-   Utilisez l’API pour écrire des fournisseurs afin de gérer les demandes DHCP et de générer des paquets de réponse.
-   La fonction [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) spécifie les attributs utilisés par le fournisseur pour filtrer les paquets. Les attributs du fournisseur peuvent être spécifiés pour que le fournisseur puisse voir tous les paquets, le fournisseur ne voit que les paquets DHCP, ou le fournisseur voit uniquement les paquets DHCP qui spécifient l’option d’identificateur de classe du fournisseur DHCP (60) comme « PXEClient ».
-   La fonction [**PxeDhcpIsValid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) vérifie qu’un paquet est un paquet DHCP valide. Les fournisseurs peuvent utiliser la fonction **PxeDhcpIsValid** pour vérifier si un paquet du client est un paquet DHCP lorsque le filtre défini avec la fonction [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) est défini de façon à recevoir tous les paquets pour déterminer si un paquet spécifié est un paquet DHCP valide.
-   La fonction [**PxeDhcpInitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) Initialise un paquet de réponse en tant que paquet de réponse DHCP basé sur les informations contenues dans un paquet reçu du client. La fonction [*PxeProviderInitialize*](pxeproviderinitialize.md) prend l’adresse d’un paquet DHCP valide reçu du client dans le rappel [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) . La fonction **PxeDhcpInitialize** prend un pointeur vers un paquet de réponse alloué avec la fonction [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) .
-   La fonction [**PxeDhcpGetOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) récupère une valeur d’option à partir d’un paquet DHCP. La fonction [**PxeDhcpGetVendorOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) récupère une valeur d’option à partir du champ informations spécifiques au fournisseur (43) d’un paquet DHCP.
-   Le fournisseur peut ensuite remplir le paquet de réponse avec les informations et utiliser la fonction [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) pour envoyer le paquet de réponse au client. La fonction [**PxeDhcpAppendOption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) ajoute une option DHCP au paquet de réponse.
-   Un fournisseur qui répond aux demandes des clients en envoyant un paquet doit allouer le paquet de réponse à l’aide de la fonction [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) . Le fournisseur peut ensuite remplir le paquet de réponse avec les informations et utiliser la fonction [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) pour envoyer le paquet de réponse au client.
-   Lorsque la mémoire allouée n’est plus nécessaire, le fournisseur doit la libérer à l’aide de la fonction [**PxePacketFree**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree) .

## <a name="enumerate-registered-providers"></a>Énumérer les fournisseurs inscrits

-   Utilisez l’API pour écrire des fournisseurs qui énumèrent et vérifient d’autres fournisseurs inscrits dans la liste.
-   La fonction [**PxeGetServerInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) retourne des informations sur le serveur PXE. La fonction **PxeGetServerInfo** retourne une valeur **booléenne** qui indique si le suivi est activé pour le serveur. **True** indique que le suivi est activé.
-   La fonction [**PxeProviderEnumFirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) démarre un fournisseur enumerationof dans la liste des fournisseurs inscrits. La fonction **PxeProviderEnumFirst** démarre l’énumération et retourne l’adresse du handle qui doit être utilisé lors de l’appel de la fonction [**PxeProviderEnumNext**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) . La fonction **PxeProviderEnumNext** retourne une structure de [**\_ fournisseur PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) contenant les informations relatives au fournisseur. La fonction [**PxeProviderFreeInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) libère la mémoire qui a été allouée pour la structure du **\_ fournisseur PXE** par la fonction **PxeProviderEnumNext** . La fonction [**PxeProviderEnumClose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) ferme l’énumération des fournisseurs dans la liste des fournisseurs inscrits.

## <a name="handle-service-control-codes"></a>Gérer les codes de contrôle de service

-   Lorsqu’un message de contrôle de service est reçu, WDS appelle le rappel [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) .
-   Le fournisseur peut définir une fonction de rappel [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) pour gérer les messages de contrôle de service.
-   Inscrivez le rappel [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) en appelant la fonction [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec **le \_ \_ \_ contrôle du service de rappel PXE** pendant le traitement du rappel [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="add-trace-entries-to-pxe-log"></a>Ajouter des entrées de trace au Journal PXE

-   La fonction [**PxeTrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) ajoute une entrée de trace au Journal PXE. WDSPXE fournit un suivi pour aider les administrateurs à résoudre les problèmes. Les fournisseurs peuvent enregistrer des entrées de suivi de différents niveaux de gravité. Les administrateurs peuvent configurer WDSPXE pour qu’il consigne uniquement les entrées de certains niveaux de gravité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de l’API Windows Deployment Services](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Utilisation de l’API du client des Services de déploiement Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 





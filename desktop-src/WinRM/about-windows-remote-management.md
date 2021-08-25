---
title: à propos de Windows Remote Management
description: Windows la gestion à distance est un composant de la Windows fonctionnalités de gestion matérielle qui gèrent le matériel serveur localement et à distance.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- à propos de Windows Remote Management
- Windows Gestion à distance, à propos de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a83df38de4af354f826b9bbba59ddab76e1b656c72e1c3dc74301da883f875cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858909"
---
# <a name="about-windows-remote-management"></a>à propos de Windows Remote Management

Windows la gestion à distance est un composant de la Windows fonctionnalités de [gestion matérielle](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) qui gèrent le matériel serveur localement et à distance. Ces fonctionnalités incluent un service qui implémente le protocole [*WS-Management*](windows-remote-management-glossary.md) , le diagnostic matériel et le contrôle via les contrôleurs Baseboard Management Controllers ([*contrôleurs BMC*](windows-remote-management-glossary.md)), ainsi qu’une API com et des [objets de script](winrm-scripting-api.md) qui vous permettent d’écrire des applications qui communiquent à distance par le biais du protocole WS-Management. Pour plus d’informations sur la spécification publique du protocole WS-Management, consultez [gestion des services Web (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

## <a name="components-of-winrm-and-hardware-management"></a>Composants de WinRM et gestion du matériel

La liste suivante répertorie les composants et les fonctionnalités fournis par WinRM et l’analyse du matériel :

-   [API de script WinRM](winrm-scripting-api.md)

    Cette API de script vous permet d’obtenir des données à partir d’ordinateurs distants à l’aide de scripts qui effectuent WS-Management opérations de protocole.

-   **WinRM. cmd**

    cet outil de ligne de commande pour la gestion du système est implémenté dans un fichier d’édition de script Visual Basic (Winrm.vbs) écrit à l’aide de l’API de script WinRM. Cet outil permet à un administrateur de configurer WinRM et d’extraire des données ou de gérer des ressources. Pour plus d’informations, consultez l’aide en ligne fournie par la ligne de commande **WinRM** **/ ?**.

-   **Winrs.exe**

    Cet outil de ligne de commande permet aux administrateurs d’exécuter à distance la plupart des commandes Cmd.exe à l’aide du protocole WS-Management. Pour plus d’informations, consultez l’aide en ligne fournie par la ligne de commande **Winrs** **/ ?**.

-   Pilote IPMI (Intelligent Platform Management Interface) et fournisseur WMI

    La gestion du matériel via le fournisseur et le pilote [*IPMI (Intelligent Platform Management Interface)*](windows-remote-management-glossary.md) vous permet de contrôler et de diagnostiquer le matériel du serveur distant via contrôleurs BMC lorsque le système d’exploitation n’est pas en cours d’exécution ou déployé.

    Pour plus d’informations, consultez le [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   Service WMI

    Le service WMI continue à s’exécuter côte à côte avec WinRM et fournit les données ou le contrôle demandés via le [*plug-in WMI*](windows-remote-management-glossary.md). Vous pouvez continuer à obtenir des données à partir de classes WMI standard, telles que le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process), ainsi que des données fournies par IPMI. Pour plus d’informations sur la configuration et l’installation requises pour WinRM, consultez Introduction à la [gestion du matériel](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

-   Protocole WS-Management

    WS-Management protocole, protocole SOAP, compatible avec un pare-feu, a été conçu pour permettre aux systèmes de localiser et d’échanger des informations de gestion. L’objectif de la spécification du protocole WS-Management est de fournir une interopérabilité et une cohérence pour les systèmes d’entreprise qui possèdent des ordinateurs s’exécutant sur divers systèmes d’exploitation de différents fournisseurs.

    WS-Management protocole est basé sur les spécifications de service Web standard suivantes : HTTPs, SOAP sur HTTP (profil WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration et WS-Eventing. Pour plus d’informations sur le brouillon actuel de la spécification, consultez la [page d’index des spécifications de gestion](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Utilisation de WinRM

pour plus d’informations sur l’écriture de scripts WinRM, consultez [utilisation de Windows Remote Management](using-windows-remote-management.md).

Le tableau suivant répertorie les rubriques qui fournissent des informations sur le protocole WS-Management, WinRM et WMI, sur la façon de spécifier des ressources de gestion, telles que des lecteurs de disque ou des processus.



| Rubrique                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Installation et Configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md) | L' [*écouteur*](windows-remote-management-glossary.md) WinRM requiert une configuration sur les ordinateurs client et serveur.                                                                                                                                                                                                                               |
| [Windows Architecture de gestion à distance](windows-remote-management-architecture.md)                                             | Diagramme illustrant les composants de WinRM et les composants qui se trouvent sur les ordinateurs clients et serveurs.                                                                                                                                                                                                                                                               |
| [Protocole Gestion des services web](ws-management-protocol.md)                                                                             | Description du protocole WS-Management standard public pour l’envoi et la réception à distance de données de gestion sur tout périphérique d’ordinateur qui implémente le protocole.                                                                                                                                                                                                             |
| [scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)                                             | L’API de script WinRM est similaire aux actions du protocole WS-Management. Les données récupérées par les scripts sont au format XML, et non des objets.                                                                                                                                                                                                                                  |
| [Authentification des connexions à distance](authentication-for-remote-connections.md)                                               | WS-Management protocole maintient la sécurité pour le transfert de données entre les ordinateurs en prenant en charge plusieurs méthodes standard d’authentification et de chiffrement des messages.                                                                                                                                                                                                                |
| [Windows Gestion à distance et WMI](windows-remote-management-and-wmi.md)                                                       | comme WinRM est intégré à [Windows Management Instrumentation (wmi)](/windows/desktop/WmiSdk/wmi-start-page), vous pouvez obtenir des données WMI avec des scripts ou des applications qui utilisent l' [API de script winrm](winrm-scripting-api.md) ou via l’outil en ligne de commande winrm.                                                                                                                     |
| [URI de ressource](resource-uris.md)                                                                                               | Un [*URI de ressource*](windows-remote-management-glossary.md) est un identificateur pour une opération ou une valeur de gestion. Par exemple, les lecteurs de disque représentent un type de ressource.                                                                                                                                                                              |
| [Gestion matérielle à distance](remote-hardware-management.md)                                                                     | Le [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) fournit des [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) et des données qui décrivent le domaine de gestion du matériel du contrôleur BMC (Baseboard Management Controller), les systèmes informatiques BMC dans le domaine et les capteurs BMC. Les autres objets représentent le journal des événements système (SEL) BMC et les messages dans le journal. |
| [Événements](events.md)                                                                                                             | Vous ne pouvez pas obtenir d’événements par le biais de scripts WinRM, mais vous pouvez utiliser l’outil de ligne de commande Wevtutil.exe pour afficher les événements du [collecteur d’événements](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .                                                                                                                                                                                        |



 

 

 
---
title: Architecture Windows Remote Management
description: L’architecture Windows Remote Management se compose de composants sur les ordinateurs clients et serveurs.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729188"
---
# <a name="windows-remote-management-architecture"></a>Architecture Windows Remote Management

L’architecture Windows Remote Management se compose de composants sur les ordinateurs clients et serveurs. L’illustration suivante montre les composants sur les deux ordinateurs, la façon dont les composants interagissent avec d’autres composants et le protocole utilisé pour la communication entre les ordinateurs.

![architecture WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a>Client demandeur

Les composants WinRM suivants résident sur l’ordinateur qui exécute le script qui demande des données.

-   Application WinRM

    Il s’agit du script ou de l’outil de ligne de commande **WinRM** qui utilise l’API de script WinRM pour effectuer des appels pour demander des données ou exécuter des méthodes. Pour plus d’informations, consultez l' [API de script WinRM](winrm-scripting-api.md).

-   WSMAuto.dll

    Couche Automation qui fournit la prise en charge des scripts.

-   WsmCL.dll

    Couche d’API C dans le système d’exploitation.

-   API HTTP

    WinRM requiert la prise en charge du transport HTTP et HTTPs.

## <a name="responding-server"></a>Serveur de réponse

Les composants WinRM suivants résident sur l’ordinateur qui répond.

-   API HTTP

    WinRM requiert la prise en charge du transport HTTP et HTTPs.

-   WSMAuto.dll

    Couche Automation qui fournit la prise en charge des scripts.

-   WsmCL.dll

    Couche d’API C dans le système d’exploitation.

-   WsmSvc.dll

    Service d' [*écoute*](windows-remote-management-glossary.md) WinRM.

-   WsmProv.dll

    Sous-système du fournisseur.

-   WsmRes.dll

    Fichier de ressources.

-   WsmWmiPl.dll

    [*Plug-in WMI*](windows-remote-management-glossary.md). Cela vous permet d’obtenir des données WMI via WinRM.

-   Pilote IPMI (Intelligent Platform Management Interface) et fournisseur IPMI WMI

    Ces composants fournissent toutes les données matérielles demandées à l’aide des classes IPMI. Pour plus d’informations, consultez [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). Le matériel BMC doit avoir été détecté par le SMBIOS ou l’appareil créé manuellement par le chargement du pilote. Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> </dl>

 

 
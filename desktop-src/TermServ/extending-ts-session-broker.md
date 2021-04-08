---
title: Extension de session Broker des services Terminal Server
description: Vous pouvez étendre TS \ 160 ; Session Broker à l’aide de l’interface IWTSSBPlugin COM.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729292"
---
# <a name="extending-terminal-services-session-broker"></a>Extension de session Broker des services Terminal Server

Session Broker TS (session Broker TS) détermine si une session est déjà ouverte pour un utilisateur qui initie une connexion. Dans ce cas, le service session Broker TS achemine la connexion entrante vers le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) avec la session existante. Si ce n’est pas le cas, le service session Broker TS achemine la connexion entrante vers le serveur hôte de session Bureau à distance avec le moins de sessions.

Vous pouvez étendre session Broker TS à l’aide de l’interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) com. Vous pouvez utiliser cette interface pour gérer les connexions aux serveurs hôtes de session Bureau à distance, ainsi qu’à tout type de connexion protocole RDP (Remote Desktop Protocol) (RDP), par exemple, les connexions aux machines virtuelles invitées qui exécutent Windows Vista Enterprise central Desktop (VECD) sur un ordinateur hôte d’ordinateur virtuel Hyper-V Windows Server 2008.

L’interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) offre plusieurs avantages :

-   Il n’est pas nécessaire d’installer un agent sur le client ou le serveur hôte de session Bureau à distance.
-   Le plug-in peut interagir de façon transparente avec d’autres services de rôle Services Bureau à distance, tels que Bureau à distance passerelle (passerelle des services Bureau à distance), et s’appuyer sur les informations de session Broker TS sur les États de session et d’ordinateur.
-   Vous pouvez utiliser le plug-in pour gérer les connexions avec des appareils client ou serveur qui prennent en charge RDP 5,2 ou une version ultérieure.
-   Vous pouvez utiliser le plug-in pour activer les solutions de bureau centralisées de Windows Vista Enterprise.

Lorsque vous implémentez les méthodes de cette interface, gardez les points suivants à l’esprit :

-   Session Broker TS peut appeler les méthodes de cet objet COM à partir de plusieurs threads.
-   Si l’une des méthodes appelées ne retourne pas immédiatement et avec succès, le service session Broker TS n’effectue plus d’appels au plug-in et revient à sa logique d’équilibrage de charge native. Pour reprendre les appels au plug-in, vous devez redémarrer le service session Broker des services Terminal Server.
-   Vous devez inscrire le plug-in en tant qu’objet COM à l’ensemble du système à l’aide de Regsvr32.exe. Étant donné que le service session Broker des services Terminal Server s’exécute sous le compte « NetworkService », vous devez accorder au compte « NetworkService » les autorisations de lancement, d’activation et d’accès requises à l’aide de Dcomcnfg.exe. Le service session Broker TS recherche le CLSID de l’objet COM qui représente le plug-in dans la sous-clé de Registre suivante :

    **HKEY \_ Paramètres \_** de Tssdis des services de l’ordinateur local \\  \\  \\  \\  \\ **paramètres** \\ **ExtensibilityPluginCLSID**

Pour plus d’informations sur la Dcomcnfg.exe, consultez Activation de la [sécurité com à l’aide de DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 
---
title: Utilisation de Services Bureau à distance
description: Comment programmer dans l’environnement Services Bureau à distance et comment étendre la technologie Services Bureau à distance (anciennement appelée services Terminal Server) au Web à l’aide de Connexion Bureau à distance par le Web.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217372"
---
# <a name="using-remote-desktop-services"></a>Utilisation de Services Bureau à distance

Les sections suivantes décrivent comment programmer dans l’environnement Services Bureau à distance et comment étendre la technologie Services Bureau à distance (anciennement appelée services Terminal Server) au Web à l’aide de Connexion Bureau à distance par le Web. si vous recherchez des informations sur l’utilisateur pour les connexions Bureau à distance, consultez [Connecter vers un autre ordinateur à l’aide de Connexion Bureau à distance](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Cette rubrique est destinée aux développeurs de logiciels.

 

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Détection de l’installation du rôle Services Bureau à distance](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

exemple de code C# qui montre une méthode qui retourne la **valeur True** si le rôle serveur Services Bureau à distance est installé et en cours d’exécution ou **false** dans le cas contraire, en commençant par Windows server 2008.

</dd> <dt>

[Extension de session Broker des services Terminal Server](extending-ts-session-broker.md)
</dt> <dd>

Vous pouvez étendre session Broker TS à l’aide de l’interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) com.

</dd> <dt>

[Implémentation d’un énumérateur de point de terminaison audio personnalisé](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

à partir de Windows Server 2008 R2, vous pouvez implémenter un énumérateur de point de terminaison audio distant personnalisé dans le cadre d’un fournisseur de protocole Bureau à distance.

</dd> <dt>

[Monikers de session](session-monikers.md)
</dt> <dd>

DCOM (Distributed COM) permet l’activation d’objets pour chaque session à l’aide d’un moniker de session fourni par le système.

</dd> <dt>

[Utilisation de l’extension ADSI pour Services Bureau à distance Configuration utilisateur](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

L’administration des propriétés utilisateur spécifiques à Services Bureau à distance est possible en utilisant les méthodes implémentées par l’extension ADSI (Active Directory Service Interfaces), qui est empaquetée avec la bibliothèque de liens dynamiques Tsuserex.dll.

</dd> <dt>

[Utilisation de l’API Services Bureau à distance](using-the-terminal-services-api.md)
</dt> <dd>

Décrit comment vous pouvez utiliser l’API Services Bureau à distance pour permettre aux applications d’effectuer des tâches dans un environnement Services Bureau à distance.

</dd> <dt>

[Utilisation de l’API de virtualisation Bureau à distance](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Les développeurs peuvent utiliser cette API pour personnaliser la logique que Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance) utilise pour déterminer la destination la plus appropriée pour une connexion cliente entrante.

</dd> <dt>

[Interface WSDL pour les solutions VDI personnalisées](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Les développeurs peuvent créer des services Web personnalisés qui gèrent les solutions VDI (Virtual Desktop Infrastructure).

</dd> </dl>

Pour plus d’informations, consultez [services Bureau à distance les instructions de programmation](terminal-services-programming-guidelines.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Les services Terminal Server sont désormais Services Bureau à distance](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Détection de l’environnement de Services Bureau à distance](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 





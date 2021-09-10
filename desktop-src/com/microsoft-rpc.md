---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363295"
---
# <a name="microsoft-rpc"></a>Microsoft RPC

Microsoft RPC est un modèle de programmation dans un environnement informatique distribué. L’objectif de RPC est de fournir une communication transparente afin que le client semble communiquer directement avec le serveur. L’implémentation de RPC de Microsoft est compatible avec le RPC de l’environnement d’exécution distribué (ETCD) Open Software Foundation (OSF).

Vous pouvez configurer RPC pour utiliser un ou plusieurs transports, un ou plusieurs services de noms et un ou plusieurs serveurs de sécurité. Les interfaces à ces fournisseurs sont gérées par RPC. Étant donné que Microsoft RPC est conçu pour fonctionner avec plusieurs fournisseurs, vous pouvez choisir les fournisseurs qui conviennent le mieux à votre réseau. Le transport est responsable de la transmission des données sur le réseau. Le service de noms prend un nom d’objet, tel qu’un moniker, et trouve son emplacement sur le réseau. Le serveur de sécurité offre aux applications la possibilité de refuser l’accès à des utilisateurs et/ou des groupes spécifiques. Pour plus d’informations sur la sécurité de l’application, consultez [règles de conception d’interface](interface-design-rules.md) .

En plus des bibliothèques Runtime RPC, Microsoft RPC comprend le langage IDL (Interface Definition Language) et son compilateur. Bien que le fichier IDL soit une partie standard de RPC, Microsoft l’a amélioré pour étendre ses fonctionnalités afin de prendre en charge les interfaces COM personnalisées. Le compilateur Microsoft Interface Definition Language (MIDL) utilise le fichier IDL qui décrit votre interface personnalisée pour générer plusieurs fichiers décrits dans [génération et inscription d’une dll proxy](building-and-registering-a-proxy-dll.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Communication entre les objets](inter-object-communication.md)
</dt> <dt>

[Détails du marshaling](marshaling-details.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Talon](stub.md)
</dt> </dl>

 

 





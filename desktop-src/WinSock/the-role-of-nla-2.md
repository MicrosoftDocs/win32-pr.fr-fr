---
description: Le fournisseur de services NLA (Network Location Awareness) est vital pour les ordinateurs ou périphériques qui peuvent se déplacer entre différents réseaux et pour sélectionner des configurations optimales lorsque plusieurs sont disponibles.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Rôle de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f44d517fc9f32d4fb61eb2b4d9b61c473bc946066e670fcb51f0ca2c753e692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733339"
---
# <a name="the-role-of-nla"></a>Rôle de NLA

Le fournisseur de services NLA (Network Location Awareness) est vital pour les ordinateurs ou périphériques qui peuvent se déplacer entre différents réseaux et pour sélectionner des configurations optimales lorsque plusieurs sont disponibles. Par exemple, un ordinateur sans fil itinérant entre des réseaux physiques peut utiliser NLA pour déterminer la configuration appropriée en fonction des informations sur la connexion réseau disponible. NLA s’avère également utile lorsqu’un ordinateur multirésident dispose d’une connexion physique à un réseau, tout en étant connecté à un autre réseau par le biais d’une connexion d’accès à distance ou d’un tunnel.

Par le passé, les développeurs devaient obtenir des informations sur une interface réseau logique et, par conséquent, prendre des décisions sur la connectivité réseau, en se basant sur une multitude d’informations réseau disparates. Dans ces circonstances, les développeurs devaient choisir l’interface réseau appropriée en fonction de l’adresse IP, du sous-réseau de l’interface, du nom DNS (Domain Name System) associé à l’interface, de l’adresse MAC d’une carte réseau, d’un nom de réseau sans fil ou d’autres informations réseau. NLA évite ce problème en fournissant une interface standard pour énumérer les informations de pièce jointe du réseau logique, en la mettant en corrélation avec les informations de l’interface réseau physique, puis en fournissant une notification lorsque les informations précédemment retournées sont invalidées.

NLA fournit les informations d’emplacement réseau suivantes :

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identité du réseau logique
</dt> <dd>

NLA tente d’abord d’identifier un réseau logique par son nom de domaine DNS. Si un réseau logique n’a pas de nom de domaine, NLA identifie le réseau à partir des informations statiques personnalisées stockées dans le registre, et enfin à partir de son adresse de sous-réseau.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfaces réseau logiques
</dt> <dd>

Pour chaque réseau auquel un ordinateur est attaché, NLA fournit un *AdapterName* qui identifie de façon unique une interface physique telle qu’une carte réseau, ou une interface logique telle qu’une connexion RAS. Le AdapterName peut ensuite être utilisé avec les fonctions disponibles dans l’API d’assistance IP pour obtenir d’autres caractéristiques d’interface.

</dd> </dl>

NLA implémente le réseau logique en tant que classe de service, avec un GUID et des propriétés de classe associés. Chaque réseau logique pour lequel NLA retourne des informations est une instance de cette classe de service.

 

 




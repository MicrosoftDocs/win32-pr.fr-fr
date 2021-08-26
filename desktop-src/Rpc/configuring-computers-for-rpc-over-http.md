---
title: Configuration des ordinateurs pour RPC sur HTTP
description: Pour utiliser HTTP comme protocole de transport pour RPC, le proxy RPC exécuté dans Internet Information Server (IIS) doit être configuré sur le réseau du programme serveur.
ms.assetid: 5a67af51-924a-4f2b-b013-a4fd1bfaeddd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4628339afe09e2b6e9a6f216504f411550d37b7a285614e507c89a4a8052c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022469"
---
# <a name="configuring-computers-for-rpc-over-http"></a>Configuration des ordinateurs pour RPC sur HTTP

Pour utiliser HTTP comme protocole de transport pour RPC, le proxy RPC exécuté dans Internet Information Server (IIS) doit être configuré sur le réseau du programme serveur. Cette section décrit les options de configuration. pour obtenir des recommandations sur les meilleures pratiques de programmation et de configuration lors de l’utilisation de rpc sur http, consultez [rpc sur le déploiement http Recommandations](rpc-over-http-deployment-recommendations.md). La tâche principale consiste à configurer le proxy RPC pour accepter et transférer les connexions RPC sur HTTP à un programme serveur RPC sur HTTP.

IIS doit d’abord être installé sur l’ordinateur exécutant le proxy RPC. Une fois IIS installé, le proxy RPC est installé. IIS et le Proxy RPC peuvent être installés simultanément à partir d' **ajout/suppression de Windows composants** dans le panneau de configuration. le proxy rpc est installé à partir des **Services de mise en réseau** et est appelé **proxy rpc sur HTTP** dans Windows installation. si IIS et Proxy RPC sont installés en même temps, Windows s’assure qu’ils sont installés dans le bon ordre.

> [!Note]  
> Une fois l’installation terminée, les services IIS doivent être redémarrés s’ils étaient en cours d’exécution pendant le processus d’installation.

 

Après l’installation du proxy RPC, vous devez effectuer certaines tâches de configuration supplémentaires :

1.  Ouvrez le composant logiciel enfichable MMC IIS et configurez le répertoire virtuel du proxy RPC pour exiger la sécurité, comme expliqué dans la rubrique [sécurité RPC sur http](rpc-over-http-security.md). Cette étape est requise uniquement si vous envisagez d’utiliser RPC sur HTTP v2.
2.  Si IIS n’a pas de certificat installé, un certificat valide doit être obtenu et installé pour cet ordinateur afin d’utiliser SSL lors de la communication avec le proxy RPC. Cette étape s’applique uniquement à RPC sur HTTP v2. Dans la mesure où RPC sur HTTP v1 ne prend pas en charge SSL, cette étape peut être omise pour RPC sur HTTP v1.
3.  Définissez la clé **ValidPorts** comme décrit dans [sécurité RPC sur http](rpc-over-http-security.md).

Lorsque ces tâches de configuration sont terminées, le proxy RPC sur HTTP est prêt à transférer les demandes du client RPC sur HTTP vers le serveur RPC sur HTTP.

## <a name="rpc-over-http-registry-keys"></a>Clés de Registre RPC sur HTTP

Cette section décrit les clés de Registre supplémentaires utilisées pour configurer le client, le serveur ou le proxy RPC dans une connexion RPC sur HTTP. Ces clés ne sont généralement pas requises ; ils sont fournis ici à des fins d’exhaustivité.

**HKLM \\ Software \\ Microsoft \\ RPC \\ DefaultChannelLifetime**

DWORD. Remplace la durée de vie du canal par défaut. Utilisé sur le client et le proxy RPC. La durée de vie du canal est exprimée en octets. S’il n’est pas spécifié, 1 Go est utilisé. Utilisé uniquement dans RPC sur HTTP v2. En cas de modification du proxy RPC, IIS doit être redémarré pour que la modification prenne effet.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ ClientReceiveWindow**

DWORD. Le cas échéant, spécifie la fenêtre de réception utilisée par le client pour les données reçues du proxy RPC. La valeur minimale valide est 8 Ko. La valeur maximale est de 1 Go. Si la valeur n’est pas présente, 64 Ko est utilisé. Utilisé uniquement dans RPC sur HTTP v2.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ InProxyReceiveWindow**

DWORD. Le cas échéant, spécifie la fenêtre de réception utilisée par le proxy RPC pour les données reçues du client. La valeur minimale valide est 8 Ko. La valeur maximale est de 1 Go. Si la valeur n’est pas présente, 64 Ko est utilisé. Utilisé uniquement dans RPC sur HTTP v2. Lorsque des modifications sont apportées à cette valeur, IIS doit être redémarré pour que la modification prenne effet.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ OutProxyReceiveWindow**

DWORD. Le cas échéant, spécifie la fenêtre de réception utilisée par le proxy RPC pour les données reçues du serveur. La valeur minimale valide est 8 Ko. La valeur maximale est de 1 Go. Si la valeur n’est pas présente, 64 Ko est utilisé. Utilisé uniquement dans RPC sur HTTP v2. Lorsque des modifications sont apportées à cette valeur, IIS doit être redémarré pour que la modification prenne effet.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ ServerReceiveWindow**

DWORD. Le cas échéant, spécifie la fenêtre de réception utilisée par le serveur pour les données reçues du proxy RPC. La valeur minimale valide est 8 Ko. La valeur maximale est de 1 Go. Si la valeur n’est pas présente, 64 Ko est utilisé. Utilisé uniquement dans RPC sur HTTP v2. Lorsque des modifications sont apportées à cette valeur, IIS doit être redémarré pour que la modification prenne effet.

\-

**\\stratégies logicielles HKLM \\ \\ Microsoft \\ Windows NT \\ Rpc \\ MinimumConnectionTimeout**

DWORD. Le cas échéant, spécifie le délai de connexion minimal utilisé par le client et le proxy RPC, en secondes. Le délai d’expiration réel utilisé est le plus bas de cette valeur et le délai d’attente de la connexion inactive IIS. Si la valeur est zéro ou si la clé n’est pas présente, le délai d’attente de la connexion inactive IIS est utilisé. Utilisé uniquement dans RPC sur HTTP v2. Lorsque des modifications sont apportées à cette valeur sur le proxy RPC, IIS doit être redémarré pour que la modification prenne effet.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ UseProxyForIPAddrIfRDNSFails**

Lorsqu’elle est présente et définie sur une valeur différente de zéro et qu’une adresse IP numérique est fournie en tant qu’adresse proxy RPC, un client RPC sur HTTP tente une résolution de nom inverse et, en cas d’échec, tente de se connecter au proxy RPC via un proxy HTTP. Peut être utilisé pour émuler Windows comportement NT sur les installations qui requièrent un tel comportement. Ignoré pour RPC sur HTTP v2. Utilisé uniquement en cas d’utilisation de RPC sur HTTP v1. pris en charge uniquement sur Windows 2000 avec Service Pack 3 (SP3) et versions ultérieures.

\-

**HKLM \\ Software \\ Microsoft \\ RPC \\ RpcProxy \\ AllowAnonymous**

DWORD. Lorsqu’il n’est pas présent ou défini à zéro, le proxy RPC vérifie si la connexion est authentifiée et si elle est sécurisée (SSL ou une autre forme de chiffrement est utilisée). Si l’un ou l’autre est false, la connexion est rejetée. Si cette valeur contient des connexions non null, anonymes et non chiffrées sont autorisées. Ce paramètre est un ajout à tous les paramètres du répertoire virtuel. Par exemple, si l’accès anonyme est désactivé au niveau du répertoire virtuel, alors que **AllowAnonymous** est différent de zéro, l’accès anonyme restera bloqué au niveau IIS. Utilisé sur le proxy RPC uniquement dans RPC sur HTTP v2. Lorsque des modifications sont apportées à cette valeur sur le proxy RPC, IIS doit être redémarré pour que la modification prenne effet.

> [!WARNING]
> Microsoft recommande vivement de définir la valeur **AllowAnonymous** sur les systèmes de production pour des raisons de sécurité. La seule raison pour laquelle cette clé doit être définie est le test sur des réseaux fermés sans accès externe. Tout système connecté à Internet et exécutant le proxy RPC avec la clé **AllowAnonymous** définie sur une valeur différente de zéro peut être vulnérable aux attaques.

 

 

 





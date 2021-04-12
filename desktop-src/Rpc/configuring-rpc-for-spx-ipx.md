---
title: Configuration de RPC pour SPX/IPX
description: Lorsque vous utilisez les \_ transports ncacn SPX et ncadg \_ IPX, le nom du serveur est exactement le même que le nom du serveur sur Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462339"
---
# <a name="configuring-rpc-for-spxipx"></a>Configuration de RPC pour SPX/IPX

Lorsque vous utilisez les transports **ncacn \_ SPX** et **ncadg \_ IPX** , le nom du serveur est exactement le même que le nom du serveur sur Windows. Toutefois, étant donné que les noms sont distribués à l’aide de protocoles Novell, ils doivent être conformes aux conventions de nommage de Novell. Si un nom de serveur n’est pas un nom Novell valide, les serveurs ne seront pas en mesure de créer des points de terminaison avec les transports **ncacn \_ SPX** ou **ncadg \_ IPX** .

Un nom de serveur Novell valide contient uniquement les caractères compris entre 0x20 et 0x7F. Les caractères minuscules sont remplacés par des majuscules. Les caractères suivants ne peuvent pas être utilisés :

" \* ,./ :; <=> ?\[\]\\\|\]

Pour assurer la compatibilité avec la première version de Windows NT, **ncacn \_ SPX** et **ncadg \_ IPX** vous permettent également d’utiliser un format spécial du nom de serveur appelé « nom tilde ». Le nom tilde est constitué d’un tilde (~), suivi du numéro de réseau à huit chiffres du serveur, puis de son adresse Ethernet à 12 chiffres. Les noms tilde présentent un avantage en ce qu’ils n’ont pas besoin de fonctionnalités de service de noms. Par conséquent, si vous êtes connecté à un serveur, le nom tilde fonctionne.

Les tableaux suivants contiennent deux exemples de configurations qui illustrent les points décrits précédemment.



| Composant                            | Configuré en tant que      |
|--------------------------------------|--------------------|
| Windows Server                       | NWCS               |
| Client Windows                       | NWCS               |
| client Windows 16 bits, client MS-DOS | Redirecteur NetWare |



 

La configuration du tableau précédent nécessite que vous disposiez de serveurs de fichiers NetWare ou de routeurs sur votre réseau. Les performances sont optimales, car les noms de serveurs sont stockés dans le Bindery NetWare.



| Composant                            | Configuré en tant que |
|--------------------------------------|---------------|
| Windows Server                       | Agent SAP     |
| Client Windows                       | IPX/SPX       |
| client Windows 16 bits, client MS-DOS | IPX/SPX       |



 

La deuxième configuration fonctionne dans un environnement qui ne contient pas de serveurs de fichiers NetWare ou de routeurs (par exemple, un réseau de deux ordinateurs : un serveur Windows et un client MS-DOS). La résolution de noms, qui est effectuée lors du premier appel sur un handle de liaison, sera légèrement plus lente que dans la première configuration. En outre, la deuxième configuration entraîne la génération d’un plus grand trafic sur le réseau.

Pour implémenter la résolution de noms, lorsqu’un serveur RPC utilise un point de terminaison SPX ou IPX, le nom du serveur et le point de terminaison sont enregistrés en tant que serveur SAP (Service Advertising Protocol) de type 640 (hexadécimal). Pour résoudre un nom de serveur, le client RPC envoie une requête SAP pour tous les services du même type, puis analyse la liste des réponses pour le nom du serveur. Ce processus se produit pendant le premier appel RPC sur chaque handle de liaison. Pour plus d’informations sur le protocole SAP pour Novell, consultez la documentation de NetWare.

> [!Note]  
> Les applications clientes Windows 16 bits qui utilisent les transports **ncacn \_ SPX** ou **ncadg \_ IPX** requièrent que le fichier Nwipxspx.dll être installé pour pouvoir s’exécuter sous le sous-système wow. Contactez Novell pour obtenir ce fichier.

 

 

 





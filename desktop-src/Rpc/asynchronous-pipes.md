---
title: Canaux asynchrones
description: L’utilisation de paramètres de canal avec RPC asynchrone vous permet de transmettre des données de façon incrémentielle, dès qu’elles sont disponibles, sans lier le client et le serveur.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729429"
---
# <a name="asynchronous-pipes"></a>Canaux asynchrones

L’utilisation de paramètres de [canal](/windows/desktop/Midl/pipe) avec RPC asynchrone vous permet de transmettre des données de façon incrémentielle, dès qu’elles sont disponibles, sans lier le client et le serveur. Cela s’avère particulièrement utile lorsque vous avez une grande quantité de données à transférer, combiné avec un client lent, un serveur lent ou un réseau lent. Si vous utilisez un canal dans un appel de fonction asynchrone, il s’agit, par définition, d’un canal asynchrone. Les canaux synchrones ne sont pas pris en charge conjointement avec les fonctions asynchrones.

Contrairement aux canaux conventionnels (synchrones) où le serveur gère tous les détails de l’envoi et de la réception des données de canal, les canaux asynchrones sont symétriques. Autrement dit, le client et le serveur peuvent à la fois pousser et extraire des données via le canal.

> [!Note]  
> Les paramètres de canal peuvent uniquement être passés par référence. Même si le fichier IDL affiche des paramètres de [canal](/windows/desktop/Midl/pipe) passés par valeur, les stubs générés acceptent les paramètres de canal par référence uniquement.

 

Dans la discussion suivante sur les canaux asynchrones, il est supposé que vous connaissez le constructeur du type de canal. Pour plus d’informations sur les procédures de canal décrites dans ces rubriques, consultez [canaux](pipes.md).

 

 
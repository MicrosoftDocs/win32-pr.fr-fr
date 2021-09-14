---
title: Syntaxe de transfert et NDR64
description: Le protocole câble NDR, également appelé syntaxe de transfert, permet aux appels RPC de traverser le réseau.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011408"
---
# <a name="transfer-syntax-and-ndr64"></a>Syntaxe de transfert et NDR64

Le protocole câble NDR, également appelé syntaxe de transfert, permet aux appels RPC de traverser le réseau. Le protocole Wire définit la représentation filaire d’un appel RPC, telle que l’ordre dans lequel les membres de données sont marshalés, l’alignement des données sur le câble, les informations supplémentaires incluses dans les données et d’autres problèmes. Le protocole NDR64 est une extension de la syntaxe de transfert de rapport de remise 32 bits, créée spécifiquement pour permettre aux développeurs ciblant des systèmes 64 bits d’obtenir des performances optimisées.

Les différences entre le format de transmission de NDR et le format de câble NDR64 traitent la taille différente des pointeurs dans un environnement 64 bits, ainsi que d’autres problèmes. Le mécanisme de NDR64 est géré par RPC. Les développeurs doivent uniquement utiliser le commutateur de ligne de commande/[**protocole**](/windows/desktop/Midl/-protocol)**tout** MIDL pour bénéficier des avantages de NDR64 sur les plateformes 64 bits. NDR64 est disponible uniquement sur les plateformes 64 bits.

 

 
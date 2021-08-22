---
description: cette section décrit les extensions Winsock spécifiques Exchange à/Sequenced packet Exchange (IPX/SPX). Il décrit également les aspects des fonctions Winsock de base qui requièrent une attention particulière ou qui peuvent présenter un comportement unique.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Annexe IPX/SPX Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e5a97b90dc29f577bf2335b93a15fb3fb2c87c8362e0585151e1ac8b1e3393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051347"
---
# <a name="winsock-ipxspx-annex"></a>Annexe IPX/SPX Winsock

cette section décrit les extensions Winsock spécifiques Exchange à/Sequenced packet Exchange (IPX/SPX). Il décrit également les aspects des fonctions Winsock de base qui requièrent une attention particulière ou qui peuvent présenter un comportement unique.



| Élément          | Description                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom (s) de protocole | IPX, SPX                                                                                                                                        |
| Description      | Fournit des services de transport sur la couche de mise en réseau IPX : IPX pour les datagrammes non fiables, SPX pour les flux de messages fiables et orientés connexion. |
| Famille d’adresses   | \_protocole IPX AF                                                                                                                                         |
| Fichier d’en-tête      | Wsipx. h                                                                                                                                         |



 

Cette section explique comment utiliser Winsock avec la famille de protocoles IPX, ce qui permet de porter les applications IPX traditionnelles vers Winsock. Comme les réseaux IPX fonctionnent de manière fondamentalement différente des réseaux IP, ces différences doivent être prises en compte lors de l’utilisation du protocole IPX/SPX.

 

 




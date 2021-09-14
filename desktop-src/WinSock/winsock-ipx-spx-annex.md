---
description: cette section décrit les extensions Winsock spécifiques Exchange à/Sequenced packet Exchange (IPX/SPX). Il décrit également les aspects des fonctions Winsock de base qui requièrent une attention particulière ou qui peuvent présenter un comportement unique.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Annexe IPX/SPX Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918904"
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

 

 




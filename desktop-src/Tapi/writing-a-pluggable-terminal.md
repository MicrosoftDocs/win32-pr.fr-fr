---
description: Normalement, un fournisseur de services de média (MSP) implémente la création de terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Écriture d’un terminal enfichable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47395515418a4c2fcc66b972674950ca0c58aa8b01276973ea4ab3e91cbd314
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072799"
---
# <a name="writing-a-pluggable-terminal"></a>Écriture d’un terminal enfichable

Normalement, un fournisseur de services de média (MSP) implémente la création de terminal. à compter de Windows 2000 SP1, TAPI 3 comprend des terminaux enfichables pour permettre à une application d’implémenter la création de terminal. Pour plus d’informations sur l’utilisation de ces terminaux, consultez la vue d’ensemble de l' [implémentation de terminaux enfichables](implementing-pluggable-terminals.md) .

Vous ne devez pas utiliser les terminaux enfichables régulièrement, car les fonctionnalités complètes d’un terminal ne sont disponibles que lorsqu’un MSP en est pleinement conscient. En outre, vous ne devez pas tenter d’implémenter des terminaux enfichables, sauf si vous êtes déjà familiarisé avec l’écriture de fournisseurs de services multimédias. Les techniques et problèmes potentiels impliqués sont très similaires.

la mise en service d’un cas particulier de terminal enfichable existe actuellement pour la situation d’un serveur de conférence qui doit ajouter des clients non-Windows 2000 SP1 ou non multicast H. 323 aux conférences de multidiffusion SDP/IP à l’interface TAPI 3.

 

 




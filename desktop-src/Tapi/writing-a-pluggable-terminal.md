---
description: Normalement, un fournisseur de services de média (MSP) implémente la création de terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Écriture d’un terminal enfichable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526811"
---
# <a name="writing-a-pluggable-terminal"></a>Écriture d’un terminal enfichable

Normalement, un fournisseur de services de média (MSP) implémente la création de terminal. À compter de Windows 2000 SP1, TAPI 3 comprend des terminaux enfichables pour permettre à une application d’implémenter la création de terminal. Pour plus d’informations sur l’utilisation de ces terminaux, consultez la vue d’ensemble de l' [implémentation de terminaux enfichables](implementing-pluggable-terminals.md) .

Vous ne devez pas utiliser les terminaux enfichables régulièrement, car les fonctionnalités complètes d’un terminal ne sont disponibles que lorsqu’un MSP en est pleinement conscient. En outre, vous ne devez pas tenter d’implémenter des terminaux enfichables, sauf si vous êtes déjà familiarisé avec l’écriture de fournisseurs de services multimédias. Les techniques et problèmes potentiels impliqués sont très similaires.

La mise en service d’un cas particulier de terminal enfichable existe actuellement pour la situation d’un serveur de conférence qui doit ajouter des clients non-Windows 2000 SP1 ou non multicast H. 323 à des conférences de multidiffusion SDP/IP multiparts TAPI 3.

 

 




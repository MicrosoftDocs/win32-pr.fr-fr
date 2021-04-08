---
title: Interfaces RAS
description: Une interface représente un réseau qui peut être atteint sur une carte réseau local ou WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea285a625377709a4eca3bc8b9947106c2f5cfd
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841721"
---
# <a name="ras-interfaces"></a>Interfaces RAS

Une interface représente un réseau qui peut être atteint sur une carte réseau local ou WAN. Chaque interface possède un identificateur unique sur le routeur. Les interfaces actives disposent d’un adaptateur fournissant une connectivité au réseau qu’ils représentent. Les interfaces inactives n’ont pas d’adaptateur assurant la connectivité, sauf si un administrateur a désactivé l’interface après qu’elle avait déjà un adaptateur.

Le routage d’un paquet vers un réseau représenté par une interface force le routeur à allouer un adaptateur pour cette interface et à établir une connexion de réseau étendu (WAN) au réseau distant. L’allocation d’un adaptateur à une interface est appelée *liaison*.

Les interfaces sont des objets gérables. Chaque interface apparaît sous la forme d’une ligne dans la table d’interface de la MIB SNMP appropriée.
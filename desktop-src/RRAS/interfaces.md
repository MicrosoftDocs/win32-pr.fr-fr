---
title: Interfaces RAS
description: Une interface représente un réseau qui peut être atteint sur une carte réseau local ou WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef716e0db05fe37a0a7d326fbf5f8da878a0628d1deec9e996fcc49d917cc051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030139"
---
# <a name="ras-interfaces"></a>Interfaces RAS

Une interface représente un réseau qui peut être atteint sur une carte réseau local ou WAN. Chaque interface possède un identificateur unique sur le routeur. Les interfaces actives disposent d’un adaptateur fournissant une connectivité au réseau qu’ils représentent. Les interfaces inactives n’ont pas d’adaptateur assurant la connectivité, sauf si un administrateur a désactivé l’interface après qu’elle avait déjà un adaptateur.

Le routage d’un paquet vers un réseau représenté par une interface force le routeur à allouer un adaptateur pour cette interface et à établir une connexion de réseau étendu (WAN) au réseau distant. L’allocation d’un adaptateur à une interface est appelée *liaison*.

Les interfaces sont des objets gérables. Chaque interface apparaît sous la forme d’une ligne dans la table d’interface de la MIB SNMP appropriée.
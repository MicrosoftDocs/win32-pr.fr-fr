---
description: Moniteur réseau fournit trois fonctions de sélection d’une carte d’interface réseau (NIC). Ces fonctions offrent trois façons d’énumérer un ensemble de cartes réseau et de sélectionner celle que vous souhaitez utiliser. Le tableau suivant répertorie ces fonctions.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Sélection d’une carte d’interface réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021031"
---
# <a name="selecting-a-network-interface-card"></a>Sélection d’une carte d’interface réseau

Moniteur réseau fournit trois fonctions de sélection d’une carte d’interface réseau (NIC). Ces fonctions offrent trois façons d’énumérer un ensemble de cartes réseau et de sélectionner celle que vous souhaitez utiliser. Le tableau suivant répertorie ces fonctions.



| Fonction                                                 | Description                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Utilise l’interface utilisateur Moniteur réseau pour afficher les cartes réseau enregistrées et retourne l’objet BLOB NPP qui représente la carte réseau qui vous intéresse.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Retourne une table d’objets BLOB. L’application doit énumérer la table et sélectionner un objet BLOB NPP.                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | Utilise l’interface Moniteur réseau pour afficher les objets BLOB NPP fournis et retourne l’objet BLOB NPP qui représente la carte réseau qui vous intéresse. |



 

Chaque carte d’interface réseau est représentée par un objet BLOB (Binary Large Object) NPP. Ces fonctions peuvent retourner un seul objet BLOB NPP à partir de ceux inscrits sur l’ordinateur, un seul objet BLOB NPP à partir d’une table d’objets BLOB NPP fournie, ou une table d’objets BLOB NPP que l’appelant doit ensuite utiliser pour sélectionner un objet BLOB spécifique. Dans les deux premiers cas, lors de la sélection à partir des cartes réseau inscrites ou d’une table d’objets BLOB NPP fournie, l’interface utilisateur Moniteur réseau affiche les cartes réseau que vous pouvez sélectionner.

> [!Note]  
> Moniteur réseau utilise une fonctionnalité appelée « NPP Finder » pour énumérer les cartes réseau inscrites sur l’ordinateur local. Le Finder NPP est un composant de Npptools.dll.

 



| Pour obtenir des informations sur                            | Consultez                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Sélection d’une carte d’interface réseau inscrite sur l’ordinateur local | [Sélection d’une carte réseau enregistrée](selecting-a-registered-nic.md)                                         |
| Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie   | [Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Récupération d’une table d’objets BLOB NPP                     | [Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 




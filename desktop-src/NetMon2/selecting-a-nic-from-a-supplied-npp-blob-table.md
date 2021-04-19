---
description: Pour sélectionner une carte d’interface réseau (NIC) à partir d’une table d’objets BLOB NPP fournie, appelez la fonction SelectNPPBlobFromTable.
ms.assetid: e75b6bb7-cf21-4e25-80a5-3b35f7ed0d0e
title: Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0215ca258c02745a7e5b4c285d6bf7df98a49e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531879"
---
# <a name="selecting-a-nic-from-a-supplied-npp-blob-table"></a>Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie

Pour sélectionner une carte d’interface réseau (NIC) à partir d’une table d’objets BLOB NPP fournie, appelez la fonction [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) . Cette fonction utilise l’interface utilisateur Moniteur réseau pour afficher les cartes réseau représentées dans la table d’objets BLOB et retourne l’objet BLOB NPP qui représente la carte réseau sélectionnée.

Quand vous appelez la fonction [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) , la boîte de dialogue **Sélectionner un réseau** s’affiche. À partir de celle-ci, vous pouvez afficher les détails du NPPs représenté dans la table d’objets BLOB NPP, sélectionner une carte réseau spécifique et afficher les détails de sa structure d’objet BLOB NPP associée.

L’illustration suivante montre les cartes réseau représentées dans une table d’objets BLOB NPP fournie.

![cartes réseau représentées dans une table d’objets BLOB NPP fournie](images/networkdb2.png)



| Pour plus d’informations sur l’un des sujets suivants :                        | Consultez                                                                                                      |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Sélection d’une carte d’interface réseau inscrite sur l’ordinateur local. | [Comment sélectionner une carte réseau enregistrée](selecting-a-registered-nic.md)                                         |
| Récupération d’une table d’objets BLOB NPP.                     | [Comment sélectionner une carte réseau à partir d’une table BLOB NPP retournée](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 




---
description: Pour sélectionner l’une des cartes réseau inscrites sur l’ordinateur local, appelez la fonction GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Sélection d’une carte réseau enregistrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7643a7bc19cabe6617de92b07a297f635c318686c02ca7caa157128300ed2d10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074422"
---
# <a name="selecting-a-registered-nic"></a>Sélection d’une carte réseau enregistrée

Pour sélectionner l’une des cartes réseau inscrites sur l’ordinateur local, appelez la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) . Cette fonction utilise l’interface utilisateur Moniteur réseau pour afficher les cartes réseau enregistrées et retourne l’objet BLOB NPP qui représente la carte réseau que vous sélectionnez. Vous pouvez afficher toutes les cartes réseau inscrites sur l’ordinateur local ou un plus petit ensemble de cartes réseau filtrées. Pour filtrer les cartes réseau affichées, fournissez un [*objet blob de filtres*](f.md) lorsque l’appel est effectué.

> [!Note]  
> Lorsque la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) est appelée, le [*Finder NPP*](n.md) communique avec les dll NPP pour obtenir les structures BLOB NPP qui représentent les cartes réseau inscrites. Pour plus d’informations et pour obtenir une procédure sur l’utilisation directe de l’interface utilisateur du Moniteur réseau, consultez la rubrique « boîte de dialogue Sélectionner un réseau » dans l’aide en ligne de Moniteur réseau.

 

Quand vous appelez la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) , la boîte de dialogue **Sélectionner un réseau** s’affiche. À partir de celle-ci, vous pouvez afficher les détails du NPPs inscrit sur l’ordinateur local. Ces informations incluent les NPPs locaux et les NPPs distants. À partir de la boîte de dialogue, vous pouvez sélectionner une carte réseau spécifique et afficher les détails de sa structure d’objet BLOB NPP associée.

L’illustration suivante montre les paramètres typiques d’un NPP NDIS fourni par Moniteur réseau.

![paramètres standard d’un NPP NDIS fourni par le moniteur réseau](images/networkdb.png)

Le tableau suivant répertorie les rubriques qui décrivent chaque méthode de sélection de carte réseau.



| Pour obtenir des informations sur                                                                          | Consultez                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Comment spécifier un filtre qui limite les cartes réseau affichées dans la boîte de dialogue **Sélectionner un réseau** . | [Spécification d’un objet BLOB de filtre](specifying-a-filter-blob.md)                                             |
| Comment sélectionner une carte réseau en appelant la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) .      | [Sélection d’une carte réseau à l’aide de GetNPPBlobFromUI](getnppblobfromui.md)                                       |
| Comment sélectionner une carte réseau à partir d’une table d’objets BLOB NPP fournie.                                            | [Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 




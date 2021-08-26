---
description: Pour sélectionner une carte réseau à partir d’une table d’objets BLOB NPP renvoyée par Moniteur réseau, appelez la fonction GetNPPBlobTable. Cette fonction retourne une table d’objets BLOB NPP, qui peut ensuite être énumérée par votre application pour sélectionner la carte réseau qui vous intéresse.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5555e68e04886b390a6b6bd1f9f8372202fe970a4784ffa2652a3fc991c4da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074469"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a>Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée

Pour sélectionner une carte réseau à partir d’une table d’objets BLOB NPP renvoyée par Moniteur réseau, appelez la fonction [**GetNPPBlobTable**](getnppblobtable.md) . Cette fonction retourne une table d’objets BLOB NPP, qui peut ensuite être énumérée par votre application pour sélectionner la carte réseau qui vous intéresse.

Lorsque vous appelez cette fonction, vous pouvez retourner une table d’objets BLOB de toutes les cartes réseau inscrites sur l’ordinateur local ou un plus petit ensemble de cartes réseau filtrées. Pour filtrer les cartes réseau qui sont renvoyées, vous pouvez fournir un [*objet blob de filtre*](f.md) lorsque l’appel est effectué.



| Pour obtenir des informations sur                                                       | Consultez                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Comment spécifier un filtre qui limite les cartes réseau retournées dans une table d’objets BLOB NPP. | [Spécification d’un objet BLOB de filtre](specifying-a-filter-blob.md)                                             |
| Comment sélectionner une carte réseau inscrite sur un ordinateur local.                         | [Sélection d’une carte réseau enregistrée](selecting-a-registered-nic.md)                                         |
| Comment sélectionner une carte réseau à partir d’une table d’objets BLOB NPP fournie                          | [Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 




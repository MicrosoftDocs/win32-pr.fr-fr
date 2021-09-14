---
description: Lorsque vous sélectionnez une carte d’interface réseau (NIC) inscrite répertoriée sur un ordinateur local, vous pouvez utiliser un objet BLOB de filtre pour ignorer les cartes réseau qui ne vous intéressent pas.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Spécification d’un objet BLOB de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194544"
---
# <a name="specifying-a-filter-blob"></a>Spécification d’un objet BLOB de filtre

Lorsque vous sélectionnez une carte d’interface réseau (NIC) inscrite répertoriée sur un ordinateur local, vous pouvez utiliser un [*objet blob de filtre*](f.md) pour ignorer les cartes réseau qui ne vous intéressent pas. Par exemple, vous pouvez limiter la recherche pour un type spécifique de carte (comme ETHERNET) ou une adresse MAC spécifique.

Lors de la recherche d’une carte réseau, chaque entrée de l’objet BLOB de filtre doit correspondre à une entrée équivalente dans l’objet BLOB NPP qui représente la carte réseau. Les objets BLOB de filtres peuvent également être des [*objets BLOB spéciaux*](s.md).

Lorsque la fonction [**GetNPPBlobFromUI**](getnppblobfromui.md) est appelée, l’objet blob de filtres restreint les cartes réseau affichées dans la boîte de dialogue **Sélectionner un réseau** . Lorsque la fonction [**GetNPPBlobTable**](getnppblobtable.md) est appelée, l’objet blob de filtres restreint les cartes réseau retournées dans la table d’objets BLOB.

Pour utiliser le filtre, vous devez créer un objet BLOB de filtre, définir les valeurs des propriétés que vous souhaitez filtrer (y compris les entrées d’objets BLOB spéciales), puis spécifier le filtre d’objet BLOB et un appel à la fonction [**GetNPPBlobTable**](getnppblobtable.md) ou [**GetNPPBlobFromUI**](getnppblobfromui.md) .



| Pour plus d’informations sur                                 | Consultez                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Comment sélectionner une carte réseau inscrite sur un ordinateur local | [Sélection d’une carte réseau enregistrée](selecting-a-registered-nic.md)                                         |
| Récupération d’une table d’objets BLOB NPP                       | [Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 




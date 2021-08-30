---
description: L’action PublishProduct gère la publication des informations sur le produit avec le système. Cette action publie le produit si le produit est en mode publication ou si une fonctionnalité est en cours d’installation ou de réinstallation.
ms.assetid: aba1baf2-d282-4f76-87aa-67188b779535
title: Action PublishProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d674f2d9d7e505f97122e62ff4175392147793f7cc9355e4b1aa2acd21b8bbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913079"
---
# <a name="publishproduct-action"></a>Action PublishProduct

L’action PublishProduct gère la publication des informations sur le produit avec le système. Cette action publie le produit si le produit est en mode publication ou si une fonctionnalité est en cours d’installation ou de réinstallation.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action PublishProduct doit venir après l’action [PublishFeatures](publishfeatures-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action        |
|-------|-----------------------------------|
| \[1\] | Identificateur du produit publié. |



 

 

 




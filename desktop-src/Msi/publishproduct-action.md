---
description: L’action PublishProduct gère la publication des informations sur le produit avec le système. Cette action publie le produit si le produit est en mode publication ou si une fonctionnalité est en cours d’installation ou de réinstallation.
ms.assetid: aba1baf2-d282-4f76-87aa-67188b779535
title: Action PublishProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9edf95ccb736bb4a4388f36d87bfbfbe299573e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119669"
---
# <a name="publishproduct-action"></a>Action PublishProduct

L’action PublishProduct gère la publication des informations sur le produit avec le système. Cette action publie le produit si le produit est en mode publication ou si une fonctionnalité est en cours d’installation ou de réinstallation.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action PublishProduct doit venir après l’action [PublishFeatures](publishfeatures-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action        |
|-------|-----------------------------------|
| \[1\] | Identificateur du produit publié. |



 

 

 




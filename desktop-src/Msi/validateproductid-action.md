---
description: L’Action ValidateProductID définit la propriété ProductID sur l’identificateur complet du produit.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Action ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be241bddbafb8f963aea1e73a2750c9d45766eb06767b0b30142883fa1bcebac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942229"
---
# <a name="validateproductid-action"></a>Action ValidateProductID

L’Action ValidateProductID définit la propriété [**ProductID**](productid.md) sur l’identificateur complet du produit.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Cette action doit être séquencée avant l’Assistant interface utilisateur dans la [table InstallUISequence](installuisequence-table.md) et avant l' [action RegisterUser](registeruser-action.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

Le programme d’installation vérifie si un produit a été validé avec succès en vérifiant la propriété [**ProductID**](productid.md) . Le programme d’installation définit la propriété **ProductID** sur l’identificateur de produit complet après une validation réussie. L’Action ValidateProductID ne fait rien si la propriété **ProductID** a déjà été définie par une validation réussie ou par une autre méthode.

L’Action ValidateProductID retourne toujours un succès, que l’identificateur de produit soit valide ou non, afin que l’identificateur de produit puisse être entré sur la ligne de commande lors de la première exécution du produit.

L’identificateur de produit peut être validé sans que l’utilisateur ne resaisisse ces informations en définissant la propriété [**PIDKEY**](pidkey.md) sur la ligne de commande ou en utilisant une transformation. L’affichage de la boîte de dialogue demandant à l’utilisateur d’entrer l’identificateur de produit peut ensuite être rendu conditionnel sur la présence de la propriété [**ProductID**](productid.md) , qui est définie lorsque la propriété **PIDKEY** est validée.

 

 




---
description: Une séquence de la boîte de dialogue FirstRun collecte le nom d’utilisateur, le nom de la société et les informations d’ID du produit. Le programme d’installation vérifie l’ID de produit au cours de cette boîte de dialogue.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Boîte de dialogue FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201962"
---
# <a name="firstrun-dialog"></a>Boîte de dialogue FirstRun

Une séquence de la boîte de dialogue FirstRun collecte le nom d’utilisateur, le nom de la société et les informations d’ID du produit. Le programme d’installation vérifie l’ID de produit au cours de cette boîte de dialogue.

Une séquence de la boîte de dialogue FirstRun n’est généralement pas une partie de la séquence d’action et est appelée à la place par la fonction [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) lors de la première exécution du produit.

L’auteur d’un package d’installation peut utiliser la séquence de dialogue de modèle ou créer une séquence différente. Toutefois, la séquence de dialogue doit définir les propriétés suivantes pour l’utilisateur :

-   Propriété [**username**](username.md)
-   [**CompanyName**](companyname.md) , propriété
-   [**PIDKEY**](pidkey.md) , propriété

L’ID de produit est validé au cours de la boîte de dialogue à l’aide de l' [Action ValidateProductID](validateproductid-action.md) ou du [ControlEvent, ValidateProductID](validateproductid-controlevent.md).

Si l’ID de produit est défini en tant que propriété sur la ligne de commande ou par une transformation, la nécessité d’avoir à nouveau l’ID de produit dans la boîte de dialogue de première exécution peut être contournée en contrôlant l’affichage à l’aide de la propriété [**ProductID**](productid.md) . Après la validation réussie de l’ID de produit, la propriété **ProductID** est définie sur l’ID de produit complet valide.

 

 




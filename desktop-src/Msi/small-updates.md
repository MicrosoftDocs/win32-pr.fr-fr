---
description: Une petite mise à jour apporte des modifications à un ou plusieurs fichiers d’application qui sont trop mineurs pour justifier la modification du code du produit.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Petites mises à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 392e19507ca37cf865fab44485b93346dd1ad6cf6d81ada212acb2ec11ddb1c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628169"
---
# <a name="small-updates"></a>Petites mises à jour

Une petite mise à jour apporte des modifications à un ou plusieurs fichiers d’application qui sont trop mineurs pour justifier la modification du code du produit. Une petite mise à jour est également communément appelée mise à jour QFE (Quick Fix Engineering). Une petite mise à jour n’autorise pas la réorganisation de l’arborescence des composants de fonctionnalité.

Une petite mise à jour classique ne modifie qu’un ou deux fichiers ou une clé de registre. Étant donné qu’une petite mise à jour modifie les informations dans le fichier .msi, le code du package d’installation doit être modifié. Le code du package est stocké dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) du flux d’informations de [synthèse](summary-information-stream.md).

Le code du produit n’est jamais modifié avec une petite mise à jour. par conséquent, toutes les modifications introduites par une petite mise à jour doivent être cohérentes avec les instructions décrites dans [modification du code du produit](changing-the-product-code.md). Une mise à jour requiert une [mise à niveau majeure](major-upgrades.md) pour modifier la valeur [**ProductCode**](productcode.md). S’il est nécessaire de faire la différence entre les produits sans modifier le code du produit, utilisez une [mise à niveau mineure](minor-upgrades.md).

pour plus d’informations sur l’application d’un package de correctifs de mise à jour à un package de Windows Installer, consultez [création d’un correctif logiciel](creating-a-small-update-patch.md)de petite mise à jour, [application de petites mises à jour en corrigeant l’Installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md)et [application de petites mises à jour en corrigeant une Image Administrative](applying-small-updates-by-patching-an-administrative-image.md).

 

 




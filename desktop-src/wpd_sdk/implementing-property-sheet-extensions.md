---
description: Implémentation des extensions de feuille de propriétés
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implémentation des extensions de feuille de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522068"
---
# <a name="implementing-property-sheet-extensions"></a>Implémentation des extensions de feuille de propriétés

L’extension d’espace de noms WPD prend en charge les feuilles de propriétés extensibles. Il s’agit des boîtes de dialogue de propriétés qui s’affichent lorsqu’un utilisateur clique avec le bouton droit sur un objet, tel qu’un fichier ou un dossier, et sélectionne des **Propriétés**. Certaines applications WPD tirent parti de ces feuilles de propriétés extensibles pour afficher des propriétés pour le contenu côté appareil (ou les objets qui résident sur l’appareil).

Les feuilles de propriétés extensibles sont prises en charge par les interfaces décrites dans le tableau suivant. pour plus d’informations sur l’une de ces interfaces, consultez le SDK Windows.



| Interface           | Description                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | Utilisé pour passer le tableau PIDL du menu contextuel au gestionnaire de menu contextuel.      |
| IPropertySetStorage | Cette interface est utilisée pour récupérer les propriétés WPD pour l’objet donné.      |
| IPropertyStorage    | Cette interface est également utilisée pour récupérer les propriétés WPD pour l’objet donné. |
| IShellExtInit       | initialise les extensions de l’interpréteur de commandes Windows Vista pour le menu contextuel.         |
| IShellPropSheetExt  | Prend en charge l’ajout d’extensions de feuille de propriétés.                              |



 

les feuilles de propriétés pour les api WPD sont implémentées comme toute autre feuille de propriétés dans Windows Vista. Si vous avez déjà implémenté un gestionnaire de feuilles de propriétés, vous pouvez modifier votre code existant afin qu’il prenne en charge le contenu côté appareil. si vous n’avez jamais créé de gestionnaire de menu contextuel, consultez la rubrique création de gestionnaires de feuille de propriétés dans la SDK Windows.

Les deux points à partir desquels un gestionnaire de feuille de propriétés WPD diffère de tout autre gestionnaire se trouvent dans l’inscription du gestionnaire et la prise en charge du contenu côté appareil.

 

 




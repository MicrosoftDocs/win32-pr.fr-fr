---
description: Le code du produit est un GUID qui est l’identification principale d’une application ou d’un produit. Consultez la section codes de produit.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Modification du code du produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0272f1901ef60342f01f4db091e7a4e62b28e30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092282"
---
# <a name="changing-the-product-code"></a>Modification du code du produit

Le code du produit est un GUID qui est l’identification principale d’une application ou d’un produit. Consultez la section [codes de produit](product-codes.md).

Une mise à jour qui respecte les instructions suivantes ne nécessite généralement pas de modification du code du produit et peut être traitée comme une [petite mise à jour](small-updates.md), ou si la version doit être modifiée, comme une [mise à niveau mineure](minor-upgrades.md):

-   La mise à jour peut agrandir ou réduire l’arborescence des composants de fonctionnalité, mais elle ne doit pas réorganiser la hiérarchie existante des fonctionnalités et composants décrits par les tables [Feature](feature-table.md) et [FeatureComponents](featurecomponents-table.md) . Il peut ajouter une nouvelle fonctionnalité à la fonctionnalité existante-arborescence des composants. Si elle supprime une fonctionnalité parente, elle doit également supprimer toutes les fonctionnalités enfants de la fonctionnalité supprimée.
-   La mise à jour peut ajouter un nouveau composant à une fonctionnalité nouvelle ou existante.
-   La mise à jour ne doit pas modifier le code d’un composant. Par conséquent, une petite mise à jour ou une mise à niveau mineure ne doit jamais modifier le nom du fichier de clé d’un composant, car cela nécessiterait la modification du code du composant.
-   La mise à jour ne doit pas modifier le nom du fichier .msi du package d’installation. Au lieu de cela, étant donné qu’elle modifie le package, elle doit modifier le code du package. Notez que cela signifie que la mise à jour peut modifier les tables, les actions personnalisées et les boîtes de dialogue dans le fichier .msi sans modifier le nom du fichier.
-   La mise à jour permet d’ajouter, de supprimer ou de modifier les fichiers, les clés de registre ou les raccourcis de composants qui ne sont pas partagés par au moins deux fonctionnalités. Si la mise à jour modifie un fichier avec version, la version de ce fichier doit être incrémentée dans la [table de fichiers](file-table.md). Si la mise à jour supprime des ressources, elle doit également mettre à jour les tables [RemoveFile](removefile-table.md) et [RemoveRegistry](removeregistry-table.md) pour supprimer les fichiers inutilisés, les clés de registre ou les raccourcis qui ont déjà été installés.
-   La mise à jour d’un composant partagé par deux fonctionnalités ou plus doit être à compatibilité descendante avec toutes les applications et toutes les fonctionnalités qui utilisent le composant. La mise à jour peut modifier la ressource d’un composant partagé, comme les fichiers, les entrées de Registre et les raccourcis, à condition que les modifications soient à compatibilité descendante. Il n’est pas recommandé d’ajouter ou de supprimer des fichiers, des entrées de registre ou des raccourcis à partir d’un composant partagé.
-   une petite mise à jour est fournie en tant que [package correctif](patch-packages.md)Windows Installer. (Un CD-ROM complet du produit n’est généralement pas fourni avec une petite mise à jour.)

Le code du produit doit être modifié si l’une des conditions suivantes est vraie pour la mise à jour :

-   Des installations coexistantes de produits d’origine et mis à jour sur le même système doivent être possibles.
-   Le nom du fichier de .msi a été modifié.
-   Le code du composant d’un composant existant a changé.
-   Un composant est supprimé d’une fonctionnalité existante.
-   Une fonctionnalité existante a été créée dans l’enfant d’une fonctionnalité existante.
-   Une fonctionnalité enfant existante a été supprimée de sa fonctionnalité parente.

Notez que l’ajout d’une nouvelle fonctionnalité enfant, composée uniquement de nouveaux composants, à une fonctionnalité existante ne nécessite pas la modification du code du produit.

Les nouvelles fonctionnalités enfants peuvent être créées en incluant msidbFeatureAttributesFollowParent et msidbFeatureAttributesUIDisallowAbsent dans le champ attributs du [tableau des fonctionnalités](feature-table.md). Si la mise à niveau mineure ajoute uniquement de nouvelles fonctionnalités enfants, puis réinstaller = ALL est suffisant pour forcer l’installation des nouvelles fonctionnalités enfants. Pour plus d’informations, consultez contrôle de la [sélection des fonctionnalités États](controlling-feature-selection-states.md).

Une nouvelle fonctionnalité enfant peut être masquée par l’utilisateur. Pour synchroniser l’état d’installation d’une nouvelle fonctionnalité enfant avec sa fonctionnalité parente, définissez les bits msidbFeatureAttributesFollowParent et msidbFeatureAttributesUIDisallowAbsent pour la fonctionnalité enfant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> <dt>

[Référence de propriété](property-reference.md)
</dt> </dl>

 

 




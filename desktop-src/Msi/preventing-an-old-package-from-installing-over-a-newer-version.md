---
description: Windows Installer les packages de mise à niveau peuvent être créés pour que les mises à niveau majeures ne soient pas installées si une version plus récente est déjà installée sur un utilisateur.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Empêcher l’installation d’un ancien package sur une version plus récente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519865"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Empêcher l’installation d’un ancien package sur une version plus récente

Windows Installer les packages de mise à niveau peuvent être créés pour que les mises à niveau majeures ne soient pas installées si une version plus récente est déjà installée sur un utilisateur. La procédure décrite dans cette rubrique peut uniquement empêcher les rétrogradations qui peuvent être provoquées par l’exécution d’un package de mise à niveau majeur. Cette procédure s’appuie sur l' [action FindRelatedProducts](findrelatedproducts-action.md), qui s’exécute uniquement lors d’une première installation et qui ne s’exécute pas en mode maintenance (réinstallation). Étant donné que les mises à niveau mineures sont effectuées à l’aide de la réinstallation, cette procédure ne peut pas être utilisée pour déterminer si un package de mise à niveau mineure tente de rétrograder une application. Pour plus d’informations, consultez [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md).

**Pour empêcher l’installation d’un ancien package sur une version plus récente**

1.  Entrez la propriété [**UpgradeCode**](upgradecode.md) du groupe de produits connexes pouvant être éligibles pour recevoir cette mise à niveau dans la colonne UpgradeCode de la [table de mise à niveau](upgrade-table.md).
2.  Entrez l’indicateur de bit **msidbUpgradeAttributesOnlyDetect** dans la colonne attributs de la [table de mise à niveau](upgrade-table.md).
3.  Entrez la version de la mise à niveau fournie par ce package dans la colonne VersionMin de la [table de mise à niveau](upgrade-table.md). Laissez la colonne VersionMax vide.
4.  Entrez le nom de la propriété qui doit être définie par l' [action FindRelatedProducts](findrelatedproducts-action.md) dans la colonne ActionProperty de la [table de mise à niveau](upgrade-table.md).
5.  Ajoutez la propriété [**SecureCustomProperties**](securecustomproperties.md) et la propriété nommée dans la colonne ActionProperty de la [table de mise à niveau](upgrade-table.md) à la [table de propriétés](property-table.md).
6.  Ajoutez un [type d’action personnalisé 19](custom-action-type-19.md) après l’action FindRelatedProducts dans la [table InstallExecuteSequence](installexecutesequence-table.md). Incluez un enregistrement dans la [table CustomAction](customaction-table.md) pour cette action et entrez le texte à afficher dans la colonne cible. L’action personnalisée de type 19 étant intégrée au programme d’installation, il n’y a aucun code à écrire.
7.  Entrez le nom du ActionProperty dans la colonne condition de l’enregistrement dans la [table InstallExecuteSequence](installexecutesequence-table.md) qui contient le [type d’action personnalisé 19](custom-action-type-19.md). Cette condition permet d’exécuter l’action personnalisée uniquement lorsque la [table de mise à niveau](upgrade-table.md) détecte qu’une version plus récente est déjà installée.

    Par exemple, un package Windows Installer qui met à niveau un groupe de produits associés vers la version 3,0 peut inclure les enregistrements suivants dans ses tables de [mise à niveau](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)et [propriété](property-table.md) . Tous les produits associés au groupe ont le même UpgradeCode, mais le programme d’installation n’installe pas ce package de mise à niveau si une version ultérieure à la version 3,0 est déjà installée sur l’ordinateur. Dans ce cas, le programme d’installation affiche un message d’erreur et l’installation échoue. Le package de mise à niveau de la version 3,0 s’installe sur les versions 1,0 et 2,0.

    [Mettre à niveau la table](upgrade-table.md)

    

    | UpgradeCode                            | VersionMin | VersionMax | Language | Attributs                                | Supprimer | ActionProperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

    [Table CustomAction](customaction-table.md)

    

    | Action | Type | Source | Cible                                 |
    |--------|------|--------|----------------------------------------|
    | AC1    | 19   |        | Une mise à niveau plus élevée est déjà installée. |

    

     

    [Table InstallExecuteSequence](installexecutesequence-table.md)

    

    | Action              | Condition       | Séquence |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | AC1                 | NEWPRODUCTFOUND | 201      |

    

     

    [Table de propriétés](property-table.md)

    

    | Propriété                                                 | Valeur                        |
    |----------------------------------------------------------|------------------------------|
    | [**SecureCustomProperties**](securecustomproperties.md) | NEWPRODUCTFOUND; UPGRADEFOUND |

    

     

 

 




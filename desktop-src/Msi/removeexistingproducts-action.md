---
description: L’action RemoveExistingProducts passe par les codes de produit figurant dans la colonne ActionProperty de la table de mise à niveau et supprime les produits en séquence en appelant des installations simultanées.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Action RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543115"
---
# <a name="removeexistingproducts-action"></a>Action RemoveExistingProducts

L’action RemoveExistingProducts passe par les codes de produit figurant dans la colonne ActionProperty de la [table de mise à niveau](upgrade-table.md) et supprime les produits en séquence en appelant des installations simultanées. Pour chaque installation simultanée, le programme d’installation définit la propriété [**ProductCode**](productcode.md) sur le code du produit et définit la propriété [**Remove**](remove.md) sur la valeur du champ Remove de la table Upgrade. Si le champ supprimer est vide, sa valeur par défaut est tous et le programme d’installation supprime l’intégralité du produit.

Le programme d’installation exécute uniquement l’action RemoveExistingProducts la première fois qu’il installe un produit. Elle n’exécute pas l’action pendant une [installation](maintenance-installation.md) ou une désinstallation de maintenance.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RemoveExistingProducts doit être planifiée dans la séquence d’action à l’un des emplacements suivants.

-   Entre l' [action InstallValidate](installvalidate-action.md) et l' [action InstallInitialize](installinitialize-action.md). Dans ce cas, le programme d’installation supprime les anciennes applications entièrement avant d’installer les nouvelles applications. Il s’agit d’un emplacement inefficace pour l’action, car tous les fichiers réutilisés doivent être recopiés.
-   Après l' [action InstallInitialize](installinitialize-action.md) et avant toute action qui génère le script d’exécution.
-   Entre l’action [InstallExecute](installexecute-action.md), l’action [InstallExecuteAgain](installexecuteagain-action.md)et l' [action InstallFinalize](installfinalize-action.md). En général, les trois dernières actions sont planifiées juste après l’autre : InstallExecute, RemoveExistingProducts et InstallFinalize. Dans ce cas, les fichiers mis à jour sont installés en premier, puis les anciens fichiers sont supprimés. Toutefois, si la suppression de l’ancienne application échoue, le programme d’installation annule la suppression de l’ancienne application et l’installation de la nouvelle application.
-   Après l' [action InstallFinalize](installfinalize-action.md). Il s’agit du positionnement le plus efficace pour l’action. Dans ce cas, le programme d’installation met à jour les fichiers avant de supprimer les anciennes applications. Seuls les fichiers en cours de mise à jour sont installés pendant l’installation. Si la suppression de l’ancienne application échoue, le programme d’installation annule uniquement la désinstallation de l’ancienne application.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action |
|-------|----------------------------|
| \[1\] | Produit supprimé.           |



 

## <a name="remarks"></a>Notes

Windows Installer définit la propriété [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) lors de l’exécution de cette action.

 

 




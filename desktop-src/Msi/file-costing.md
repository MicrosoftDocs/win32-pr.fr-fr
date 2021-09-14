---
description: L’évaluation des coûts est le processus qui consiste à déterminer l’espace disque total requis pour une installation.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Coût des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a4e6221775c2b9ecc429bd32f136e519a2b63b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021753"
---
# <a name="file-costing"></a>Coût des fichiers

L’évaluation des coûts est le processus qui consiste à déterminer l’espace disque total requis pour une installation. Les éléments calculés dans le processus de coût des fichiers incluent la quantité d’espace disque dans laquelle les fichiers sont installés ou supprimés, ainsi que la quantité d’espace disque occupée par les entrées de Registre, les raccourcis et d’autres fichiers divers. Les fichiers existants planifiés pour être remplacés sont également calculés dans les totaux de coût du disque.

Les coûts totaux sont accumulés pour chaque[composant](components-and-features.md) et se composent de trois parties distinctes : les coûts locaux, les coûts de source et les coûts de suppression. Ces éléments correspondent au coût du disque qui est encouru si le composant est installé localement, installé pour s’exécuter à partir du média source ou supprimé.

Tous les calculs impliquant le coût d’installation des fichiers dépendent du volume de disque sur lequel le fichier doit être installé ou supprimé. Chaque fois que le répertoire associé à un composant change, les coûts des fichiers d’installation contrôlés par ce composant doivent être recalculés. Par exemple, étant donné qu’une modification de répertoire peut également impliquer une modification de volume, les tailles de fichiers en cluster doivent être recalculées. En outre, le nouveau répertoire doit être vérifié pour déterminer si des fichiers existants pouvant être remplacés doivent être pris en compte.

Une fois l’action [CostInitialize](costinitialize-action.md) appelée, l’action [FileCost](filecost-action.md) doit être appelée. L’action CostInitialize initialise les routines internes du programme d’installation qui calculent dynamiquement les coûts de disque associés aux actions d’installation standard. Aucun autre calcul de coût dynamique n’est effectué à ce stade.

Ensuite, l’action [CostFinalize](costfinalize-action.md) doit être appelée. Cette action permet de finaliser tous les calculs de coûts et de rendre disponibles les données de coût dans la table des [composants](component-table.md) .

Une fois l’exécution de l’action [CostFinalize](costfinalize-action.md) terminée, la table des [composants](component-table.md) est entièrement initialisée et une séquence de la boîte de dialogue de l’interface utilisateur contenant un contrôle [SelectionTree](selectiontree-control.md) peut être lancée si nécessaire. Les boîtes de dialogue de l’interface utilisateur peuvent offrir la possibilité de modifier l’état de sélection ou le répertoire de destination des fonctionnalités de la table de [fonctionnalités](feature-table.md) pour l’utilisateur. Le processus est similaire lorsque l’état de sélection d’un composant change ; Toutefois, dans ce cas, le coût dynamique du composant modifié est uniquement recalculé.

Une fois que l’utilisateur a terminé de sélectionner des fonctionnalités dans l’interface utilisateur, l’action [InstallValidate](installvalidate-action.md) doit être appelée. Cette action permet de vérifier que tous les volumes auxquels le coût a été attribué disposent d’un espace suffisant pour l’installation.

 

 




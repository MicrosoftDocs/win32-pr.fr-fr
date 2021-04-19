---
description: Les administrateurs peuvent contrôler la quantité de données que chaque utilisateur peut stocker sur un volume de système de fichiers NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Gestion des quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534101"
---
# <a name="managing-disk-quotas"></a>Gestion des quotas de disque

Le système de fichiers NTFS prend en charge les *quotas de disque*, ce qui permet aux administrateurs de contrôler la quantité de données que chaque utilisateur peut stocker sur un volume de système de fichiers NTFS. Les administrateurs peuvent éventuellement configurer le système pour qu’il journalise un événement lorsque les utilisateurs sont proches de leur quota et pour refuser de l’espace disque aux utilisateurs qui dépassent leur quota. Les administrateurs peuvent également générer des rapports et utiliser l’observateur d’événements pour suivre les problèmes de quota.

Vous pouvez déterminer si un système de fichiers prend en charge les quotas de disque en appelant la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et en examinant l’indicateur de bit **quotas de \_ volume \_ de fichier** .

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                   | Description                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Administration au niveau de l’utilisateur des quotas de disque](user-level-administration-of-disk-quotas.md)<br/>     | Comment obtenir davantage d’espace disque disponible après avoir dépassé le quota alloué.<br/>                                                                  |
| [Administration au niveau du système des quotas de disque](system-level-administration-of-disk-quotas.md)<br/> | L’administrateur système peut définir des quotas pour des utilisateurs spécifiques sur un volume. L’administrateur peut également définir des quotas par défaut pour le volume.<br/> |
| [Limites de quota de disque](disk-quota-limits.md)<br/>                                                   | Décrit deux types de limites de quota de disque et la mesure des limites de quota de disque.<br/>                                                      |
| [Interfaces de quota de disque](disk-quota-interfaces.md)<br/>                                           | Interfaces utilisées avec les quotas de disque.<br/>                                                                                                     |



 

 

 





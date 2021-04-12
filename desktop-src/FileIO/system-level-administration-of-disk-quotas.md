---
description: L’administrateur système peut définir des quotas pour des utilisateurs spécifiques sur un volume. L’administrateur peut également définir des quotas par défaut pour le volume.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Administration au niveau du système des quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201604"
---
# <a name="system-level-administration-of-disk-quotas"></a>Administration au niveau du système des quotas de disque

L’administrateur système peut définir des quotas pour des utilisateurs spécifiques sur un volume. L’administrateur peut également définir des quotas par défaut pour le volume. Un nouvel utilisateur sur le volume reçoit le quota par défaut, sauf si l’administrateur a établi un quota spécifique pour cet utilisateur.

L’administrateur peut interroger le niveau de suivi et d’application du quota (ou les États de quota), les limites de quota par défaut et les informations de quota par utilisateur. Les informations de quota par utilisateur contiennent la limite de quota matériel de l’utilisateur, le seuil d’avertissement et l’utilisation du quota. L’administrateur peut également activer ou désactiver l’application des quotas.

Il existe trois États de quota, comme indiqué dans le tableau suivant.



| State          | Description                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quota désactivé | Les modifications de l’utilisation du quota ne sont pas suivies, mais les limites de quota ne sont pas supprimées. Dans cet État, les performances ne sont pas affectées par les quotas de disque. Il s’agit de la valeur par défaut.                         |
| Quota suivi  | Les modifications de l’utilisation du quota sont suivies, mais les limites de quota ne sont pas appliquées. Dans cet État, aucun événement de violation de quota n’est généré et aucune opération de fichier ne réussit en raison de violations de quota de disque. |
| Quota appliqué | Les modifications de l’utilisation du quota sont suivies et les limites de quota sont appliquées.                                                                                                                           |



 

 

 




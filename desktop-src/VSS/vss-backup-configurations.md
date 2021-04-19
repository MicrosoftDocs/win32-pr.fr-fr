---
description: Il existe un certain nombre de types de sauvegardes pris en charge de façon conventionnelle&\# 8212 ; Incremental, Differential et full&\# 8212 ; que VSS reconnaît, ainsi qu’une configuration de sauvegarde propre à VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurations de sauvegarde VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514618"
---
# <a name="vss-backup-configurations"></a>Configurations de sauvegarde VSS

Il existe un certain nombre de types de sauvegardes pris en charge de façon conventionnelle (incrémentielle, différentielle et complète) dont VSS est conscient, ainsi qu’une configuration de sauvegarde propre à VSS.

Lors de la définition d’une configuration de sauvegarde, un demandeur et les rédacteurs sur un système indiquent comment les données seront écrites sur un dispositif de stockage, comment le mécanisme de cliché instantané sera déployé et quelles informations doivent être enregistrées. L’interaction entre les enregistreurs et les demandeurs est déterminée par le type de sauvegarde qu’un demandeur souhaite exécuter et les genres (ou schémas) que chaque Writer peut prendre en charge :

-   [État de sauvegarde VSS](vss-backup-state.md)
-   [Prise en charge du schéma de sauvegarde de l’enregistreur](writer-backup-schema-support.md)
-   [Prise en charge des schémas au niveau du fichier](file-level-schema-support.md)

 

 




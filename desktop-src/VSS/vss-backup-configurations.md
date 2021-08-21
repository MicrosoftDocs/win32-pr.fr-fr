---
description: Il existe un certain nombre de types de sauvegardes pris en charge de façon conventionnelle&\# 8212 ; Incremental, Differential et full&\# 8212 ; que VSS reconnaît, ainsi qu’une configuration de sauvegarde propre à VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurations de sauvegarde VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8552bc379be4fc2bf7301043355a1a4417a59154ea15c36061b9cfd13c5d209f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056337"
---
# <a name="vss-backup-configurations"></a>Configurations de sauvegarde VSS

Il existe un certain nombre de types de sauvegardes pris en charge de façon conventionnelle (incrémentielle, différentielle et complète) dont VSS est conscient, ainsi qu’une configuration de sauvegarde propre à VSS.

Lors de la définition d’une configuration de sauvegarde, un demandeur et les rédacteurs sur un système indiquent comment les données seront écrites sur un dispositif de stockage, comment le mécanisme de cliché instantané sera déployé et quelles informations doivent être enregistrées. L’interaction entre les enregistreurs et les demandeurs est déterminée par le type de sauvegarde qu’un demandeur souhaite exécuter et les genres (ou schémas) que chaque Writer peut prendre en charge :

-   [État de sauvegarde VSS](vss-backup-state.md)
-   [Prise en charge du schéma de sauvegarde de l’enregistreur](writer-backup-schema-support.md)
-   [Prise en charge des schémas au niveau du fichier](file-level-schema-support.md)

 

 




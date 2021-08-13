---
description: la propriété MSIFASTINSTALL peut être utilisée pour réduire le temps nécessaire à l’installation d’un package de Windows Installer volumineux.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propriété MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28c731d34e769f0612acc12586349247231bce663036d3577f41df6a7256f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628501"
---
# <a name="msifastinstall-property"></a>Propriété MSIFASTINSTALL

la propriété **MSIFASTINSTALL** peut être utilisée pour réduire le temps nécessaire à l’installation d’un package de Windows Installer volumineux. La propriété peut être définie sur la ligne de commande ou dans la table de [Propriétés](property-table.md) pour configurer les opérations que l’utilisateur ou le développeur détermine sont non essentielles pour l’installation.

La valeur de la propriété **MSIFASTINSTALL** peut être une combinaison des valeurs suivantes.



| Valeur | Signification                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Valeur par défaut                                                                |
| 1     | Aucun point de restauration système n’est enregistré pour cette installation.                      |
| 2     | Effectuez uniquement les [coûts des fichiers](file-costing.md) et ignorez les autres coûts. |
| 4     | Réduisez la fréquence des messages de progression.                                   |



 

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette propriété est disponible à partir de Windows Installer 5,0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



 

 





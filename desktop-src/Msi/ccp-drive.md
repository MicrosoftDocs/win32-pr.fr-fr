---
description: La \_ propriété lecteur CCP est définie sur le chemin d’accès racine du volume amovible dans lequel la recherche doit être effectuée par RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: CCP_DRIVE, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7e96b5c69ecb3b52ae57da5476f4b9408039659f5cf26474cc443072b870de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075139"
---
# <a name="ccp_drive-property"></a>\_Propriété du lecteur CCP

La **propriété \_ lecteur CCP** est définie sur le chemin d’accès racine du volume amovible dans lequel la recherche doit être effectuée par [RMCCPSearch](rmccpsearch-action.md). L’action RMCCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant d’effectuer une installation de mise à niveau.

Cette propriété est généralement définie par l’intermédiaire de l’interface utilisateur ou d’une action personnalisée. Cette propriété doit être définie avant l’exécution de l’action [RMCCPSearch](rmccpsearch-action.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





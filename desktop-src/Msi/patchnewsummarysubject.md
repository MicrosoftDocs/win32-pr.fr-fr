---
description: La propriété PATCHNEWSUMMARYSUBJECT met à jour la propriété Résumé de l’objet d’une image administrative lors de la mise à jour corrective.
ms.assetid: 8aee1905-59a4-4818-b073-4bc401a6963d
title: Propriété PATCHNEWSUMMARYSUBJECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912fe9ea21605625135b385a400fd5136c993c1d0dd0e3bfadd6a2b6699d21e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926165"
---
# <a name="patchnewsummarysubject-property"></a>Propriété PATCHNEWSUMMARYSUBJECT

La propriété **PATCHNEWSUMMARYSUBJECT** met à jour la propriété Résumé de l' [**objet**](subject-summary.md) d’une image administrative lors de la mise à jour corrective. Cette propriété est définie uniquement par une transformation dans un fichier. msp. Le fichier. msp doit inclure une transformation qui ajoute cette propriété à la [table de propriétés](property-table.md) et définit sa valeur. Le programme d’installation écrit ensuite la valeur de **PATCHNEWSUMMARYSUBJECT** dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) .

## <a name="remarks"></a>Remarques

Les propriétés [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)et **PATCHNEWSUMMARYSUBJECT** sont utilisées pour mettre à jour les informations de résumé lorsqu’un correctif est installé sur une image administrative.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





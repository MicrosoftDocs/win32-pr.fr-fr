---
description: La propriété PATCHNEWPACKAGECODE met à jour la propriété Résumé du numéro de révision d’une image administrative lors de la mise à jour corrective.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propriété PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d7e64729643fa1b6449838496416d10e1ec12374762b3f702b306a146338f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926161"
---
# <a name="patchnewpackagecode-property"></a>Propriété PATCHNEWPACKAGECODE

La propriété **PATCHNEWPACKAGECODE** met à jour la propriété [**Résumé du numéro de révision**](revision-number-summary.md) d’une image administrative lors de la mise à jour corrective. Cette propriété est définie uniquement par une transformation dans un fichier. msp. Le fichier. msp doit inclure une transformation qui ajoute cette propriété à la [table de propriétés](property-table.md) et définit sa valeur. Le programme d’installation écrit ensuite la valeur de **PATCHNEWPACKAGECODE** dans la propriété **Résumé du numéro de révision** .

## <a name="remarks"></a>Remarques

Les propriétés **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)et [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) sont utilisées pour mettre à jour les informations de résumé lorsqu’un correctif est installé sur une image administrative.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





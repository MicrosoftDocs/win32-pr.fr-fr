---
description: La propriété PATCHNEWSUMMARYCOMMENTS met à jour la propriété Résumé des commentaires d’une installation d’administration pendant la mise à jour corrective.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Propriété PATCHNEWSUMMARYCOMMENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef7a67b960b41e55caf5251a33ac6d3198147b92bcab895a2ca711af330acd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074779"
---
# <a name="patchnewsummarycomments-property"></a>Propriété PATCHNEWSUMMARYCOMMENTS

La propriété **PATCHNEWSUMMARYCOMMENTS** met à jour la propriété [**Résumé des commentaires**](comments-summary.md) d’une installation d’administration pendant la mise à jour corrective. Cette propriété est définie uniquement par une transformation dans un fichier. msp. Le fichier. msp doit inclure une transformation qui ajoute cette propriété à la [table de propriétés](property-table.md) et définit sa valeur. Le programme d’installation écrit ensuite la valeur de **PATCHNEWSUMMARYCOMMENTS** dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) .

## <a name="remarks"></a>Remarques

Les propriétés [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** et [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) sont utilisées pour mettre à jour les informations de résumé lorsqu’un correctif est installé sur une image administrative.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





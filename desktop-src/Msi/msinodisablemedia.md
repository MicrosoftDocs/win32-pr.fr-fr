---
description: Définissez la propriété MSINODISABLEMEDIA pour empêcher le programme d’installation de définir la propriété DISABLEMEDIA. La définition de la propriété DISABLEMEDIA empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Propriété MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021316"
---
# <a name="msinodisablemedia-property"></a>Propriété MSINODISABLEMEDIA

Définissez la propriété **MSINODISABLEMEDIA** pour empêcher le programme d’installation de définir la propriété [**DISABLEMEDIA**](-disablemedia.md) . La définition de la propriété **DISABLEMEDIA** empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit.

Quand **MSINODISABLEMEDIA** n’est pas défini, le programme d’installation peut ajouter [**DISABLEMEDIA**](-disablemedia.md) au flux de propriétés d’administration lors de l’exécution d’une [installation d’administration](administrative-installation.md). Cela empêche les utilisateurs qui installent à partir de l’image administrative de s’installer à partir d’un support, tel qu’un CD-ROM.

-   Lorsque vous effectuez une installation administrative, le programme d’installation ajoute uniquement [**DISABLEMEDIA**](-disablemedia.md) au flux de propriétés d’administration si la propriété de [**Résumé du nombre de pages**](page-count-summary.md) est inférieure à 150.

Si [**DISABLEMEDIA**](-disablemedia.md) est listé dans la propriété [**AdminProperties**](adminproperties.md) , la définition de **MSINODISABLEMEDIA** empêche la définition de **DISABLEMEDIA** au cours d’une installation d’administration. Dans ce cas, le programme d’installation peut inscrire une source de média et un utilisateur peut alors avoir la possibilité de réinstaller à partir de la source du média si l’image d’installation d’administration d’origine n’est plus disponible.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003, Windows XP et Windows 2000. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





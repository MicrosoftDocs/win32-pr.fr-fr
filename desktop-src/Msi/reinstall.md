---
description: La valeur de la propriété réinstaller est une liste de fonctionnalités délimitée par des virgules qui doivent être réinstallées. Les fonctionnalités indiquées doivent être présentes dans la colonne fonctionnalité du tableau des fonctionnalités. Pour réinstaller toutes les fonctionnalités, utilisez réinstaller = ALL sur la ligne de commande.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: RÉINSTALLER la propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009674"
---
# <a name="reinstall-property"></a>RÉINSTALLER la propriété

La valeur de la propriété **réinstaller** est une liste de fonctionnalités délimitée par des virgules qui doivent être réinstallées. Les fonctionnalités indiquées doivent être présentes dans la colonne fonctionnalité [du tableau des fonctionnalités.](feature-table.md) Pour réinstaller toutes les fonctionnalités, utilisez réinstaller = ALL sur la ligne de commande.

## <a name="remarks"></a>Remarques

Notez que les noms de fonctionnalités respectent la casse.

Si la propriété **réinstaller** est définie, la propriété [**REINSTALLMODE**](reinstallmode.md) doit également être définie pour indiquer le type de réinstallation à effectuer. Si la propriété **REINSTALLMODE** n’est pas définie, par défaut, tous les fichiers qui sont actuellement installés sont réinstallés, si le fichier actuellement installé est une version antérieure (ou n’est pas présent). Par défaut, aucune entrée de Registre n’est réécrite.

Notez que même si la **réinstallation** est définie sur tous, seules les fonctionnalités qui ont déjà été installées précédemment sont réinstallées. Ainsi, si la **réinstallation** est définie pour un produit qui n’est pas encore installé, aucune action d’installation n’aura lieu.

Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Installez**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  **INSTALLÉ**
6.  [**PUBLIÉS**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**FILEADDLOCAL**](fileaddlocal.md)
10. [**FILEADDSOURCE**](fileaddsource.md)
11. [**FILEADDDEFAULT**](fileadddefault.md)

Par exemple, si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source. Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, puis lorsque ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.

Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





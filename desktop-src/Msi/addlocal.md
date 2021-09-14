---
description: La valeur de la propriété ADDLOCAL est une liste de fonctionnalités qui sont délimitées par des virgules et qui doivent être installées localement.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: Propriété ADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092798"
---
# <a name="addlocal-property"></a>Propriété ADDLOCAL

La valeur de la propriété **addlocal** est une liste de fonctionnalités qui sont délimitées par des virgules et qui doivent être installées localement. Les fonctionnalités doivent être présentes dans la colonne Feature de la [table Feature](feature-table.md). Pour installer toutes les fonctionnalités localement, utilisez ADDLOCAL = ALL sur la ligne de commande. N’entrez pas ADDLOCAL = ALL dans la [table de propriétés](property-table.md), car cela génère un package installé localement qui ne peut pas être supprimé correctement.

## <a name="remarks"></a>Notes

Les noms de fonctionnalités respectent la casse. Si l’indicateur de bit SourceOnly est défini dans la colonne attributs de la [table des composants](component-table.md) pour un composant d’une fonctionnalité de la liste, ce composant est installé en tant qu’exécution à partir de la source.

Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :

1.  **ADDLOCAL**
2.  [**Installez**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**INSTALLÉ**](reinstall.md)
6.  [**PUBLIÉS**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Par exemple :

-   Si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = **MyFeature**, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis **MyFeature** est défini sur Run-from-source.
-   Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL =**MyFeature**, First **MyFeature** est défini sur Run-local, puis lorsque addsource = All est évalué, toutes les fonctionnalités (y compris **MyFeature**) sont réinitialisées à l’exécution à partir de la source.

Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue, ou lorsque l’une des propriétés précédentes est spécifiée sur la ligne de commande.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





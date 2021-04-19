---
description: La valeur de la propriété ADDSOURCE est une liste de fonctionnalités qui sont délimitées par des virgules et qui doivent être installées pour s’exécuter à partir de la source.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: Propriété ADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533490"
---
# <a name="addsource-property"></a>Propriété ADDSOURCE

La valeur de la propriété **addsource** est une liste de fonctionnalités qui sont délimitées par des virgules et qui doivent être installées pour s’exécuter à partir de la source. Les fonctionnalités doivent être présentes dans la colonne Feature de la [table Feature](feature-table.md). Pour installer toutes les fonctionnalités en tant qu’exécution à partir de la source, utilisez ADDSOURCE = ALL sur la ligne de commande. N’entrez pas ADDSOURCE = ALL dans la [table de propriétés](property-table.md), car cela génère un package d’exécution à partir de la source qui ne peut pas être supprimé correctement.

## <a name="remarks"></a>Notes

Les noms des fonctionnalités respectent la casse. Si l’indicateur de bit LocalOnly est défini dans la colonne attributs de la [table des composants](component-table.md) pour un composant d’une fonctionnalité de la liste, ce composant est installé pour s’exécuter localement.

Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Installez**](remove.md)
3.  **ADDSOURCE**
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

Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue, ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





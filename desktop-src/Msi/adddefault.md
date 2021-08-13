---
description: La valeur de la propriété ADDDEFAULT est une liste de fonctionnalités délimitée par des virgules, qui doivent être installées dans leur configuration par défaut.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Propriété ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e854df38b58a19f41f98cf1f96657dafdda0c4134c7085c50b4c9c4528b3164e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639703"
---
# <a name="adddefault-property"></a>Propriété ADDDEFAULT

La valeur de la propriété **AddDefault** est une liste de fonctionnalités délimitée par des virgules, qui doivent être installées dans leur configuration par défaut. Les fonctionnalités doivent être présentes dans la colonne Feature de la [table Feature.](feature-table.md) Pour installer toutes les fonctionnalités dans leurs configurations par défaut, utilisez ADDDEFAULT = ALL sur la ligne de commande.

Une fonctionnalité indiquée dans la propriété **AddDefault** est installée dans le même état d’installation que si l’utilisateur a demandé une installation à la demande de la fonctionnalité. L’État est déterminé par les bits définis pour la fonctionnalité dans la colonne attributs de la table de [fonctionnalités](feature-table.md), et les bits définis pour les composants de la fonctionnalité dans la colonne attributs de la [table des composants](component-table.md).

## <a name="remarks"></a>Remarques

Les noms des fonctionnalités respectent la casse.

Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Installez**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**INSTALLÉ**](reinstall.md)
6.  [**PUBLIÉS**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Par exemple :

-   Si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis **MyFeature** est défini sur Run-from-source.
-   Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First **MyFeature** est défini sur Run-local, puis lorsque addsource = All est évalué, toutes les fonctionnalités (y compris **MyFeature**) sont réinitialisées à l’exécution à partir de la source.

Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue, ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





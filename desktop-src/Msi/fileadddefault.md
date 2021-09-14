---
description: La valeur de la propriété FILEADDDEFAULT est une liste de clés de fichier délimitée par des virgules qui sont installées dans leur configuration par défaut.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: Propriété FILEADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021742"
---
# <a name="fileadddefault-property"></a>Propriété FILEADDDEFAULT

La valeur de la propriété **FILEADDDEFAULT** est une liste de clés de fichier délimitée par des virgules qui sont installées dans leur configuration par défaut. Pour chaque clé de fichier de la liste, le programme d’installation détermine le composant qui contrôle ce fichier et installe la fonctionnalité qui nécessite le moins d’espace disque. Les clés de fichier de la liste doivent être présentes dans la colonne fichier de la table [file](file-table.md) . Une fonctionnalité est installée dans le même état d’installation que si l’utilisateur avait demandé une installation à la demande de la fonctionnalité. L’État est déterminé par les bits définis pour la fonctionnalité dans la colonne attributs de la [table de fonctionnalités](feature-table.md), et par les bits définis pour les composants de la fonctionnalité dans la colonne attributs de la [table des composants](component-table.md).

## <a name="remarks"></a>Notes

Notez que les noms de clé de fichier respectent la casse. Notez également que si l’indicateur de bit SourceOnly est défini dans la colonne attributs de la table des [composants](component-table.md) pour un composant, le composant est installé pour s’exécuter à partir de la source.

Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant.

1.  [**ADDLOCAL**](addlocal.md)
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
12. **FILEADDDEFAULT**

Par exemple, si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source. Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, puis lorsque ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.

Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 





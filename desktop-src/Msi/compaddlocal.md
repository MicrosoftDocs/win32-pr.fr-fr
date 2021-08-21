---
description: La valeur de la propriété COMPADDLOCAL est une liste de GUID de composant à partir de la colonne ComponentId de la table de composants, délimitée par des virgules, qui doivent être installées localement.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: Propriété COMPADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c442ede6e8affaaddef1dc028a8a6fffc5b780afd536bbc3eaa52e6949df8fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145142"
---
# <a name="compaddlocal-property"></a>Propriété COMPADDLOCAL

La valeur de la propriété **COMPADDLOCAL** est une liste de GUID de composant à partir de la colonne ComponentID de la [table de composants](component-table.md), délimitée par des virgules, qui doivent être installées localement. Le programme d’installation utilise cette liste pour déterminer les fonctionnalités qui sont configurées pour être installées localement, en fonction des composants spécifiés. Pour chaque ID de composant listé, le programme d’installation examine toutes les fonctionnalités liées à ce composant par le biais de la table [FeatureComponents](featurecomponents-table.md) et installe la fonctionnalité qui nécessite le moins d’espace disque à installer. Les composants listés doivent être présents dans la colonne composant de la table des [composants](component-table.md) .

## <a name="remarks"></a>Remarques

Notez que les noms des composants respectent la casse. Notez également que si l’indicateur de bit SourceOnly est défini dans la colonne attributs de la table des [composants](component-table.md) pour un composant, le composant est installé pour s’exécuter à partir de la source.

Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Installez**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**INSTALLÉ**](reinstall.md)
6.  [**PUBLIÉS**](advertise.md)
7.  **COMPADDLOCAL**
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

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

 

 





---
description: Certaines formules nécessitent à la fois une propriété de compteur et une propriété de base.
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: Types de compteurs de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518925"
---
# <a name="base-counter-types"></a>Types de compteurs de base

Certaines formules nécessitent à la fois une propriété de compteur et une propriété de base. La valeur de base est le dénominateur dans la formule pour le type de compteur. Dans les [classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) de données brutes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), la propriété de base doit suivre immédiatement la propriété Counter. La propriété de base doit avoir le même nom que le compteur précédent, avec la **\_ base** ajoutée.

Par exemple, la propriété **AvgDiskBytesPerRead** dans le disque [**\_ logique Win32 PerfRawData \_ Perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md) contient la valeur brute, en octets, transférée à partir du disque pendant les opérations de lecture. Elle possède une propriété de base, **AvgDiskBytesPerRead \_ base**, qui représente le nombre cumulé d’opérations. Lorsque WMI applique la formule pour le type de compteur spécifié, la base de la **\_ moyenne \_ des performances**, **AvgDiskBytesPerRead** est divisée par **AvgDiskBytesPerRead \_ base** pour produire la valeur moyenne. Cette valeur apparaît dans le moniteur système et est stockée dans la propriété de [**\_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) correspondante. Les propriétés de base sont utilisées uniquement dans les classes de données brutes.

Dans les classes dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), le qualificateur de **compteur** spécifie la propriété numérateur dans la classe brute et le qualificateur de **base** spécifie la propriété de dénominateur de base.

Le tableau suivant répertorie les valeurs **de constantes** .



| @, Constante                                                                                      | Description                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Performances \_ MOYENNE de \_ base](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimale 1073939458<br/>        | Valeur de base utilisée pour calculer **le \_ \_ minuteur de performances moyenne** et les types de compteurs **\_ \_ en bloc de performance moyenne** .                                                                                             |
| [Performances \_ COMPTEUR-nombre décimal à \_ \_ BASE multiple](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1107494144<br/> | Valeur de base utilisée pour calculer **le \_ compteur de performance multi- \_ \_ Timer**, **compteur de performance \_ \_ \_ \_** multi-Timer, **perf \_ 100NSEC \_ multi- \_ Timer** et **perf \_ 100NSEC \_ plusieurs \_ minuteurs \_ INV** . |
| [Performances \_ GRANDE décimale \_ brute de \_ base](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939712<br/>     | Valeur de base trouvée dans le calcul de la **\_ \_ fraction brute de perf**, 64 bits.                                                                                                                         |
| [Performances \_ Décimale de \_ base brute](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939459<br/>            | Valeur de base utilisée pour calculer le type de compteur de **\_ \_ fractions brutes perf** .                                                                                                                           |
| [Performances \_ EXEMPLE de \_ base](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimale 1073939457<br/>         | Valeur de base utilisée pour calculer **l' \_ exemple \_** de compteur de performance et les types de compteurs de **\_ \_ fractions** de l’échantillon de performance.                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Types de compteurs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))
</dt> </dl>

 


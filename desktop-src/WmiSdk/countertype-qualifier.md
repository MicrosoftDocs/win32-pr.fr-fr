---
description: Le qualificateur abPerfRawData contient la valeur entière pour le type de compteur de la propriété pour les propriétés des \_ classes Win32. CookingType contient les constantes pour les types de formule de propriété dans les \_ classes PerfFormattedData Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Qualificateur de l’identificateur de la
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120458"
---
# <a name="countertype-qualifier"></a>Qualificateur de l’identificateur de la

Le **qualificateur abPerfRawData contient la valeur** entière pour le type de compteur de la propriété pour les propriétés des classes [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . **CookingType** contient les constantes pour les types de formule de propriété dans les classes [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Pour plus d’informations et une répartition des types de compteurs par fonction, consultez [types de compteurs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).



| CounterType | CookingType                              |
|-------------|------------------------------------------|
| 0           | compteur de performances \_ \_ RAWCOUNT \_ Hex             |
| 256         | compteur de performances \_ \_ grand \_ RAWCOUNT \_ Hex hex      |
| 2816        | \_texte du compteur de performances \_                      |
| 65536       | compteur de performances \_ \_ RAWCOUNT                  |
| 65792       | compteur de performances- \_ \_ grand \_ RAWCOUNT           |
| 73728       | PERF \_ double \_ brut                        |
| 4195328     | \_delta du compteur de performances \_                     |
| 4195584     | compteur de performances- \_ \_ \_ Delta important              |
| 4260864     | \_compteur d’exemples perf \_                    |
| 4523008     | \_type de \_ QUEUELEN du compteur de performances \_            |
| 4523264     | TYPE de QUEUELEN de compteur de performances \_ \_ élevé \_ \_     |
| 5571840     | TYPE de QUEUELEN de compteur de performances \_ \_ 100 NS \_ \_     |
| 6620416     | TYPE de QUEUELEN du compteur de performance \_ \_ obj \_ Time \_ \_ |
| 272696320   | \_compteur de compteur de performances \_                   |
| 272696576   | nombre de compteurs de performances \_ \_ en bloc \_               |
| 537003008   | FRACTION de performances \_ brutes \_                      |
| 541132032   | \_minuteur de compteur de performances \_                     |
| 541525248   | \_ \_ minuteur système de précision de performance \_           |
| 542180608   | \_ \_ Minuteur 100NSEC perf                     |
| 542573824   | \_ \_ Minuteur de 100 précision de performance \_            |
| 543229184   | \_ \_ minuteur de temps obj de perf \_                   |
| 543622400   | \_ \_ minuteur d’objet de précision de performance \_           |
| 549585920   | FRACTION de l' \_ exemple perf \_                   |
| 557909248   | \_ \_ inventaire du compteur de performances \_                |
| 558957824   | PERF \_ 100NSEC \_ minuteur \_ inv                |
| 574686464   | compteur de performances \_ \_ multiple \_ Timer              |
| 575735040   | \_ \_ \_ MINUTEur 100NSEC perf              |
| 591463680   | compteur de performances ( \_ \_ plusieurs \_ minuteurs) \_ inv         |
| 592512256   | PERF \_ 100NSEC \_ multi- \_ Timer \_         |
| 805438464   | \_minuteur de performance moyen \_                     |
| 807666944   | \_temps écoulé de \_ performance                      |
| 1073742336  | compteur de performances \_ \_ NoData                    |
| 1073874176  | moyenne de performances \_ \_ en bloc                      |
| 1073939457  | \_exemple de \_ base de performances                       |
| 1073939458  | \_base moyenne de performances \_                      |
| 1073939459  | \_base brute de perf. \_                          |
| 1073939712  | \_horodatage de précision de performance \_               |
| 1073939715  | BASE de performances \_ volumineuse \_ brute \_                   |
| 1107494144  | compteur de performances \_ \_ multi- \_ base               |
| 2147483648  | \_type d' \_ histogramme du compteur de performances \_           |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Qualificateurs spécifiques aux classes de performance WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 


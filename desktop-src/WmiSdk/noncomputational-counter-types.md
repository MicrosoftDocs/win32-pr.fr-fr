---
description: Les types de compteurs non calculés n’ont pas de formule associée. La valeur brute est directement explicite.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Types de compteurs décalculés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203735"
---
# <a name="noncomputational-counter-types"></a>Types de compteurs décalculés

Les types de compteurs non calculés n’ont pas de formule associée. La valeur brute est directement explicite.

La propriété **FilesToBeIndexed** de la [**classe \_ \_ \_ IndexingService Win32 PerfRawData ContentIndex**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) est un exemple du type de compteur de **performance \_ \_ RAWCOUNT du compteur de performances** . Il contient le nombre de fichiers qui n’ont pas été indexés.

Les types de compteurs sont désignés par la constante définie dans Winperf. h situé dans le kit de développement logiciel (SDK) Microsoft Windows. Le tableau suivant répertorie les types de compteurs décalculés qui sont fournis.



| CounterType                                                                                                 | Description                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Performances \_ \_Texte du compteur](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 2816<br/>                | Ce type de compteur affiche une chaîne de texte de longueur variable en Unicode. Elle n’affiche pas les valeurs calculées.               |
| [Performances \_ COMPTEUR \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 65536<br/>           | Valeur de compteur brute qui ne nécessite pas de calculs, et représente un échantillon qui est la dernière valeur observée uniquement. |
| [Performances \_ COUNTER \_ \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | Identique au **compteur de performances \_ \_ RAWCOUNT**, mais une représentation 64 bits pour les valeurs plus élevées.                                    |
| [Performances \_ COMPTEUR \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Valeur la plus récemment observée au format hexadécimal. Il n'affiche pas une moyenne.                                    |
| [Performances \_ COUNTER \_ grand \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 256<br/> | Identique au **compteur de performances \_ \_ RAWCOUNT \_ Hex**, mais une représentation 64 bits au format hexadécimal pour une utilisation avec des valeurs élevées.        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> </dl>

 


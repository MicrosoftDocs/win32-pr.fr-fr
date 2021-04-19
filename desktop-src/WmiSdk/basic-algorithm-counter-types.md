---
description: Représentent les différences entre les échantillons au fil du temps et utilisent souvent une valeur de base pour le calcul.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Types de compteurs de l’algorithme de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524391"
---
# <a name="basic-algorithm-counter-types"></a>Types de compteurs de l’algorithme de base

Les types de compteurs de l’algorithme de base représentent généralement les différences entre les exemples au fil du temps, et utilisent souvent une valeur de base pour le calcul. Par exemple, la propriété **PercentFreeSpace** de la classe [**Win32 \_ PerfFormattedData \_ Perfdisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) représente le rapport entre l’espace libre disponible sur l’unité de disque physique et l’espace total utilisable fourni par le lecteur de disque physique sélectionné. Cette classe contient également la valeur de base, **PercentFreeSpace \_ base**. Le pourcentage d’espace disque disponible est obtenu en divisant **PercentFreeSpace** par **PercentFreeSpace \_ base** et en multipliant par 100%.

Les algorithmes de base dans le tableau suivant sont fournis.



| @, Constante                                                                                    | Description                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Performances \_ \_Fraction brute](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimale 537003008<br/>       | Rapport entre un sous-ensemble et son ensemble sous forme de pourcentage. Ce type de compteur affiche le pourcentage actuel uniquement, et non une moyenne dans le temps.                                    |
| [Performances \_ EXEMPLE de \_ fraction](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimale 549585920<br/>    | Taux moyen d’accès à toutes les opérations au cours des deux derniers intervalles d’échantillonnage. Ce type de compteur requiert une propriété de base avec \_ le \_ type de compteur de base Sample perf. |
| [Performances \_ COMPTEUR \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 4195328<br/>        | Ce type de compteur affiche la modification de l'attribut mesuré entre les deux derniers intervalles échantillons.                                                         |
| [Performances \_ COUNTER nombre décimal \_ \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195584<br/> | Identique au Delta de compteur de performances, \_ \_ mais une représentation 64 bits pour les valeurs plus élevées.                                                                                        |
| [Performances \_ \_Temps écoulé](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 807666944<br/>       | Durée totale entre le démarrage du processus et l’heure à laquelle cette valeur est calculée.                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> </dl>

 


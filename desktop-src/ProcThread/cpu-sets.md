---
description: Les ensembles d’UC fournissent des API pour déclarer l’affinité de l’application selon un mode « soft » qui est compatible avec la gestion de l’alimentation du système d’exploitation.
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: Ensembles d’UC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801474591751f04a5bffe570d6b8caff4974203f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518253"
---
# <a name="cpu-sets"></a>Ensembles d’UC

Les ensembles d’UC fournissent des API pour déclarer l’affinité de l’application selon un mode « soft » qui est compatible avec la gestion de l’alimentation du système d’exploitation. En outre, l’API fournit aux applications la possibilité de reaffinitize tous les threads d’arrière-plan du processus à un sous-ensemble de processeurs à l’aide du mécanisme de **processus par défaut** afin d’éviter les interférences entre les threads du système d’exploitation au sein du processus. Certaines versions de Windows prennent en charge les stratégies de réservation principales, dans lesquelles un sous-ensemble des ensembles d’UC du système peut être consacré à l’utilisation exclusive des applications et charges de travail individuelles.

L’API d’ensemble d’UC fonctionne avec des ID de jeu de PROCESSEURs, qui sont associés à des affinités de processeur virtuel. Sur la plupart des systèmes, et dans la plupart des cas, chaque ID de jeu d’UC est mappé directement à un seul processeur logique d' **hébergement** . Un thread affinité à un ensemble d’UC donné s’exécute généralement sur l’un des processeurs de sa liste d’ID de jeux d’UC sélectionnés.

Les ensembles d’UC réservés peuvent être déterminés en inspectant l’indicateur **alloué** dans les \_ informations du jeu d’UC système \_ \_ . Le système contrôle l’accès aux jeux d’UC réservés et l’assignation peut être interrogée à l’aide de l’indicateur **AllocatedToTargetProcess** de la \_ structure d’informations du jeu d’UC système \_ \_ . Si un processus tente d’utiliser une attribution de jeu d’UC qui est allouée exclusivement à d’autres processus, sa demande est ignorée et les threads affectés à des ensembles d’UC non autorisés sont planifiés ailleurs. Les ensembles d’UC peuvent être affectés à deux niveaux. Les ensembles d’UC par défaut du processus sont affectés à tous les threads d’un processus qui n’ont pas d’attribution au niveau du thread sélectionné. Si un thread ou un processus possède un masque d’affinité restrictif défini, le masque d’affinité est respecté au-dessus de toute affectation de jeu d’UC conflictuel. Sur les systèmes à plusieurs groupes, les affectations d’UC sont ignorées si elles se trouvent dans des groupes qui ne correspondent pas au groupe dans le masque d’affinité du thread. Si un thread est affecté à plusieurs ensembles d’UC valides, il s’exécutera sur l’un des processeurs correspondants en fonction de ses priorités et des priorités des threads concurrents sur ces processeurs.

**Fonctions/énumérations/structures de l’ensemble d’UC**

-   [**GetProcessDefaultCpuSets**](getprocessdefaultcpusets.md) fonction)
-   [**GetSystemCpuSetInformation**](getsystemcpusetinformation.md) fonction)
-   [**GetThreadSelectedCpuSets**](getthreadselectedcpusets.md) fonction)
-   [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md) fonction)
-   [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) fonction)
-   [**Processeur \_ DÉFINIR \_ \_**](cpu-set-information-type.md) l’énumération des types d’informations
-   [**Système \_ Structure \_ des \_ informations du jeu de processeurs**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 




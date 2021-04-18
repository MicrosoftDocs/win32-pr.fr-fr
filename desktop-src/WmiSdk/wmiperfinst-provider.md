---
description: À compter de Windows Vista, le fournisseur WmiPerfInst fournit des données de compteur de performances brutes et mises en forme de manière dynamique aux classes de compteur de performances WMI dérivées de la \_ performance Win32.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Fournisseur WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519036"
---
# <a name="wmiperfinst-provider"></a>Fournisseur WmiPerfInst

À compter de Windows Vista, le fournisseur WmiPerfInst fournit des données de compteur de performances brutes et mises en forme de manière dynamique aux [classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI dérivées de la [**\_ performance Win32**](/windows/desktop/CIMWin32Prov/win32-perf). Ce fournisseur remplace le [fournisseur de données de performance mis en forme](formatted-performance-data-provider.md), également appelé « fournisseur de compteurs cuit », et le [fournisseur de compteur de performance](performance-counter-provider.md).

Le fournisseur WmiPerfInst fournit des données aux classes WMI fournies par le fournisseur [wmiperfclass](wmiperfclass-provider.md) . Ce fournisseur est un pont entre les instances de l’application d’assistance des données de performance (PDH) et les classes de performance WMI fournies par le fournisseur WmiPerfClass. Quand WmiPerfInst reçoit une requête de données, il charge la classe et utilise les [qualificateurs](qualifiers-specific-to-wmi-performance-classes.md) de la classe et de la propriété pour localiser les instances PDH. Pour plus d’informations, consultez [utilisation des fonctions PDH pour consommer des données de compteur](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

Il n’est pas recommandé de développer de nouveaux objets de performance en créant un fournisseur haute performance WMI et en fonction du processus de l' [*adaptateur inverse adap*](gloss-r.md) pour transférer les données vers les bibliothèques de performances. La seule exception est lorsque vous développez un pilote Windows Driver Model et que vous souhaitez fournir des données de performances. Tandis que le processus de l’adaptateur inverse continue de fonctionner pour des raisons de compatibilité descendante, la méthode recommandée consiste à utiliser les [compteurs de performance Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Le nom d’instance [**\_ \_ Win32Provider**](--win32provider.md) de ce fournisseur est « WmiPerfInst ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> <dt>

[Bibliothèques de performances et WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

 

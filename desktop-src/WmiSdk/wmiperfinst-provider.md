---
description: depuis Windows Vista, le fournisseur WmiPerfInst fournit des données de compteur de performances brutes et mises en forme de manière dynamique aux Classes de compteur de performances WMI dérivées de la \_ performance Win32.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Fournisseur WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a781fc1dc48f0e16d1c25e03eff1b2ab3c80fcd7058d1b49f95912b392d241
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049747"
---
# <a name="wmiperfinst-provider"></a>Fournisseur WmiPerfInst

depuis Windows Vista, le fournisseur WmiPerfInst fournit des données de compteur de performances brutes et mises en forme de manière dynamique aux [Classes de compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI dérivées de la [**\_ performance Win32**](/windows/desktop/CIMWin32Prov/win32-perf). ce fournisseur remplace le [Fournisseur de données de performance mis en forme](formatted-performance-data-provider.md), également appelé « fournisseur de compteurs cuit », et le [fournisseur de compteur de performance](performance-counter-provider.md).

Le fournisseur WmiPerfInst fournit des données aux classes WMI fournies par le fournisseur [wmiperfclass](wmiperfclass-provider.md) . Ce fournisseur est un pont entre les instances de l’application d’assistance des données de performance (PDH) et les classes de performance WMI fournies par le fournisseur WmiPerfClass. Quand WmiPerfInst reçoit une requête de données, il charge la classe et utilise les [qualificateurs](qualifiers-specific-to-wmi-performance-classes.md) de la classe et de la propriété pour localiser les instances PDH. Pour plus d’informations, consultez [utilisation des fonctions PDH pour consommer des données de compteur](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

Il n’est pas recommandé de développer de nouveaux objets de performance en créant un fournisseur haute performance WMI et en fonction du processus de l' [*adaptateur inverse adap*](gloss-r.md) pour transférer les données vers les bibliothèques de performances. la seule exception est lorsque vous développez un pilote Windows Driver Model et que vous souhaitez fournir des données de performances. Tandis que le processus de l’adaptateur inverse continue de fonctionner pour des raisons de compatibilité descendante, la méthode recommandée consiste à utiliser les [compteurs de performance Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Le nom d’instance [**\_ \_ Win32Provider**](--win32provider.md) de ce fournisseur est « WmiPerfInst ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> <dt>

[Bibliothèques de performances et WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

 

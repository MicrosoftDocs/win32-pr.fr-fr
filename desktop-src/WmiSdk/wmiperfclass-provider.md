---
description: À compter de Windows Vista, ce fournisseur crée les classes de compteur de performance WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Fournisseur WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034614"
---
# <a name="wmiperfclass-provider"></a>Fournisseur WmiPerfClass

À compter de Windows Vista, ce fournisseur crée les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI. Les données sont fournies dynamiquement par le fournisseur [wmiperfinst](wmiperfinst-provider.md) à ces classes de performance WMI. Le processus AutoDiscovery/AutoPurge (ADAP) ne transfère plus les objets de compteur de performance dans les classes de performance WMI de l’espace de stockage WMI. Pour plus d’informations, consultez [bibliothèques de performances et WMI](performance-libraries-and-wmi.md).

Pour plus d’informations, consultez [bibliothèques de performances et WMI](performance-libraries-and-wmi.md).

Bien qu’il ne soit pas recommandé de développer de nouveaux objets de performance en créant un fournisseur de haute performance WMI et de dépendre du processus d' [*adaptateur inverse adap*](gloss-r.md) pour transférer les données vers les bibliothèques de performances, l’exception est le développement d’un pilote Windows Driver Model qui fournit des données de performances. Tandis que le processus de l’adaptateur inverse continue de fonctionner pour des raisons de compatibilité descendante, la méthode recommandée consiste à utiliser les [compteurs de performance Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Le nom d’instance [**\_ \_ Win32Provider**](--win32provider.md) de ce fournisseur est « WmiPerfClass ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> <dt>

[Bibliothèques de performances et WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

 

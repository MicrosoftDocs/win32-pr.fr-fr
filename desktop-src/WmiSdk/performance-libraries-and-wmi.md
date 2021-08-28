---
description: Le fournisseur WMIPerfClass et le fournisseur WMIPerfInst fournissent dynamiquement des données de compteurs de performances pour les classes de compteur de performance WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliothèques de performances et WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877623bcf27dffe71146df4f9c117da83941bd1d8e2ed46436a04c1d7ace95df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996409"
---
# <a name="performance-libraries-and-wmi"></a>Bibliothèques de performances et WMI

Le fournisseur [wmiperfclass](wmiperfclass-provider.md) et le [fournisseur WMIPerfInst](wmiperfinst-provider.md) fournissent dynamiquement des données de compteurs de performances pour les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Fournisseurs WMIPerfClass et WMIPerfInst

Le [fournisseur wmiperfclass](wmiperfclass-provider.md) crée des [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI au moment de l’initialisation du système. Le [fournisseur WMIPerfInst](wmiperfinst-provider.md) fournit dynamiquement des données de compteurs de performance pour ces classes. Le fournisseur WMIPerfClass fournit des classes pour les [compteurs de performance](/windows/desktop/PerfCtrs/performance-counters-portal)version 1 et version 2.

Les compteurs de la version 1 se trouvent dans le Registre sous **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services**. Les services qui fournissent des données de performances ont une sous-clé de **performance** . Les classes de performance WMI créées à partir des compteurs de la version 1 n’ont pas de « compteurs » dans leur nom.

le **GUID** identifiant un fournisseur de compteurs de performance version 2 se trouve dans le registre sous **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

WMIPerfClass est inscrit en tant que fournisseur de classe WMI normal. WMIPerfInst est un fournisseur d’instances WMI qui fournit des données de performance Data Helper (PDH) pour les compteurs version 1 et version 2. Pour plus d’informations, consultez [utilisation des fonctions PDH pour consommer des données de compteur](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

 

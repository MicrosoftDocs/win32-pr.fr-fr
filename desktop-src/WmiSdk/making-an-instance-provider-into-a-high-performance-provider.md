---
description: L’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Création d’un fournisseur d’instances dans un fournisseur de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524249"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Création d’un fournisseur d’instances dans un fournisseur de High-Performance

L’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée. À compter de Windows Vista, les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI ne sont plus migrées dans les bibliothèques de performances Windows par l’adaptateur inverse AutoDiscovery/AutoPurge (ADAP). Pour créer un fournisseur de compteurs de performance, utilisez les [compteurs de performance Version 2,0](/windows/desktop/PerfCtrs/performance-counters-portal). Une fois les objets de bibliothèque de performances créés, le [fournisseur wmiperfclass](wmiperfclass-provider.md) analyse les objets et crée ou actualise une classe WMI dérivée de la [**\_ performance Win32**](/windows/desktop/CIMWin32Prov/win32-perf) pour chaque objet de performance. Le [fournisseur WMIPerfInst](wmiperfinst-provider.md) fournit ensuite dynamiquement des données de compteur de performances brutes et mises en forme aux classes de performance WMI.

La procédure de haut niveau suivante fournit les étapes nécessaires à la création d’un fournisseur à hautes performances.

**Pour créer un fournisseur à hautes performances**

1.  Inscrivez votre fournisseur auprès de WMI. Pour plus d’informations, consultez [inscription d’un fournisseur de High-Performance](registering-a-high-performance-provider.md).
2.  Implémentez votre fournisseur. Pour plus d’informations, consultez [écriture d’un fournisseur d’instances](writing-an-instance-provider.md).
3.  Implémentez l’interface hautes performances. Pour plus d’informations, consultez [implémentation de l’Interface High-Performance](implementing-the-high-performance-interface.md).
4.  Dérivez et écrivez votre schéma format MOF (MOF) pour obtenir des données de performances brutes. Pour plus d’informations, consultez [prise en charge de la \_ classe Win32 PerfRawData](supporting-the-win32-perfrawdata-class.md).
5.  Dérivez et écrivez votre schéma MOF pour obtenir des données précalculées. En prenant en charge cette classe, le fournisseur n’est pas obligé d’effectuer les calculs. Ces données sont les mêmes que celles du moniteur système dans Perfmon. Pour plus d’informations, consultez [prise en charge de la \_ classe Win32 PerfFormattedData](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Bibliothèques de performances et WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 

---
description: Les classes de compteur de performance permettent aux scripts et aux programmes d’accéder aux données de performances système calculées par les fournisseurs de haute performance existants.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classes du compteur de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006975"
---
# <a name="performance-counter-classes"></a>Classes du compteur de performances

Les classes de compteur de performance permettent aux scripts et aux programmes d’accéder aux données de performances système calculées par les fournisseurs de haute performance existants. Ces classes se composent de classes de compteur de performances brutes et de classes de compteurs de performance mises en forme.

Différents fournisseurs fournissent des données de bibliothèque de performances via WMI. Les fournisseurs [wmiperfclass](/windows/desktop/WmiSdk/wmiperfclass-provider) et [wmiperfinst](/windows/desktop/WmiSdk/wmiperfinst-provider) fournissent des classes pour les [compteurs de performance](/windows/desktop/PerfCtrs/performance-counters-portal)version 1 et version 2. Ces fournisseurs maintiennent la compatibilité avec les classes disponibles dans les systèmes d’exploitation antérieurs.

Les classes de cette section sont les classes de base abstraites utilisées pour créer des classes de compteur de performance. Il ne s’agit pas d’une liste complète des classes que vous pouvez trouver sur votre système d’exploitation. Pour plus d’informations, consultez [bibliothèques de performances et WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**\_Performances Win32**](win32-perf.md)
</dt> <dd>

Classe de base pour les classes de compteur de performance [**Win32 \_ PerfRawData**](win32-perfrawdata.md) et [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

</dd> <dt>

[**\_PerfFormattedData Win32**](win32-perfformatteddata.md)
</dt> <dd>

classe de base abstraite pour les classes de données calculées préinstallées.

</dd> <dt>

[**\_PerfRawData Win32**](win32-perfrawdata.md)
</dt> <dd>

Classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes Win32](win32-provider.md)
</dt> </dl>

 

 

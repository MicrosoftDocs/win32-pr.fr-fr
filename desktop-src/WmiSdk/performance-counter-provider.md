---
description: Le fournisseur de compteur de performance est un fournisseur à hautes performances qui fournit des données de compteur de performances brutes aux classes de compteur de performance WMI dérivées de Win32 \_ PerfRawData. Le nom de l' \_ \_ instance Win32Provider est &\# 0034 ; NT5 \_ GenericPerfProvider \_ V1&\# 0034 ;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Fournisseur de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9288da5ac20bff6340950ba2a3506d9128200cfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035201"
---
# <a name="performance-counter-provider"></a>Fournisseur de compteurs de performances

\[Le fournisseur du compteur de performance n’est plus disponible. Au lieu de cela, utilisez le fournisseur [wmiperfinst](wmiperfinst-provider.md) .\]

Le fournisseur de compteur de performance est un fournisseur à hautes performances qui fournit des données de compteur de performances brutes aux [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). Le nom de l’instance [**\_ \_ Win32Provider**](--win32provider.md) est « NT5 \_ GenericPerfProvider \_ v1 ».

Les classes [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) se trouvent dans l’espace de noms WMI « root \\ cimv2 ». Chaque classe de performance WMI correspond à un objet de performance dans une bibliothèque de performances. Les propriétés de ces classes représentent les compteurs de l’objet. Le nom de classe WMI d’un objet compteur brut se présente sous la forme **Win32 \_ PerfRawData \_ \_* service \_ name *\_* \_ Name * * *. Par exemple, le nom de classe WMI qui contient les compteurs de disque logique est [**Win32 \_ PerfRawData \_ Perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).

Vous pouvez utiliser la classe [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) correspondante pour récupérer les données de performances précalculées affichées dans le [*Moniteur système*](gloss-s.md). Par exemple, utilisez la classe disque [**\_ \_ \_ logique Win32 PerfFormattedData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) pour obtenir des données de disque précalculées.

Pour plus d’informations sur l’écriture d’un client qui peut accéder aux données de performances brutes, consultez [accès aux données de performances en C++](accessing-performance-data-in-c--.md).

En tant que fournisseur à hautes performances, le fournisseur de compteurs de performance implémente l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que la méthode [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) et les méthodes [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) suivantes :

-   [**CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> </dl>

 

 

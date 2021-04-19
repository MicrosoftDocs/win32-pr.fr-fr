---
description: Fournitures calculées (&\# 0034 ;&cuit \# 0034 ;) données du compteur de performances. Fournit des données dynamiques aux classes WMI dérivées de Win32 \_ PerfFormattedData. Également connu sous le nom de fournisseur de compteurs cuit.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Fournisseur de données de performance mis en forme
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0db075ebdafcd31c7aa0980d191ed565873f686f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524149"
---
# <a name="formatted-performance-data-provider"></a>Fournisseur de données de performance mis en forme

\[Le Fournisseur de données de performance mis en forme, également connu sous le nom de « fournisseur de compteurs cuit », ne peut plus être utilisé. Au lieu de cela, utilisez le fournisseur [wmiperfinst](wmiperfinst-provider.md) .\]

Le fournisseur de données de performances mis en forme hautes performances fournit des données de compteur de performances (« cuites ») calculées, telles que le pourcentage de temps passé par un disque à écrire des données. Ce fournisseur fournit des données dynamiques aux classes WMI dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). La différence entre ce fournisseur et le [fournisseur de compteur de performance](performance-counter-provider.md) est que le fournisseur de compteurs de performance fournit des données brutes et que le fournisseur de compteurs cuit fournit des données de performances qui s’affichent exactement comme dans le [*Moniteur système*](gloss-s.md). Le nom de l’instance [**\_ \_ Win32Provider**](--win32provider.md) est « HiPerfCooker \_ v1 ».

Le nom de classe au format WMI pour un objet de compteur se présente sous la forme « Win32 \_ PerfFormattedData \_ *service \_ Name* \_ *\_ Name*». Par exemple, le nom de classe WMI qui contient les compteurs de disque logique est **Win32 \_ PerfFormattedData \_ Perfdisk \_ LogicalDisk**. Ces classes se trouvent dans l’espace de \\ noms « root cimv2 ».

Étant donné que les classes de données de performances sont ajoutées et modifiées dynamiquement sur un système donné, il n’est pas possible de documenter formellement les propriétés de tous les objets de performance connus. Pour déterminer les classes à votre disposition et pour identifier les membres de ces classes, consultez [récupération de la documentation sur les objets de données de performances brutes et mises en forme](retrieving-raw-and-formatted-performance-data.md).

Les [**classes \_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) utilisent le qualificateur **CookingType** dans les [types de compteurs de performance WMI](wmi-performance-counter-types.md) pour spécifier la formule pour le calcul des données de performances. Ce qualificateur est le même que **le qualificateur de l’identificateur** de classe dans les classes [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .

En tant que fournisseur de haute performance, le fournisseur de compteur cuit implémente l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que la méthode [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) et les méthodes [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) suivantes :

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

 

 

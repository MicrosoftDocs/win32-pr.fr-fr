---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952981"
---
# <a name="p-wmi"></a>P (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [e](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**compteur de performances**
</dt> <dd>

Propriété d’une classe de performance dérivée de [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) qui stocke les données de performances.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**objet de performance**
</dt> <dd>

Objet dans une bibliothèque de performances qui stocke des données dans des compteurs. Ces objets sont visibles dans l’utilitaire [*Moniteur système*](gloss-s.md) . Les exemples sont les objets de cache et de disque logique. Lorsqu’ils sont transférés dans WMI par le processus [*adap*](gloss-a.md) , chaque objet devient deux classes de performance WMI. Une classe, contenant des données brutes, dérive de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). L’autre classe dérive de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) et contient les mêmes données visibles dans le moniteur système que celles calculées par le fournisseur de compteur cuit.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consommateur permanent**
</dt> <dd>

[*Consommateur d’événements*](gloss-e.md) dont l’inscription dure jusqu’à ce qu’elle soit explicitement annulée. Voir aussi [*consommateur temporaire*](gloss-t.md).

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consommateur physique**
</dt> <dd>

Objet COM implémenté par un [*fournisseur de consommateur d’événements*](gloss-e.md) qui comprend un [*récepteur*](gloss-s.md) pour recevoir des notifications d’événements.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**propriété**
</dt> <dd>

Une paire nom/valeur qui décrit une unité de données pour une classe. Les valeurs de propriété doivent avoir un type de données [*format MOF (MOF)*](gloss-m.md) valide. Consultez également la [*propriété Reference*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**fournisseur de propriétés**
</dt> <dd>

Serveur COM qui prend en charge la récupération et la modification des propriétés WMI. Les fournisseurs de propriétés implémentent les interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**moteur**
</dt> <dd>

Serveur COM qui communique avec des objets gérés pour accéder aux données et aux notifications d’événements, telles que le registre ou un périphérique SNMP. Les fournisseurs transfèrent ces données au [*Gestionnaire d’objets CIMOM*](gloss-c.md) pour l’intégration et l’interprétation.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**méthode du fournisseur**
</dt> <dd>

Méthode implémentée par un *fournisseur* WMI.

</dd> </dl>

 

 

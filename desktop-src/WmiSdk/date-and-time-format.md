---
description: Décrit le format de date et d’heure Common Information Model (CIM) utilisé par WMI. Ce format est indépendant des paramètres régionaux, de sorte que les scripts utilisant DATETIME peuvent s’exécuter dans de nombreux fuseaux horaires.
ms.assetid: be239bf8-88a3-47bc-ae4f-49a5195e7a7d
ms.tgt_platform: multiple
title: Format de date et d’heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e8f97930efa33942fe87b2109aa7cd7ba9d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115043"
---
# <a name="date-and-time-format"></a>Format de date et d’heure

WMI utilise les formats de date et d’heure définis par la spécification[DMTF.org](https://www.dmtf.org/)(Distributed Management Task Force) Common Information Model (CIM).

Le **format \_ DateTime CIM** est implémenté dans Microsoft [format MOF (MOF)](managed-object-format--mof-.md) par le type de données MOF [DateTime](datetime.md) . Les formats de date et d’heure peuvent également exprimer un intervalle de temps.

Pour plus d’informations sur les formats WMI, voir [format d’intervalle](interval-format.md)et [ \_ DateTime CIM](cim-datetime.md) .

Pour plus d’informations sur la conversion vers et à partir du format DATETIME WMI, consultez [**SWbemDateTime**](swbemdatetime.md) et l’article sur technet scriptcenter [il s’agit du temps (Oh, et à propos des dates)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> </dl>

 

 




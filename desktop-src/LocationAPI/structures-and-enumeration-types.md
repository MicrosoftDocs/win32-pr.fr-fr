---
description: L’API d’emplacement définit les types d’énumération suivants.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Structures et types énumération (API location)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8cfea31e8822147cc33710239b31dcd4b982ca3b523dfb6f118d1969af703c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129809"
---
# <a name="structures-and-enumeration-types-location-api"></a>Structures et types énumération (API location)

\[L’API emplacement Win32 peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) . \]

L’API d’emplacement définit les types d’énumération suivants.



| Énumération                                                                       | Description                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**précision de l’emplacement \_ souhaitée \_**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))                  | Définit les types de précision souhaités possibles.                         |
| [**\_État du rapport d’emplacement \_**](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | Définit l’état possible des nouveaux rapports d’un type de rapport particulier. |



 

## <a name="location-constants-from-the-sensor-api"></a>Constantes d’emplacement à partir de l’API de capteur

L’API de capteur définit également des constantes et des clés de propriétés liées à l’emplacement. Les clés de propriété définies dans sensors. h peuvent être utilisées pour récupérer des données d’emplacement à partir d’un rapport en appelant [**ILocationReport :: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).

 

 

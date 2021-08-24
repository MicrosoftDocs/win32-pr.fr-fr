---
title: Énumération DODownloadCostPolicy
description: Spécifie l’ID des options de stratégie de coût associées à la propriété **DODownloadProperty_CostPolicy** .
keywords:
- Énumération DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 763042ed6d0df6fa287fbe66d23528a199a73041cb3500c6a2812e6db86cb698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677879"
---
# <a name="dodownloadcostpolicy-enumeration"></a>Énumération DODownloadCostPolicy

L’énumération **DODownloadCostPolicy** spécifie l’ID des options de stratégie de coût associées à la propriété **DODownloadProperty_CostPolicy** .

## <a name="syntax"></a>Syntaxe

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a>Constantes

| Condition requise | Valeur |
|-|-|
| DODownloadCostPolicy_Always | Les exécutions sont téléchargées quel que soit le coût. |
| DODownloadCostPolicy_Unrestricted | Le téléchargement s’effectue à moins que n’impose des coûts ou des limites de trafic. |
| DODownloadCostPolicy_Standard | Le téléchargement s’effectue à moins qu’il ne soit soumis à une surcharge ou à une épuisement. |
| DODownloadCostPolicy_NoRoaming | Le téléchargement s’exécute à moins que cette connectivité soit sujette à des surcharges d’itinérance. |
| DODownloadCostPolicy_NoSurcharge | Le téléchargement s’effectue à moins qu’il ne soit soumis à une surcharge. |
| DODownloadCostPolicy_NoCellular | Le téléchargement s’exécute sauf si le réseau est sur un réseau cellulaire. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DeliveryOptimizationDownloadTypes. h |

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
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517653"
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

## <a name="requirements"></a>Spécifications

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DeliveryOptimizationDownloadTypes. h |

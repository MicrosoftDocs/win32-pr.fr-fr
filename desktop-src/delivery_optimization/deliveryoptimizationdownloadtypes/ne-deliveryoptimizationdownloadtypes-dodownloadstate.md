---
title: Énumération DODownloadState
description: Spécifie l’ID de l’état de téléchargement actuel, qui fait partie de la structure **DO_DOWNLOAD_STATUS** .
keywords:
- Énumération DODownloadState, DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517649"
---
# <a name="dodownloadstate-enumeration"></a>Énumération DODownloadState

L’énumération **DODownloadState** spécifie l’ID de l’état de téléchargement actuel, qui fait partie de la structure **DO_DOWNLOAD_STATUS** .

## <a name="syntax"></a>Syntaxe

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a>Constantes

| Condition requise | Valeur |
|-|-|
| DODownloadState_Created | Le téléchargement de l’objet est créé mais n’a pas encore démarré. |
| DODownloadState_Transferring | Le téléchargement est en cours. |
| DODownloadState_Transferred | Le téléchargement est transféré et peut redémarrer en téléchargeant une autre partie du fichier. |
| DODownloadState_Finalized | Le téléchargement est finalisé et ne peut pas être redémarré. |
| DODownloadState_Aborted | Le téléchargement a été abandonné. |
| DODownloadState_Paused | Le téléchargement a été suspendu à la demande ou en raison d’une erreur temporaire. |

## <a name="requirements"></a>Spécifications

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DeliveryOptimizationDownloadTypes. h |

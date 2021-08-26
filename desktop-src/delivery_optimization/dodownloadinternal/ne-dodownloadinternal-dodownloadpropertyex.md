---
title: Énumération DODownloadPropertyEx
description: Spécifie l’ID des propriétés étendues pour l’opération de téléchargement.
keywords:
- Énumération DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: f5ec26d845fd6df2bfe0e84fffed0979c39e1971244788c9dfe5ddd3a0c0beca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990379"
---
# <a name="dodownloadpropertyex-enumeration"></a>Énumération DODownloadPropertyEx

> [!IMPORTANT]
> L’énumération **DODownloadPropertyEx** est déconseillée. Utilisez plutôt l’énumération [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) avec [IDODownload :: GetProperty](../do/nf-do-idodownload-getproperty.md) et [IDODownload :: SetProperty](../do/nf-do-idodownload-setproperty.md).

L’énumération **DODownloadPropertyEx** spécifie l’ID des propriétés étendues pour l’opération de téléchargement. Cette énumération est utilisée par l’interface **IDODownloadInternal** et une valeur de **type Variant** est utilisée pour obtenir et définir la valeur de la propriété.

## <a name="syntax"></a>Syntaxe

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a>Constantes

| Condition requise | Valeur |
|-|-|
| DODownloadPropertyEx_UpdateId | Réservé. Ne pas utiliser. |
| DODownloadPropertyEx_CorrelationVector | Facultatif. Définit un vecteur de corrélation spécifique à des fins de télémétrie. Le type VARIANT est VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Réservé. Ne pas utiliser. |
| DODownloadPropertyEx_IntegrityCheckInfo | Facultatif en écriture seule. Définit l’emplacement du fichier de hachage de l’élément (PHF), utilisé par pour effectuer des vérifications de l’intégrité du Runtime sur le contenu téléchargé. Le type VARIANT est VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Facultatif. Définit un indicateur booléen indiquant si l’utilisation du fichier de hachage de la pièce (PHF) est obligatoire. Si VARIANT_TRUE, le téléchargement est abandonné une fois la vérification d’intégrité en échec. Le type VARIANT est VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Réservé. Ne pas utiliser. |
| DODownloadPropertyEx_TempLocalFileUsage | Réservé. Ne pas utiliser. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DODownloadInternal. h |

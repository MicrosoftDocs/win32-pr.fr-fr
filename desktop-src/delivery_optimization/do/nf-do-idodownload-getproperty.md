---
title: 'IDODownload :: GetProperty, méthode'
description: Récupère un pointeur vers un **Variant** qui contient une propriété de téléchargement spécifique.
keywords:
- 'IDODownload :: GetProperty, méthode'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841733"
---
# <a name="idodownloadgetproperty-method"></a>IDODownload :: GetProperty, méthode

Récupère un pointeur vers un **Variant** qui contient une propriété de téléchargement spécifique.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Paramètres

`propId`

ID de propriété requis pour la récupération (de type **DODownloadProperty**).

`propVal`

Valeur de la propriété résultante, stockée dans un **Variant**.

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

|Valeur retournée|Description|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propid* est inconnu.|
|DO_E_WRITE_ONLY_PROPERTY|La propriété est en écriture seule et ne peut pas être lue.|
|E_NOT_SET|Aucune propriété de ce type n’a été définie via **SetProperty**.|

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |

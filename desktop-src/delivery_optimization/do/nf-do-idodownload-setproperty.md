---
title: 'IDODownload :: SetProperty, méthode'
description: Définit une propriété de téléchargement.
keywords:
- 'IDODownload :: SetProperty, méthode'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7d966edb083107b80f0723bce195bfc588797efb8ad1931e0e75a468bec5a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543898"
---
# <a name="idodownloadsetproperty-method"></a>IDODownload :: SetProperty, méthode

Définit une propriété de téléchargement. La méthode accepte un pointeur vers un **Variant** qui contient une propriété spécifique à appliquer au téléchargement.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Paramètres

`propId`

ID de propriété requis à définir (de type **DODownloadProperty**).

`propVal`

Valeur de la propriété à définir, stockée dans un **Variant**.

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

|Valeur retournée|Description|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propid* est inconnu.|
|DO_E_INVALID_STATE|Le téléchargement n’est pas actuellement dans un État qui permet de définir des propriétés.|

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |

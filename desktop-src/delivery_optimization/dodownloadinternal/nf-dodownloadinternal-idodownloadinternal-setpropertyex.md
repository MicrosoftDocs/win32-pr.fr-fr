---
title: 'IDODownloadInternal :: SetPropertyEx, méthode'
description: Définit une propriété de téléchargement étendue. La méthode accepte un pointeur vers un **Variant** qui contient une valeur de propriété spécifique à appliquer au téléchargement.
keywords:
- 'IDODownloadInternal :: SetPropertyEx, méthode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: d6156f4309c0eac9d2d250c85f7e9ab365e4a3b1e4072aabec7f6aa7e17c437f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858799"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>IDODownloadInternal :: SetPropertyEx, méthode

> [!IMPORTANT]
> L’interface **IDODownloadInternal** est déconseillée. Utilisez plutôt l’interface [IDODownload](../do/nn-do-idodownload.md) .

Définit une propriété de téléchargement étendue. La méthode accepte un pointeur vers un **Variant** qui contient une valeur de propriété spécifique à appliquer au téléchargement.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Paramètres

`propId`

ID de propriété requis à définir (de type **DODownloadPropertyEx**).

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
| **En-tête** | DODownloadInternal. h |
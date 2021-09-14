---
title: 'IDODownloadInternal :: GetPropertyEx, méthode'
description: Récupère un pointeur vers un **Variant** qui contient une valeur de propriété de téléchargement étendue spécifique.
keywords:
- 'IDODownloadInternal :: GetPropertyEx, méthode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916779"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>IDODownloadInternal :: GetPropertyEx, méthode

> [!IMPORTANT]
> L’interface **IDODownloadInternal** est déconseillée. Utilisez plutôt l’interface [IDODownload](../do/nn-do-idodownload.md) .

Récupère un pointeur vers un **Variant** qui contient une valeur de propriété de téléchargement étendue spécifique.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Paramètres

`propId`

ID de propriété requis pour la récupération (de type **DODownloadPropertyEx**).

`propVal`

Valeur de la propriété résultante, stockée dans un **Variant**.

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

|Valeur de retour|Description|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propid* est inconnu.|
|DO_E_WRITE_ONLY_PROPERTY|La propriété est en écriture seule et ne peut pas être lue.|
|E_NOT_SET|Aucune propriété de ce type n’a été définie via **SetPropertyEx**.|

## <a name="requirements"></a>Spécifications

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DODownloadInternal. h |
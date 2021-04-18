---
title: 'IDOManager :: EnumDownloads, méthode'
description: Récupère un pointeur d’interface vers un objet énumérateur utilisé pour énumérer les téléchargements existants.
keywords:
- 'IDOManager :: EnumDownloads, méthode'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106512291"
---
# <a name="idomanagerenumdownloads-method"></a>IDOManager :: EnumDownloads, méthode

Récupère un pointeur d’interface vers un objet énumérateur utilisé pour énumérer les téléchargements existants.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Paramètres

`category`

Facultatif. Nom de la propriété à utiliser comme catégorie à énumérer. La réussite `nullptr` permet de récupérer tous les téléchargements existants. Les propriétés suivantes sont prises en charge en tant que catégorie.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

Adresse d’un pointeur d’interface vers **IEnumUnknown**, qui est utilisé pour énumérer les téléchargements existants. Le contenu de l’énumérateur dépend de la valeur de *Category*. Les téléchargements inclus dans l’interface d’énumération sont ceux qui ont été précédemment créés par le même appelant à cette fonction. 

## <a name="return-value"></a>Valeur renvoyée

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](/windows/desktop/com/structure-of-com-error-codes) [code d’erreur](/windows/desktop/com/com-error-codes-10)HRESULT.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |

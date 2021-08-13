---
title: Structure DO_DOWNLOAD_ENUM_CATEGORY
description: 'Utilisé par **IDOManager :: EnumDownloads** pour filtrer l’énumération downloads par la valeur de la propriété spécifique.'
keywords:
- Structure DO_DOWNLOAD_ENUM_CATEGORY
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 32bdc7ca9a84bfe87ff453d34c4ecff57a8dabf5f67b21cc0d54ba079efd1578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543756"
---
# <a name="do_download_enum_category-structure"></a>Structure DO_DOWNLOAD_ENUM_CATEGORY

La structure **DO_DOWNLOAD_ENUM_CATEGORY** est utilisée par **IDOManager :: EnumDownloads** pour filtrer l’énumération downloads selon la valeur de la propriété spécifique.

## <a name="syntax"></a>Syntaxe
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a>Membres

`Property`

Nom de la propriété à utiliser pour l’énumération de téléchargement. Ces propriétés sont prises en charge à des fins d’énumération.
- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`Value`

Valeur de la propriété.

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ Applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Serveur, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | Do. h |

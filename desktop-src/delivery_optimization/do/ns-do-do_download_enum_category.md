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
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518901"
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

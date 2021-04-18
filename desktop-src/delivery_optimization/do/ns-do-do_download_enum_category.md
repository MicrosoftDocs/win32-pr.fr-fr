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
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "106509421"
---
# <a name="do_download_enum_category-structure"></a><span data-ttu-id="40781-104">Structure DO_DOWNLOAD_ENUM_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="40781-104">DO_DOWNLOAD_ENUM_CATEGORY structure</span></span>

<span data-ttu-id="40781-105">La structure **DO_DOWNLOAD_ENUM_CATEGORY** est utilisée par **IDOManager :: EnumDownloads** pour filtrer l’énumération downloads selon la valeur de la propriété spécifique.</span><span class="sxs-lookup"><span data-stu-id="40781-105">The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.</span></span>

## <a name="syntax"></a><span data-ttu-id="40781-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40781-106">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a><span data-ttu-id="40781-107">Membres</span><span class="sxs-lookup"><span data-stu-id="40781-107">Members</span></span>

`Property`

<span data-ttu-id="40781-108">Nom de la propriété à utiliser pour l’énumération de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="40781-108">The property name to be used for the download enumeration.</span></span> <span data-ttu-id="40781-109">Ces propriétés sont prises en charge à des fins d’énumération.</span><span class="sxs-lookup"><span data-stu-id="40781-109">These properties are supported for enumeration purposes.</span></span>
- <span data-ttu-id="40781-110">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="40781-110">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="40781-111">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="40781-111">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="40781-112">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="40781-112">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="40781-113">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="40781-113">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="40781-114">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="40781-114">**DODownloadProperty_LocalPath**</span></span>

`Value`

<span data-ttu-id="40781-115">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="40781-115">The property's value.</span></span>

## <a name="requirements"></a><span data-ttu-id="40781-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40781-116">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="40781-117">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="40781-117">**Minimum supported client**</span></span> | <span data-ttu-id="40781-118">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40781-118">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="40781-119">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="40781-119">**Minimum supported server**</span></span> | <span data-ttu-id="40781-120">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40781-120">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="40781-121">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="40781-121">**Header**</span></span> | <span data-ttu-id="40781-122">Do. h</span><span class="sxs-lookup"><span data-stu-id="40781-122">Do.h</span></span> |

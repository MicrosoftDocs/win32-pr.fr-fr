---
description: Cette API est réservée à un usage interne et ne doit pas être utilisée dans votre code.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: ApiSetQueryApiSetPresence, fonction (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527716"
---
# <a name="apisetqueryapisetpresence-function"></a><span data-ttu-id="7864a-103">ApiSetQueryApiSetPresence fonction)</span><span class="sxs-lookup"><span data-stu-id="7864a-103">ApiSetQueryApiSetPresence function</span></span>

<span data-ttu-id="7864a-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7864a-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7864a-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7864a-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7864a-106">Cette API est réservée à un usage interne et ne doit pas être utilisée dans votre code.</span><span class="sxs-lookup"><span data-stu-id="7864a-106">This API is intended for internal use only and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7864a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7864a-107">Syntax</span></span>


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a><span data-ttu-id="7864a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7864a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7864a-109">*Espace de noms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7864a-109">*Namespace* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7864a-110">*Présent* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7864a-110">*Present* \[out\]</span></span>
<span data-ttu-id="7864a-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7864a-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7864a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7864a-112">Requirements</span></span>



| <span data-ttu-id="7864a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7864a-113">Requirement</span></span> | <span data-ttu-id="7864a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7864a-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7864a-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7864a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7864a-116">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7864a-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="7864a-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7864a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7864a-118">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7864a-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="7864a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7864a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7864a-120"><dt>Apiquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="7864a-120"><dt>Apiquery.h</dt></span></span> </dl>                                                                                                                 |
| <span data-ttu-id="7864a-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7864a-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="7864a-122"><dt>API-MS-Win-Core-apiquery-L1. lib ; </dt> <dt>API-MS-Win-Core-apiquery-L1-1 1/-0. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7864a-122"><dt>Api-ms-win-core-apiquery-l1.lib; </dt> <dt>Api-ms-win-core-apiquery-l1-1-0.lib</dt></span></span> </dl> |
| <span data-ttu-id="7864a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7864a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7864a-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7864a-124"><dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt></span></span> </dl>                                                                                        |



 

 





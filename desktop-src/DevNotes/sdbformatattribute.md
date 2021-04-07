---
description: Convertit les données d’attribut spécifiées au format XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: SdbFormatAttribute fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846901"
---
# <a name="sdbformatattribute-function"></a><span data-ttu-id="6f71e-103">SdbFormatAttribute fonction)</span><span class="sxs-lookup"><span data-stu-id="6f71e-103">SdbFormatAttribute function</span></span>

<span data-ttu-id="6f71e-104">Convertit les données d’attribut spécifiées au format XML.</span><span class="sxs-lookup"><span data-stu-id="6f71e-104">Converts the specified attribute data to XML format.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f71e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f71e-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="6f71e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f71e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f71e-107">*pAttrInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f71e-107">*pAttrInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f71e-108">Structure [**ATTRINFO**](attrinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6f71e-108">An [**ATTRINFO**](attrinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6f71e-109">*pchBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6f71e-109">*pchBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f71e-110">Mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="6f71e-110">The output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6f71e-111">*dwBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f71e-111">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f71e-112">Taille de la mémoire tampon *pchBuffer* , en caractères.</span><span class="sxs-lookup"><span data-stu-id="6f71e-112">The size of the *pchBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f71e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f71e-113">Return value</span></span>

<span data-ttu-id="6f71e-114">La fonction retourne **true** en cas de réussite ou **false** si la mémoire tampon est insuffisante ou si l’attribut est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6f71e-114">The function returns **TRUE** on success or **FALSE** if the buffer is too small or the attribute is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f71e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f71e-115">Requirements</span></span>



| <span data-ttu-id="6f71e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f71e-116">Requirement</span></span> | <span data-ttu-id="6f71e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f71e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f71e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f71e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6f71e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f71e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6f71e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f71e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6f71e-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f71e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f71e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6f71e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f71e-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f71e-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f71e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f71e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f71e-125">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="6f71e-125">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 





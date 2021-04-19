---
description: La fonction RegOpenBlobKey récupère un objet BLOB stocké à la clé de Registre donnée.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: RegOpenBlobKey, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543542"
---
# <a name="regopenblobkey-function"></a><span data-ttu-id="77699-103">RegOpenBlobKey fonction)</span><span class="sxs-lookup"><span data-stu-id="77699-103">RegOpenBlobKey function</span></span>

<span data-ttu-id="77699-104">La fonction **RegOpenBlobKey** récupère un objet BLOB stocké à la clé de Registre donnée.</span><span class="sxs-lookup"><span data-stu-id="77699-104">The **RegOpenBlobKey** function retrieves a BLOB stored at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="77699-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77699-105">Syntax</span></span>


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="77699-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77699-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77699-107">*HKEY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77699-107">*hkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77699-108">Handle de la clé de Registre qui contient l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="77699-108">Handle to the registry key that contains the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="77699-109">*szBlobName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77699-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77699-110">Nom qui identifie l’objet BLOB donné dans le registre.</span><span class="sxs-lookup"><span data-stu-id="77699-110">Name that identifies the given BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="77699-111">*phBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="77699-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77699-112">Pointeur vers l’objet BLOB qui est récupéré.</span><span class="sxs-lookup"><span data-stu-id="77699-112">Pointer to the BLOB that is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77699-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77699-113">Return value</span></span>

<span data-ttu-id="77699-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="77699-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="77699-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="77699-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="77699-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77699-116">Requirements</span></span>



| <span data-ttu-id="77699-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77699-117">Requirement</span></span> | <span data-ttu-id="77699-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="77699-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77699-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77699-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77699-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77699-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77699-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77699-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77699-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77699-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77699-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="77699-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="77699-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="77699-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="77699-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77699-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="77699-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77699-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="77699-127">DLL</span><span class="sxs-lookup"><span data-stu-id="77699-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77699-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77699-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77699-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77699-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77699-130">RegCreateBlobKey</span><span class="sxs-lookup"><span data-stu-id="77699-130">RegCreateBlobKey</span></span>](regcreateblobkey.md)
</dt> </dl>

 

 





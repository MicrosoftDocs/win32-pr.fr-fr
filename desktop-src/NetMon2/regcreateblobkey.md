---
description: La fonction RegCreateBlobKey stocke un objet BLOB à la clé de Registre donnée.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: RegCreateBlobKey, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524722"
---
# <a name="regcreateblobkey-function"></a><span data-ttu-id="ea53c-103">RegCreateBlobKey fonction)</span><span class="sxs-lookup"><span data-stu-id="ea53c-103">RegCreateBlobKey function</span></span>

<span data-ttu-id="ea53c-104">La fonction **RegCreateBlobKey** stocke un objet blob à la clé de Registre donnée.</span><span class="sxs-lookup"><span data-stu-id="ea53c-104">The **RegCreateBlobKey** function stores a BLOB at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea53c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea53c-105">Syntax</span></span>


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="ea53c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea53c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea53c-107">*HKEY* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea53c-107">*hkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea53c-108">Handle de la clé de Registre dans laquelle l’objet BLOB sera stocké.</span><span class="sxs-lookup"><span data-stu-id="ea53c-108">Handle to the registry key where the BLOB will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="ea53c-109">*szBlobName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea53c-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea53c-110">Nom (défini par l’application) qui représente l’objet BLOB dans le registre.</span><span class="sxs-lookup"><span data-stu-id="ea53c-110">Name (application defined) that represents the BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="ea53c-111">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea53c-111">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea53c-112">Handle de l’objet BLOB enregistré.</span><span class="sxs-lookup"><span data-stu-id="ea53c-112">Handle to the BLOB that is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea53c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea53c-113">Return value</span></span>

<span data-ttu-id="ea53c-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ea53c-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ea53c-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ea53c-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea53c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea53c-116">Requirements</span></span>



| <span data-ttu-id="ea53c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea53c-117">Requirement</span></span> | <span data-ttu-id="ea53c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea53c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea53c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea53c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea53c-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea53c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ea53c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea53c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea53c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea53c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ea53c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea53c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea53c-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea53c-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ea53c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea53c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea53c-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea53c-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea53c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ea53c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea53c-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea53c-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea53c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea53c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea53c-130">RegOpenBlobKey</span><span class="sxs-lookup"><span data-stu-id="ea53c-130">RegOpenBlobKey</span></span>](regopenblobkey.md)
</dt> </dl>

 

 





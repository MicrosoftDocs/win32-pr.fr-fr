---
description: La fonction CreateNPPInterface utilise l’objet BLOB retourné par le Finder pour créer un NPP que l’application peut utiliser.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: CreateNPPInterface, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952275"
---
# <a name="createnppinterface-function"></a><span data-ttu-id="4e44c-103">CreateNPPInterface fonction)</span><span class="sxs-lookup"><span data-stu-id="4e44c-103">CreateNPPInterface function</span></span>

<span data-ttu-id="4e44c-104">La fonction **CreateNPPInterface** utilise l’objet BLOB retourné par le Finder pour créer un NPP que l’application peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="4e44c-104">The **CreateNPPInterface** function uses the BLOB returned from the finder to create an NPP that the application can use.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e44c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e44c-105">Syntax</span></span>


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="4e44c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e44c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e44c-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e44c-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e44c-108">Handle vers l’objet BLOB retourné par le Finder.</span><span class="sxs-lookup"><span data-stu-id="4e44c-108">Handle to the BLOB returned from the finder.</span></span>

</dd> <dt>

<span data-ttu-id="4e44c-109">*IID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e44c-109">*iid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e44c-110">Identificateur de l’interface que vous appelez à partir de NPP (**IRTC** ou **IDelaydC**, par exemple).</span><span class="sxs-lookup"><span data-stu-id="4e44c-110">Identifier of the interface that you call from the NPP (**IRTC** or **IDelaydC**, for example).</span></span>

</dd> <dt>

<span data-ttu-id="4e44c-111">*ppvObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4e44c-111">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e44c-112">Pointeur vers le pointeur retourné vers l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="4e44c-112">Pointer to the returned pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e44c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e44c-113">Return value</span></span>

<span data-ttu-id="4e44c-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4e44c-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4e44c-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4e44c-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e44c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e44c-116">Requirements</span></span>



| <span data-ttu-id="4e44c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e44c-117">Requirement</span></span> | <span data-ttu-id="4e44c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e44c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e44c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e44c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e44c-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e44c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4e44c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e44c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e44c-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e44c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e44c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e44c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e44c-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e44c-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="4e44c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e44c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e44c-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e44c-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e44c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4e44c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e44c-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e44c-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 





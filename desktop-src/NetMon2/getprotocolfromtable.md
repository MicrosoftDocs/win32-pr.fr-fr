---
description: La fonction GetProtocolFromTable retourne un handle à un protocole&\# 8212 ; en fonction d’une table de remise et d’une valeur données.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: GetProtocolFromTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950957"
---
# <a name="getprotocolfromtable-function"></a><span data-ttu-id="ff2cf-103">GetProtocolFromTable fonction)</span><span class="sxs-lookup"><span data-stu-id="ff2cf-103">GetProtocolFromTable function</span></span>

<span data-ttu-id="ff2cf-104">La fonction **GetProtocolFromTable** retourne un handle à un protocole basé sur une table de remise et une valeur données.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-104">The **GetProtocolFromTable** function returns a handle to a protocol based on a given handoff table and value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff2cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff2cf-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="ff2cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff2cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff2cf-107">*htable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff2cf-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff2cf-108">Handle vers une table de remise.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-108">Handle to a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="ff2cf-109">*ItemToFind* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff2cf-109">*ItemToFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff2cf-110">Valeur utilisée pour localiser le protocole dans une table de remise.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-110">Value used to locate the protocol in a handoff table.</span></span> <span data-ttu-id="ff2cf-111">La valeur doit être disponible dans les données de protocole.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-111">The value must be available in the protocol data.</span></span>

</dd> <dt>

<span data-ttu-id="ff2cf-112">*lpInstData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ff2cf-112">*lpInstData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff2cf-113">S’il est disponible dans la table de remise, données d’instance pour le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-113">If available in the handoff table, instance data for the next protocol.</span></span> <span data-ttu-id="ff2cf-114">La longueur des données d’instance ne peut pas être supérieure à celle \_ d’un PTR DWORD.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-114">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff2cf-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff2cf-115">Return value</span></span>

<span data-ttu-id="ff2cf-116">Si la fonction réussit, la valeur de retour est un handle de protocole.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-116">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="ff2cf-117">Si la fonction échoue, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff2cf-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ff2cf-118">Remarks</span></span>

<span data-ttu-id="ff2cf-119">Lors de l’implémentation de la fonction d’exportation [RecognizeFrame](recognizeframe.md) , la fonction **GetProtocolFromTable** est utilisée pour obtenir un handle pour le protocole suivant.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-119">When implementing the [RecognizeFrame](recognizeframe.md) export function, the **GetProtocolFromTable** function is used to obtain a handle to the next protocol.</span></span> <span data-ttu-id="ff2cf-120">La fonction **GetProtocolFromTable** est appelée pour récupérer un handle à partir du protocole suivant si le protocole identifie le protocole qui suit.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-120">The **GetProtocolFromTable** function is called to retrieve a handle from the next protocol if the protocol identifies which protocol follows.</span></span>

<span data-ttu-id="ff2cf-121">**Données d’instance**</span><span class="sxs-lookup"><span data-stu-id="ff2cf-121">**Instance data**</span></span>

<span data-ttu-id="ff2cf-122">Les données d’instance peuvent être des données qui sont inférieures ou égales à un \_ ptr DWORD en longueur, ou un pointeur vers des données, telles que des données de trame brutes, qui n’a pas besoin d’être alloué ou libéré par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="ff2cf-122">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff2cf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff2cf-123">Requirements</span></span>



| <span data-ttu-id="ff2cf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff2cf-124">Requirement</span></span> | <span data-ttu-id="ff2cf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff2cf-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff2cf-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff2cf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff2cf-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff2cf-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ff2cf-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff2cf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff2cf-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff2cf-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff2cf-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff2cf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff2cf-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff2cf-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ff2cf-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff2cf-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff2cf-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff2cf-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff2cf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ff2cf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff2cf-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff2cf-135"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff2cf-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff2cf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff2cf-137">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="ff2cf-137">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 





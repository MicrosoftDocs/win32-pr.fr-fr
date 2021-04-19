---
description: La fonction CreatePropertyDatabase crée une base de données de propriétés qui stocke les propriétés d’un protocole.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: CreatePropertyDatabase, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519684"
---
# <a name="createpropertydatabase-function"></a><span data-ttu-id="473c0-103">CreatePropertyDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="473c0-103">CreatePropertyDatabase function</span></span>

<span data-ttu-id="473c0-104">La fonction **CreatePropertyDatabase** crée une base de données de propriétés qui stocke les propriétés d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="473c0-104">The **CreatePropertyDatabase** function creates a property database that stores the properties of a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="473c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="473c0-105">Syntax</span></span>


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a><span data-ttu-id="473c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="473c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="473c0-107">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="473c0-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="473c0-108">Handle du protocole associé à la base de données.</span><span class="sxs-lookup"><span data-stu-id="473c0-108">Handle of the protocol that is associated with the database.</span></span> <span data-ttu-id="473c0-109">Lorsque Moniteur réseau appelle la fonction [Register](register-parser.md) , moniteur réseau transmet le descripteur de protocole à la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="473c0-109">When Network Monitor calls the [Register](register-parser.md) function, Network Monitor passes the protocol handle to the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="473c0-110">*nProperties* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="473c0-110">*nProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="473c0-111">Nombre de propriétés stockées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="473c0-111">Number of properties stored in the database.</span></span> <span data-ttu-id="473c0-112">Définissez ce paramètre sur le nombre de propriétés prises en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="473c0-112">Set this parameter to the number of properties that the protocol supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="473c0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="473c0-113">Return value</span></span>

<span data-ttu-id="473c0-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="473c0-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="473c0-115">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="473c0-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="473c0-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="473c0-116">Return code</span></span>                                                                                             | <span data-ttu-id="473c0-117">Description</span><span class="sxs-lookup"><span data-stu-id="473c0-117">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="473c0-118"><dt>**\_erreur interne \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="473c0-118"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="473c0-119">Une erreur interne s'est produite.</span><span class="sxs-lookup"><span data-stu-id="473c0-119">An internal error has occurred.</span></span><br/>                                     |
| <dl> <span data-ttu-id="473c0-120"><dt>**NMERR \_ non valide \_ HPOTOCOL**</dt></span><span class="sxs-lookup"><span data-stu-id="473c0-120"><dt>**NMERR\_INVALID\_HPOTOCOL**</dt></span></span> </dl> | <span data-ttu-id="473c0-121">Le descripteur du protocole spécifié dans *hProtocol* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="473c0-121">The handle to the protocol specified in *hProtocol* is invalid.</span></span><br/>     |
| <dl> <span data-ttu-id="473c0-122"><dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="473c0-122"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="473c0-123">Moniteur réseau ne dispose pas de suffisamment de mémoire pour créer la base de données.</span><span class="sxs-lookup"><span data-stu-id="473c0-123">Network Monitor does not have enough memory to create the database.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="473c0-124">Notes</span><span class="sxs-lookup"><span data-stu-id="473c0-124">Remarks</span></span>

<span data-ttu-id="473c0-125">La fonction **CreatePropertyDatabase** doit être appelée uniquement lors de l’implémentation de la fonction [Register](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="473c0-125">The **CreatePropertyDatabase** function should be called only when implementing the [Register](register-parser.md) function.</span></span> <span data-ttu-id="473c0-126">L’analyseur utilise **CreatePropertyDatabase** pour créer une base de données de propriétés qui décrit les propriétés d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="473c0-126">The parser uses **CreatePropertyDatabase** to create a property database that describes the properties of a protocol.</span></span> <span data-ttu-id="473c0-127">Moniteur réseau utilise la base de données pour interpréter les informations contenues dans le protocole.</span><span class="sxs-lookup"><span data-stu-id="473c0-127">Network Monitor uses the database to interpret the information within the protocol.</span></span>

<span data-ttu-id="473c0-128">La fonction **CreatePropertyDatabase** alloue les structures dont Moniteur réseau a besoin pour gérer une base de données de propriétés.</span><span class="sxs-lookup"><span data-stu-id="473c0-128">The **CreatePropertyDatabase** function allocates the structures that Network Monitor needs to maintain a property database.</span></span>

## <a name="requirements"></a><span data-ttu-id="473c0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="473c0-129">Requirements</span></span>



| <span data-ttu-id="473c0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="473c0-130">Requirement</span></span> | <span data-ttu-id="473c0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="473c0-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="473c0-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="473c0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="473c0-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="473c0-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="473c0-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="473c0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="473c0-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="473c0-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="473c0-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="473c0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="473c0-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="473c0-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="473c0-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="473c0-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="473c0-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="473c0-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="473c0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="473c0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="473c0-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="473c0-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="473c0-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="473c0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="473c0-143">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="473c0-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 





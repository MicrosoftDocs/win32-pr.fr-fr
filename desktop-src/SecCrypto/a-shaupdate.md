---
description: Ajoute des données à un objet de hachage spécifié.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate, fonction (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525347"
---
# <a name="a_shaupdate-function"></a><span data-ttu-id="5b3a7-103">Une \_ fonction SHAUpdate</span><span class="sxs-lookup"><span data-stu-id="5b3a7-103">A\_SHAUpdate function</span></span>

<span data-ttu-id="5b3a7-104">Ajoute des données à un objet de hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-104">Adds data to a specified hash object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b3a7-105">Syntax</span></span>


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="5b3a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b3a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b3a7-107">*Contexte* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5b3a7-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3a7-108">Contexte SHA.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="5b3a7-109">*Mémoire tampon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5b3a7-109">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3a7-110">Table de hachage.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-110">The hash table.</span></span>

</dd> <dt>

<span data-ttu-id="5b3a7-111">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="5b3a7-111">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="5b3a7-112">Taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-112">The size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b3a7-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5b3a7-113">Return value</span></span>

<span data-ttu-id="5b3a7-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3a7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5b3a7-115">Remarks</span></span>

<span data-ttu-id="5b3a7-116">Cette fonction peut être appelée plusieurs fois pour calculer le hachage sur des flux de données longs ou des flux de données discontinus.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-116">This function can be called multiple times to compute the hash on long data streams or discontinuous data streams.</span></span> <span data-ttu-id="5b3a7-117">La [**fonction \_ SHAFinal**](a-shafinal.md) doit être appelée avant la récupération de la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-117">The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.</span></span>

<span data-ttu-id="5b3a7-118">Cette fonction est très similaire à SHAUpdate, mais elle est appelée directement à partir de la bibliothèque, plutôt que d’être routée via l’infrastructure de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="5b3a7-118">This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="5b3a7-119">Pour plus d’informations, consultez [fournisseurs NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="5b3a7-119">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3a7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b3a7-120">Requirements</span></span>



| <span data-ttu-id="5b3a7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b3a7-121">Requirement</span></span> | <span data-ttu-id="5b3a7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b3a7-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3a7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b3a7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5b3a7-124"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b3a7-124"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="5b3a7-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5b3a7-125">Library</span></span><br/> | <dl> <span data-ttu-id="5b3a7-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b3a7-126"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b3a7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5b3a7-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b3a7-128"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b3a7-128"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 

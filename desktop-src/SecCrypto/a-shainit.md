---
description: Initialise le hachage d’un flux de données.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: A_SHAInit, fonction (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532915"
---
# <a name="a_shainit-function"></a><span data-ttu-id="66373-103">Une \_ fonction SHAInit</span><span class="sxs-lookup"><span data-stu-id="66373-103">A\_SHAInit function</span></span>

<span data-ttu-id="66373-104">Initialise le hachage d’un flux de données.</span><span class="sxs-lookup"><span data-stu-id="66373-104">Initiates the hashing of a stream of data.</span></span>

## <a name="syntax"></a><span data-ttu-id="66373-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66373-105">Syntax</span></span>


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a><span data-ttu-id="66373-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66373-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66373-107">*Contexte* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="66373-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="66373-108">Contexte SHA.</span><span class="sxs-lookup"><span data-stu-id="66373-108">The SHA context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66373-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="66373-109">Return value</span></span>

<span data-ttu-id="66373-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="66373-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66373-111">Notes</span><span class="sxs-lookup"><span data-stu-id="66373-111">Remarks</span></span>

<span data-ttu-id="66373-112">Cette fonction est très similaire à SHAInit, mais elle est appelée directement à partir de la bibliothèque, plutôt que d’être routée via l’infrastructure de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="66373-112">This function is very similar to SHAInit, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="66373-113">Pour plus d’informations, consultez [fournisseurs NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="66373-113">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="66373-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66373-114">Requirements</span></span>



| <span data-ttu-id="66373-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66373-115">Requirement</span></span> | <span data-ttu-id="66373-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="66373-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66373-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="66373-117">Header</span></span><br/>  | <dl> <span data-ttu-id="66373-118"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="66373-118"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="66373-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66373-119">Library</span></span><br/> | <dl> <span data-ttu-id="66373-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66373-120"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="66373-121">DLL</span><span class="sxs-lookup"><span data-stu-id="66373-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="66373-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66373-122"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 

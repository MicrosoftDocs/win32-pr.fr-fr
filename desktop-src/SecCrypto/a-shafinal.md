---
description: Calcule le hachage final des données entrées par la fonction MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: A_SHAFinal, fonction (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543782"
---
# <a name="a_shafinal-function"></a><span data-ttu-id="04d96-103">Une \_ fonction SHAFinal</span><span class="sxs-lookup"><span data-stu-id="04d96-103">A\_SHAFinal function</span></span>

<span data-ttu-id="04d96-104">Calcule le hachage final des données entrées par la fonction MD5Update.</span><span class="sxs-lookup"><span data-stu-id="04d96-104">Computes the final hash of the data entered by the MD5Update function.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d96-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04d96-105">Syntax</span></span>


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a><span data-ttu-id="04d96-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04d96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d96-107">*Contexte* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="04d96-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="04d96-108">Contexte SHA.</span><span class="sxs-lookup"><span data-stu-id="04d96-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="04d96-109">*Résultat* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04d96-109">*Result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04d96-110">Table de hachage résultante.</span><span class="sxs-lookup"><span data-stu-id="04d96-110">The resulting hash table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d96-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04d96-111">Return value</span></span>

<span data-ttu-id="04d96-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04d96-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d96-113">Notes</span><span class="sxs-lookup"><span data-stu-id="04d96-113">Remarks</span></span>

<span data-ttu-id="04d96-114">Cette fonction est très similaire à SHAFinal, mais elle est appelée directement à partir de la bibliothèque, plutôt que d’être routée via l’infrastructure de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="04d96-114">This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="04d96-115">Pour plus d’informations, consultez [fournisseurs NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="04d96-115">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="04d96-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04d96-116">Requirements</span></span>



| <span data-ttu-id="04d96-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04d96-117">Requirement</span></span> | <span data-ttu-id="04d96-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="04d96-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04d96-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="04d96-119">Header</span></span><br/>  | <dl> <span data-ttu-id="04d96-120"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d96-120"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="04d96-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04d96-121">Library</span></span><br/> | <dl> <span data-ttu-id="04d96-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d96-122"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="04d96-123">DLL</span><span class="sxs-lookup"><span data-stu-id="04d96-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="04d96-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d96-124"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 

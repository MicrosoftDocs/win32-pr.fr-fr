---
description: Récupère un nombre spécifié d’octets aléatoires à partir du générateur de nombres aléatoires du système.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513202"
---
# <a name="systemprng-function"></a><span data-ttu-id="31335-103">SystemPrng fonction)</span><span class="sxs-lookup"><span data-stu-id="31335-103">SystemPrng function</span></span>

<span data-ttu-id="31335-104">\[**SystemPrng** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="31335-104">\[**SystemPrng** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31335-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="31335-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="31335-106">Utilisez plutôt [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span><span class="sxs-lookup"><span data-stu-id="31335-106">Instead, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span></span>

<span data-ttu-id="31335-107">La fonction **SystemPrng** récupère un nombre spécifié d’octets aléatoires à partir du générateur de nombres aléatoires du système.</span><span class="sxs-lookup"><span data-stu-id="31335-107">The **SystemPrng** function retrieves a specified number of random bytes from the system random number generator.</span></span>

> [!Note]  
> <span data-ttu-id="31335-108">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="31335-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="31335-109">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31335-109">To call this function, you must create a user-defined header file.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="31335-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31335-110">Syntax</span></span>


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a><span data-ttu-id="31335-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31335-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31335-112">*pbRandomData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="31335-112">*pbRandomData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31335-113">Pointeur vers une mémoire tampon qui reçoit les octets récupérés.</span><span class="sxs-lookup"><span data-stu-id="31335-113">A pointer to a buffer that receives the retrieved bytes.</span></span>

</dd> <dt>

<span data-ttu-id="31335-114">*cbRandomData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31335-114">*cbRandomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31335-115">Nombre d'octets à récupérer.</span><span class="sxs-lookup"><span data-stu-id="31335-115">The number of bytes to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31335-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31335-116">Return value</span></span>

<span data-ttu-id="31335-117">Retourne toujours la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="31335-117">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="31335-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31335-118">Requirements</span></span>



| <span data-ttu-id="31335-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31335-119">Requirement</span></span> | <span data-ttu-id="31335-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="31335-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31335-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31335-121">Minimum supported client</span></span><br/> | <span data-ttu-id="31335-122">Windows Vista avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31335-122">Windows Vista with SP1 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="31335-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31335-123">Minimum supported server</span></span><br/> | <span data-ttu-id="31335-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31335-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                           |
| <span data-ttu-id="31335-125">DLL</span><span class="sxs-lookup"><span data-stu-id="31335-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31335-126"><dt>Ksecdd.sys sur Windows Server 2008 et Windows Vista avec SP1 ; </dt> <dt>Cng.sys sur Windows 7 et Windows Server 2008 R2</dt></span><span class="sxs-lookup"><span data-stu-id="31335-126"><dt>Ksecdd.sys on Windows Server 2008 and Windows Vista with SP1; </dt> <dt>Cng.sys on Windows 7 and Windows Server 2008 R2</dt></span></span> </dl> |



 

 





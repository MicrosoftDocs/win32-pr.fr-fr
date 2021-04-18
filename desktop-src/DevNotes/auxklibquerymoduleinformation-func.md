---
description: Récupère des informations sur l’ensemble de modules actuellement chargés pour le système.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Fonction AuxKlibQueryModuleInformation (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540354"
---
# <a name="auxklibquerymoduleinformation-function"></a><span data-ttu-id="07756-103">AuxKlibQueryModuleInformation fonction)</span><span class="sxs-lookup"><span data-stu-id="07756-103">AuxKlibQueryModuleInformation function</span></span>

<span data-ttu-id="07756-104">Récupère des informations sur l’ensemble de modules actuellement chargés pour le système.</span><span class="sxs-lookup"><span data-stu-id="07756-104">Retrieves information about the currently loaded set of modules for the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="07756-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07756-105">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a><span data-ttu-id="07756-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07756-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07756-107">*BufferSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="07756-107">*BufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07756-108">En entrée, taille de la mémoire tampon *QueryInfo* , en octets.</span><span class="sxs-lookup"><span data-stu-id="07756-108">On input, the size of the *QueryInfo* buffer, in bytes.</span></span> <span data-ttu-id="07756-109">Sur la sortie, reçoit la taille réelle requise.</span><span class="sxs-lookup"><span data-stu-id="07756-109">On output, receives the actual required size.</span></span> <span data-ttu-id="07756-110">Étant donné que la liste des modules système peut changer entre les appels, cette valeur peut également changer entre les appels.</span><span class="sxs-lookup"><span data-stu-id="07756-110">Because the system module list can change between calls, this value can also change between calls.</span></span>

</dd> <dt>

<span data-ttu-id="07756-111">*Éléments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07756-111">*ElementSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07756-112">Taille, en octets, d’un élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="07756-112">The size, in bytes, of an array element.</span></span> <span data-ttu-id="07756-113">Cette taille détermine le format de la sortie.</span><span class="sxs-lookup"><span data-stu-id="07756-113">This size determines the format of the output.</span></span>

</dd> <dt>

<span data-ttu-id="07756-114">*QueryInfo* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="07756-114">*QueryInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07756-115">Pointeur vers une mémoire tampon qui reçoit les informations du module.</span><span class="sxs-lookup"><span data-stu-id="07756-115">A pointer to a buffer that receives the module information.</span></span> <span data-ttu-id="07756-116">Ces informations sont retournées dans un tableau dont les éléments sont l’une des structures suivantes : [**\_ informations de \_ base \_ sur le module**](aux-module-basic-info-struct.md) ou [**\_ \_ \_ informations étendues du module**](aux-module-extended-info-struct.md)aux.</span><span class="sxs-lookup"><span data-stu-id="07756-116">This information is returned in an array whose elements are one of the following structures: [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) or [**AUX\_MODULE\_EXTENDED\_INFO**](aux-module-extended-info-struct.md).</span></span> <span data-ttu-id="07756-117">La structure spécifique utilisée dépend de la taille de l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="07756-117">The specific structure used depends on the specified element size.</span></span>

<span data-ttu-id="07756-118">Si ce paramètre a la **valeur null**, la fonction retourne la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="07756-118">If this parameter is **NULL**, the function returns the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07756-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07756-119">Return value</span></span>

<span data-ttu-id="07756-120">Si la fonction réussit, la valeur de retour est STATUs \_ successful.</span><span class="sxs-lookup"><span data-stu-id="07756-120">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="07756-121">Si la fonction échoue, la valeur de retour peut être l’un des codes d’État définis dans Ntstatus. h, qui est disponible dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="07756-121">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="07756-122">Notes</span><span class="sxs-lookup"><span data-stu-id="07756-122">Remarks</span></span>

<span data-ttu-id="07756-123">Vous devez appeler la fonction [**AuxKlibInitialize**](auxklibinitialize-func.md) avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="07756-123">You must call the [**AuxKlibInitialize**](auxklibinitialize-func.md) function before calling this function.</span></span>

<span data-ttu-id="07756-124">La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="07756-124">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="07756-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07756-125">Requirements</span></span>



| <span data-ttu-id="07756-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07756-126">Requirement</span></span> | <span data-ttu-id="07756-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="07756-127">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07756-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="07756-128">Redistributable</span></span><br/> | <span data-ttu-id="07756-129">Bibliothèque d’API auxiliaires Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="07756-129">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="07756-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="07756-130">Header</span></span><br/>          | <dl> <span data-ttu-id="07756-131"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="07756-131"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="07756-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="07756-132">Library</span></span><br/>         | <dl> <span data-ttu-id="07756-133"><dt>Aux \_ klib. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07756-133"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07756-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07756-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07756-135">**AuxKlibInitialize**</span><span class="sxs-lookup"><span data-stu-id="07756-135">**AuxKlibInitialize**</span></span>](auxklibinitialize-func.md)
</dt> <dt>

[<span data-ttu-id="07756-136">**\_informations de \_ base du module aux \_**</span><span class="sxs-lookup"><span data-stu-id="07756-136">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> <dt>

[<span data-ttu-id="07756-137">**\_ \_ informations étendues du module aux \_**</span><span class="sxs-lookup"><span data-stu-id="07756-137">**AUX\_MODULE\_EXTENDED\_INFO**</span></span>](aux-module-extended-info-struct.md)
</dt> </dl>

 

 





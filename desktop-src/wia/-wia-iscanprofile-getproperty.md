---
description: Obtient la valeur des propriétés enfants spécifiées dans le <Properties> élément d’un profil de numérisation.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'IScanProfile :: GetProperty, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524911"
---
# <a name="iscanprofilegetproperty-method"></a><span data-ttu-id="833a5-104">IScanProfile :: GetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="833a5-104">IScanProfile::GetProperty method</span></span>

<span data-ttu-id="833a5-105">Obtient la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="833a5-105">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="833a5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="833a5-106">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="833a5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="833a5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833a5-108">*nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="833a5-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="833a5-109">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="833a5-109">Type: **ULONG**</span></span>

<span data-ttu-id="833a5-110">Nombre d’entrées dans les tableaux qui sont pointés par *PID* et *pvar*.</span><span class="sxs-lookup"><span data-stu-id="833a5-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="833a5-111">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="833a5-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="833a5-112">Type : \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="833a5-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="833a5-113">Pointeur vers un tableau des numéros d’identification des propriétés à définir.</span><span class="sxs-lookup"><span data-stu-id="833a5-113">A pointer to an array of the identification numbers of the properties to be set.</span></span> <span data-ttu-id="833a5-114">Chaque valeur du tableau est une [constante de propriété WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="833a5-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="833a5-115">_pvar \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="833a5-115">_pvar\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="833a5-116">Tapez : \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="833a5-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="833a5-117">Pointeur vers un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="833a5-117">A pointer to an array of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="833a5-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="833a5-118">Return value</span></span>

<span data-ttu-id="833a5-119">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="833a5-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="833a5-120">Retourne \_ la valeur false si l’une des valeurs de propriété n’est pas disponible ; sinon, retourne s \_ OK ou un code d’erreur com standard.</span><span class="sxs-lookup"><span data-stu-id="833a5-120">Returns S\_FALSE if any of the property values is not available; otherwise, returns S\_OK or a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="833a5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="833a5-121">Remarks</span></span>

<span data-ttu-id="833a5-122">Le type de chaque valeur doit être du même type que celui qui a été défini avec l’appel à [**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="833a5-122">The type of each value must be the same type that was set with the call to [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).</span></span>

<span data-ttu-id="833a5-123">Chaque valeur du tableau que *PID* pointe vers est l’une des [constantes de propriété WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="833a5-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="833a5-124">Vous pouvez étendre ce système d’identification.</span><span class="sxs-lookup"><span data-stu-id="833a5-124">You can extend this identification system.</span></span> <span data-ttu-id="833a5-125">Consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="833a5-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="833a5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="833a5-126">Requirements</span></span>



| <span data-ttu-id="833a5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="833a5-127">Requirement</span></span> | <span data-ttu-id="833a5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="833a5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="833a5-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833a5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="833a5-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="833a5-130">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="833a5-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833a5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="833a5-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="833a5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="833a5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="833a5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="833a5-134"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="833a5-134"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="833a5-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="833a5-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="833a5-136"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="833a5-136"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833a5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="833a5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833a5-138">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="833a5-138">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="833a5-139">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="833a5-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="833a5-140">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="833a5-140">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="833a5-141">Constantes de propriété WIA</span><span class="sxs-lookup"><span data-stu-id="833a5-141">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="833a5-142">Définition des propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="833a5-142">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 

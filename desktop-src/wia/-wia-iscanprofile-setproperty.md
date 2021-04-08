---
description: Définit la valeur des propriétés enfants spécifiées dans le <Properties> élément d’un profil de numérisation.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'IScanProfile :: SetProperty, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752853"
---
# <a name="iscanprofilesetproperty-method"></a><span data-ttu-id="3d200-104">IScanProfile :: SetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="3d200-104">IScanProfile::SetProperty method</span></span>

<span data-ttu-id="3d200-105">Définit la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="3d200-105">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d200-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d200-106">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="3d200-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d200-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d200-108">*nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d200-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d200-109">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="3d200-109">Type: **ULONG**</span></span>

<span data-ttu-id="3d200-110">Nombre d’entrées dans les tableaux qui sont pointés par *PID* et *pvar*.</span><span class="sxs-lookup"><span data-stu-id="3d200-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="3d200-111">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d200-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d200-112">Type : \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="3d200-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="3d200-113">Pointeur vers un tableau de numéros d’identification des propriétés à définir.</span><span class="sxs-lookup"><span data-stu-id="3d200-113">A pointer to an array of identification numbers of the properties to be set.</span></span> <span data-ttu-id="3d200-114">Chaque valeur du tableau est une [constante de propriété WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d200-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d200-115">_pvar \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d200-115">_pvar\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d200-116">Tapez : \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="3d200-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="3d200-117">Pointeur vers un tableau de valeurs à assigner aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="3d200-117">A pointer to an array of values to be assigned to the properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d200-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d200-118">Return value</span></span>

<span data-ttu-id="3d200-119">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3d200-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3d200-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3d200-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d200-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3d200-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d200-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3d200-122">Remarks</span></span>

<span data-ttu-id="3d200-123">Chaque valeur du tableau que *PID* pointe vers est l’une des [constantes de propriété WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d200-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="3d200-124">Vous pouvez étendre ce système d’identification.</span><span class="sxs-lookup"><span data-stu-id="3d200-124">You can extend this identification system.</span></span> <span data-ttu-id="3d200-125">Consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3d200-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="3d200-126">Les modifications apportées à un profil ne sont pas enregistrées sur le disque tant que l’application n’a pas appelé la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="3d200-126">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="3d200-127">Si deux applications créent des objets de profil d’analyse à partir du même fichier XML, et que chaque application écrit des modifications dans son objet, seules les modifications apportées par l’application qui appelle [**IScanProfile :: Save**](-wia-iscanprofile-save.md) Last sont enregistrées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="3d200-127">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d200-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d200-128">Requirements</span></span>



| <span data-ttu-id="3d200-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d200-129">Requirement</span></span> | <span data-ttu-id="3d200-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d200-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d200-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d200-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3d200-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d200-132">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3d200-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d200-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3d200-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d200-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d200-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d200-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d200-136"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d200-136"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="3d200-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="3d200-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d200-138"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d200-138"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d200-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d200-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d200-140">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="3d200-140">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="3d200-141">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3d200-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3d200-142">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="3d200-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="3d200-143">Constantes de propriété WIA</span><span class="sxs-lookup"><span data-stu-id="3d200-143">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="3d200-144">Définition des propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="3d200-144">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 

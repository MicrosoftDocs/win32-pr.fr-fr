---
description: Supprime une liste spécifiée de propriétés enfants dans le <Properties> élément d’un profil de numérisation.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'IScanProfile :: RemoveProperty, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113910"
---
# <a name="iscanprofileremoveproperty-method"></a><span data-ttu-id="5c8d1-104">IScanProfile :: RemoveProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="5c8d1-104">IScanProfile::RemoveProperty method</span></span>

<span data-ttu-id="5c8d1-105">Supprime une liste spécifiée de propriétés enfants dans l' `<Properties>` élément d’un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-105">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c8d1-106">Syntax</span></span>


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a><span data-ttu-id="5c8d1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c8d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c8d1-108">*nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c8d1-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c8d1-109">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-109">Type: **ULONG**</span></span>

<span data-ttu-id="5c8d1-110">Nombre d’entrées dans le tableau sur lequel *PID* pointe.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-110">The number of entries in the array that *pid* points to.</span></span>

</dd> <dt>

<span data-ttu-id="5c8d1-111">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c8d1-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c8d1-112">Type : \**propid \** _</span><span class="sxs-lookup"><span data-stu-id="5c8d1-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="5c8d1-113">Pointeur vers un tableau de numéros d’identification des propriétés à supprimer.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-113">A pointer to an array of identification numbers of the properties to be deleted.</span></span> <span data-ttu-id="5c8d1-114">Chaque est une [constante de propriété WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5c8d1-114">Each is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c8d1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c8d1-115">Return value</span></span>

<span data-ttu-id="5c8d1-116">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5c8d1-116">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5c8d1-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c8d1-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c8d1-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8d1-119">Notes</span><span class="sxs-lookup"><span data-stu-id="5c8d1-119">Remarks</span></span>

<span data-ttu-id="5c8d1-120">Chaque valeur du tableau que *PID* pointe vers est l’une des [constantes de propriété WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5c8d1-120">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="5c8d1-121">Vous pouvez étendre ce système d’identification.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-121">You can extend this identification system.</span></span> <span data-ttu-id="5c8d1-122">Consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5c8d1-122">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="5c8d1-123">Les modifications apportées à un profil ne sont pas enregistrées sur le disque tant que l’application n’a pas appelé la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="5c8d1-123">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="5c8d1-124">Si deux applications créent des objets de profil d’analyse à partir du même fichier XML, et que chaque application écrit des modifications dans son objet, seules les modifications apportées par l’application qui appelle [**IScanProfile :: Save**](-wia-iscanprofile-save.md) Last sont enregistrées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="5c8d1-124">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8d1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c8d1-125">Requirements</span></span>



| <span data-ttu-id="5c8d1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c8d1-126">Requirement</span></span> | <span data-ttu-id="5c8d1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c8d1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8d1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c8d1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c8d1-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c8d1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5c8d1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c8d1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c8d1-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c8d1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c8d1-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c8d1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c8d1-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c8d1-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="5c8d1-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="5c8d1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c8d1-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c8d1-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c8d1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c8d1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c8d1-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="5c8d1-138">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5c8d1-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c8d1-139">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="5c8d1-139">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="5c8d1-140">Constantes de propriété WIA</span><span class="sxs-lookup"><span data-stu-id="5c8d1-140">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="5c8d1-141">Définition des propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="5c8d1-141">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 





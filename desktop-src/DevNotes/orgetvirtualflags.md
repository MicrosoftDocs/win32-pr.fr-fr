---
description: Récupère les indicateurs virtuels sur la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: ORGetVirtualFlags, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543814"
---
# <a name="orgetvirtualflags-function"></a><span data-ttu-id="379da-103">ORGetVirtualFlags fonction)</span><span class="sxs-lookup"><span data-stu-id="379da-103">ORGetVirtualFlags function</span></span>

<span data-ttu-id="379da-104">Récupère les indicateurs virtuels sur la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="379da-104">Retrieves the virtual flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="379da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="379da-105">Syntax</span></span>


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="379da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="379da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="379da-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="379da-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="379da-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="379da-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="379da-109">*pdwFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="379da-109">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="379da-110">Pointeur vers une variable qui reçoit les indicateurs de virtualisation définis pour la clé.</span><span class="sxs-lookup"><span data-stu-id="379da-110">A pointer to a variable to receive the virtualization flags set for the key.</span></span> <span data-ttu-id="379da-111">Une fois que la fonction a retourné une valeur, ce paramètre peut avoir une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="379da-111">After the function returns, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="379da-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="379da-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="379da-113">Signification</span><span class="sxs-lookup"><span data-stu-id="379da-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="379da-114"><dt>**Reg \_ La clé ne dispose pas d’un \_ \_ \_ échec silencieux**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="379da-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="379da-115">Si cet indicateur est défini et qu’une opération d’ouverture échoue sur une clé pour laquelle la virtualisation est activée, le registre ne tente pas de rouvrir la clé.</span><span class="sxs-lookup"><span data-stu-id="379da-115">If this flag is set and an Open operation fails on a key that has virtualization enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="379da-116">Si cet indicateur est désactivé, le registre tente de rouvrir la clé avec un \_ accès maximal autorisé.</span><span class="sxs-lookup"><span data-stu-id="379da-116">If this flag is clear, the registry attempts to reopen the key with MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="379da-117"><dt>**Reg \_ CLÉ \_ non \_ virtualisée**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="379da-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="379da-118">Si cet indicateur est défini et qu’une opération de création de clé échoue parce que l’appelant n’a pas le \_ droit créer une \_ sous- \_ clé de clé sur la clé parente, le registre fait échouer l’opération de création.</span><span class="sxs-lookup"><span data-stu-id="379da-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="379da-119">Si cet indicateur est désactivé, le registre tente de créer la clé dans le magasin virtuel.</span><span class="sxs-lookup"><span data-stu-id="379da-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="379da-120">L’appelant doit disposer de la clé \_ Read Right sur la clé parente.</span><span class="sxs-lookup"><span data-stu-id="379da-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="379da-121"><dt>**Reg \_ \_ \_ Indicateur recurse de clé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="379da-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="379da-122">Si cet indicateur est défini, les indicateurs de virtualisation du Registre sont propagés à partir de la clé parente.</span><span class="sxs-lookup"><span data-stu-id="379da-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="379da-123">Si cet indicateur est désactivé, les indicateurs de virtualisation du registre ne sont pas propagés.</span><span class="sxs-lookup"><span data-stu-id="379da-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="379da-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="379da-124">Return value</span></span>

<span data-ttu-id="379da-125">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="379da-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="379da-126">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="379da-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="379da-127">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="379da-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="379da-128">Notes</span><span class="sxs-lookup"><span data-stu-id="379da-128">Remarks</span></span>

<span data-ttu-id="379da-129">La virtualisation du Registre est une technologie de compatibilité des applications temporaire qui permet d’effectuer des opérations d’écriture dans le Registre qui ont un impact global sur les emplacements par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="379da-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="379da-130">Cette redirection est transparente pour les applications qui lisent ou écrivent dans le registre.</span><span class="sxs-lookup"><span data-stu-id="379da-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="379da-131">La virtualisation du Registre est prise en charge à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="379da-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="379da-132">Toutefois, Microsoft envisage de la supprimer des versions futures du système d’exploitation Windows à mesure que d’autres applications sont compatibles avec Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="379da-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="379da-133">Par conséquent, les applications ne doivent pas dépendre du comportement de la virtualisation du Registre dans le système.</span><span class="sxs-lookup"><span data-stu-id="379da-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="379da-134">La virtualisation du Registre est activée uniquement pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="379da-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="379da-135">processus interactifs 32 bits</span><span class="sxs-lookup"><span data-stu-id="379da-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="379da-136">Clés dans **HKEY \_ local \_ machine \\ Software**</span><span class="sxs-lookup"><span data-stu-id="379da-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="379da-137">Clés dans lesquelles un administrateur peut écrire</span><span class="sxs-lookup"><span data-stu-id="379da-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="379da-138">Pour plus d’informations, consultez [virtualisation du Registre](../sysinfo/registry-virtualization.md).</span><span class="sxs-lookup"><span data-stu-id="379da-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="379da-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="379da-139">Requirements</span></span>



| <span data-ttu-id="379da-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="379da-140">Requirement</span></span> | <span data-ttu-id="379da-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="379da-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="379da-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="379da-142">Redistributable</span></span><br/> | <span data-ttu-id="379da-143">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="379da-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="379da-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="379da-144">Header</span></span><br/>          | <dl> <span data-ttu-id="379da-145"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="379da-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="379da-146">DLL</span><span class="sxs-lookup"><span data-stu-id="379da-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="379da-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="379da-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="379da-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="379da-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="379da-149">**ORSetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="379da-149">**ORSetVirtualFlags**</span></span>](orsetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="379da-150">Virtualisation du Registre</span><span class="sxs-lookup"><span data-stu-id="379da-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 

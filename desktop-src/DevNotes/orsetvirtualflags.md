---
description: Définit des indicateurs de virtualisation sur la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: ORSetVirtualFlags, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: f694d69684a474cfa6d4f6c33c6d8cab7072f605
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543158"
---
# <a name="orsetvirtualflags-function"></a><span data-ttu-id="cf556-103">ORSetVirtualFlags fonction)</span><span class="sxs-lookup"><span data-stu-id="cf556-103">ORSetVirtualFlags function</span></span>

<span data-ttu-id="cf556-104">Définit des indicateurs de virtualisation sur la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="cf556-104">Sets virtualization flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf556-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf556-105">Syntax</span></span>


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cf556-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf556-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf556-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf556-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf556-108">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="cf556-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="cf556-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf556-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf556-110">Ce paramètre contrôle le comportement du Registre lorsqu’une opération de création ou d’ouverture échoue sur une clé dans une ruche virtualisée.</span><span class="sxs-lookup"><span data-stu-id="cf556-110">This parameter controls the behavior of the registry when a Create or Open operation fails on a key in a virtualized hive.</span></span> <span data-ttu-id="cf556-111">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf556-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cf556-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf556-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="cf556-113">Signification</span><span class="sxs-lookup"><span data-stu-id="cf556-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="cf556-114"><dt>**Reg \_ La clé ne dispose pas d’un \_ \_ \_ échec silencieux**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cf556-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="cf556-115">Si cet indicateur est défini et qu’une opération d’ouverture échoue sur une clé pour laquelle la virtualisation est activée, le registre n’essaie pas de rouvrir la clé.</span><span class="sxs-lookup"><span data-stu-id="cf556-115">If this flag is set and an Open operation fails on a key for which virtualization is enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="cf556-116">Si cet indicateur est désactivé, le registre tente de rouvrir la clé avec le MAXIMUM d' \_ accès autorisé.</span><span class="sxs-lookup"><span data-stu-id="cf556-116">If this flag is clear, the registry attempts to reopen the key with the MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="cf556-117"><dt>**Reg \_ CLÉ \_ non \_ virtualisée**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cf556-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="cf556-118">Si cet indicateur est défini et qu’une opération de création de clé échoue parce que l’appelant n’a pas le \_ droit créer une \_ sous- \_ clé de clé sur la clé parente, le registre fait échouer l’opération de création.</span><span class="sxs-lookup"><span data-stu-id="cf556-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="cf556-119">Si cet indicateur est désactivé, le registre tente de créer la clé dans le magasin virtuel.</span><span class="sxs-lookup"><span data-stu-id="cf556-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="cf556-120">L’appelant doit disposer de la clé \_ Read Right sur la clé parente.</span><span class="sxs-lookup"><span data-stu-id="cf556-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="cf556-121"><dt>**Reg \_ \_ \_ Indicateur recurse de clé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="cf556-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="cf556-122">Si cet indicateur est défini, les indicateurs de virtualisation du Registre sont propagés à partir de la clé parente.</span><span class="sxs-lookup"><span data-stu-id="cf556-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="cf556-123">Si cet indicateur est désactivé, les indicateurs de virtualisation du registre ne sont pas propagés.</span><span class="sxs-lookup"><span data-stu-id="cf556-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf556-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf556-124">Return value</span></span>

<span data-ttu-id="cf556-125">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="cf556-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="cf556-126">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="cf556-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="cf556-127">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="cf556-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf556-128">Notes</span><span class="sxs-lookup"><span data-stu-id="cf556-128">Remarks</span></span>

<span data-ttu-id="cf556-129">La virtualisation du Registre est une technologie de compatibilité des applications temporaire qui permet d’effectuer des opérations d’écriture dans le Registre qui ont un impact global sur les emplacements par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf556-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="cf556-130">Cette redirection est transparente pour les applications qui lisent ou écrivent dans le registre.</span><span class="sxs-lookup"><span data-stu-id="cf556-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="cf556-131">La virtualisation du Registre est prise en charge à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf556-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="cf556-132">Toutefois, Microsoft envisage de la supprimer des versions futures du système d’exploitation Windows à mesure que d’autres applications sont compatibles avec Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf556-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="cf556-133">Par conséquent, les applications ne doivent pas dépendre du comportement de la virtualisation du Registre dans le système.</span><span class="sxs-lookup"><span data-stu-id="cf556-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="cf556-134">La virtualisation du Registre est activée uniquement pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="cf556-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="cf556-135">processus interactifs 32 bits</span><span class="sxs-lookup"><span data-stu-id="cf556-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="cf556-136">Clés dans **HKEY \_ local \_ machine \\ Software**</span><span class="sxs-lookup"><span data-stu-id="cf556-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="cf556-137">Clés dans lesquelles un administrateur peut écrire</span><span class="sxs-lookup"><span data-stu-id="cf556-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="cf556-138">Pour plus d’informations, consultez [virtualisation du Registre](../sysinfo/registry-virtualization.md).</span><span class="sxs-lookup"><span data-stu-id="cf556-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf556-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf556-139">Requirements</span></span>



| <span data-ttu-id="cf556-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf556-140">Requirement</span></span> | <span data-ttu-id="cf556-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf556-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf556-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="cf556-142">Redistributable</span></span><br/> | <span data-ttu-id="cf556-143">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="cf556-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="cf556-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf556-144">Header</span></span><br/>          | <dl> <span data-ttu-id="cf556-145"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf556-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf556-146">DLL</span><span class="sxs-lookup"><span data-stu-id="cf556-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="cf556-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf556-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf556-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf556-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf556-149">**ORGetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="cf556-149">**ORGetVirtualFlags**</span></span>](orgetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="cf556-150">Virtualisation du Registre</span><span class="sxs-lookup"><span data-stu-id="cf556-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 

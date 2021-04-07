---
description: Définissez la nouvelle configuration active du collecteur.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Méthode SetConfiguration de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747781"
---
# <a name="setconfiguration-method-of-the-control-class"></a><span data-ttu-id="ae66e-103">Méthode SetConfiguration de la classe Control</span><span class="sxs-lookup"><span data-stu-id="ae66e-103">SetConfiguration method of the Control class</span></span>

<span data-ttu-id="ae66e-104">Définissez la nouvelle configuration active du collecteur.</span><span class="sxs-lookup"><span data-stu-id="ae66e-104">Set the new active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae66e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae66e-105">Syntax</span></span>


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="ae66e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae66e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae66e-107">*Configuration* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-108">Configuration à activer.</span><span class="sxs-lookup"><span data-stu-id="ae66e-108">The configuration to activate.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-109">*OldTimestampLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-110">Bits de poids faible d’un horodatage qui indique quand la configuration active actuelle a été définie.</span><span class="sxs-lookup"><span data-stu-id="ae66e-110">The low-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="ae66e-111">La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="ae66e-111">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-112">*OldTimestampHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-113">Bits de poids fort d’un horodatage qui indique quand la configuration active actuelle a été définie.</span><span class="sxs-lookup"><span data-stu-id="ae66e-113">The high-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="ae66e-114">La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="ae66e-114">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-115">*NewTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-115">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-116">Lorsque cette méthode est retournée, ce paramètre contient les bits de poids faible d’un horodatage qui indique quand la nouvelle configuration a été définie.</span><span class="sxs-lookup"><span data-stu-id="ae66e-116">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="ae66e-117">La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="ae66e-117">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-118">*NewTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-118">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-119">Lorsque cette méthode est retournée, ce paramètre contient les bits de poids fort de l’horodatage qui indique quand la nouvelle configuration a été définie.</span><span class="sxs-lookup"><span data-stu-id="ae66e-119">When this method returns, this parameter contains the high-order bits of the timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="ae66e-120">La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="ae66e-120">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-121">*ErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-121">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-122">Lorsque cette méthode est retournée, en cas d’erreur, ce paramètre contient la description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae66e-122">When this method returns, if there was an error, this parameter contains the error description.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-123">*WarningString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-123">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-124">Lorsque cette méthode est retournée, ce paramètre contient tous les messages d’avertissement relatifs à l’opération.</span><span class="sxs-lookup"><span data-stu-id="ae66e-124">When this method returns, this parameter contains any warnings messages for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-125">*InfoString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-125">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-126">Lorsque cette méthode est retournée, ce paramètre contient des informations relatives à la nouvelle configuration active.</span><span class="sxs-lookup"><span data-stu-id="ae66e-126">When this method returns, this parameter contains information for the new active configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-127">*ErrorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-127">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-128">Lorsque cette méthode est retournée, en cas d’erreur, ce paramètre indique le type d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae66e-128">When this method returns, if there was an error, this parameter indicates the error type.</span></span>

<dt>

<span data-ttu-id="ae66e-129">0</span><span class="sxs-lookup"><span data-stu-id="ae66e-129">0</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-130">La nouvelle configuration est manquante.</span><span class="sxs-lookup"><span data-stu-id="ae66e-130">The new configuration is missing.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-131">1</span><span class="sxs-lookup"><span data-stu-id="ae66e-131">1</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-132">Le format de la nouvelle configuration n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ae66e-132">The format of the new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-133">2</span><span class="sxs-lookup"><span data-stu-id="ae66e-133">2</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-134">La nouvelle configuration n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ae66e-134">The new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-135">3</span><span class="sxs-lookup"><span data-stu-id="ae66e-135">3</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-136">Une erreur s’est produite en raison d’un socket ouvert.</span><span class="sxs-lookup"><span data-stu-id="ae66e-136">There was an error caused by an open socket.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-137">4</span><span class="sxs-lookup"><span data-stu-id="ae66e-137">4</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-138">Une erreur d’écriture de fichier s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ae66e-138">There was a file write error.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-139">5</span><span class="sxs-lookup"><span data-stu-id="ae66e-139">5</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-140">Une erreur d’atomicité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ae66e-140">There was an atomicity error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae66e-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae66e-141">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="ae66e-142">0</span><span class="sxs-lookup"><span data-stu-id="ae66e-142">0</span></span>

<span data-ttu-id="ae66e-143">Échec</span><span class="sxs-lookup"><span data-stu-id="ae66e-143">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ae66e-144">1</span><span class="sxs-lookup"><span data-stu-id="ae66e-144">1</span></span>

<span data-ttu-id="ae66e-145">Succès</span><span class="sxs-lookup"><span data-stu-id="ae66e-145">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae66e-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae66e-146">Requirements</span></span>



| <span data-ttu-id="ae66e-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae66e-147">Requirement</span></span> | <span data-ttu-id="ae66e-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae66e-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae66e-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae66e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ae66e-150">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ae66e-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae66e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ae66e-152">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ae66e-152">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="ae66e-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ae66e-153">Namespace</span></span><br/>                | <span data-ttu-id="ae66e-154">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="ae66e-154">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="ae66e-155">MOF</span><span class="sxs-lookup"><span data-stu-id="ae66e-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae66e-156"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae66e-156"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae66e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ae66e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae66e-158"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae66e-158"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ae66e-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae66e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae66e-160">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="ae66e-160">**Control**</span></span>](control.md)
</dt> </dl>

 

 





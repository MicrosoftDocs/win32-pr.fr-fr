---
description: Réinitialiser la configuration active du collecteur à partir du fichier de sauvegarde ultérieur (déterminé par la progression à partir de l’horodatage d’origine actuel). Si la configuration a été annulée, cela signifie que la modification n’a pas été effectuée.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Méthode Redo de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110058"
---
# <a name="redo-method-of-the-control-class"></a><span data-ttu-id="e768d-104">Méthode Redo de la classe Control</span><span class="sxs-lookup"><span data-stu-id="e768d-104">Redo method of the Control class</span></span>

<span data-ttu-id="e768d-105">Réinitialiser la configuration active du collecteur à partir du fichier de sauvegarde ultérieur (déterminé par la progression à partir de l’horodatage d’origine actuel).</span><span class="sxs-lookup"><span data-stu-id="e768d-105">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="e768d-106">Si la configuration a été annulée, cela signifie que la modification n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="e768d-106">If the configuration has been undone, this means redoing the undone change.</span></span>

## <a name="syntax"></a><span data-ttu-id="e768d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e768d-107">Syntax</span></span>


```mof
Uint32 Redo(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="e768d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e768d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e768d-109">*OldTimestampLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e768d-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-110">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="e768d-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="e768d-111">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="e768d-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="e768d-112">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e768d-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e768d-113">*OldTimestampHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e768d-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-114">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="e768d-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="e768d-115">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="e768d-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="e768d-116">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e768d-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e768d-117">*NewTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-118">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="e768d-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="e768d-119">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e768d-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e768d-120">*NewTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-121">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="e768d-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="e768d-122">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e768d-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e768d-123">*OriginalTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-124">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="e768d-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="e768d-125">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e768d-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e768d-126">*OriginalTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-127">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="e768d-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="e768d-128">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e768d-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e768d-129">*ErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-130">Chaîne de texte avec une explication de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e768d-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="e768d-131">*WarningString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-132">Chaîne de texte avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="e768d-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="e768d-133">*InfoString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-134">Chaîne de texte contenant des informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="e768d-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e768d-135">*ErrorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e768d-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e768d-136">Type de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="e768d-136">The type of the error.</span></span> <span data-ttu-id="e768d-137">Notez que 0 ou absent indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="e768d-137">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="e768d-138">0</span><span class="sxs-lookup"><span data-stu-id="e768d-138">0</span></span>
</dt> <dd>

<span data-ttu-id="e768d-139">Réussite.</span><span class="sxs-lookup"><span data-stu-id="e768d-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="e768d-140">1</span><span class="sxs-lookup"><span data-stu-id="e768d-140">1</span></span>
</dt> <dd>

<span data-ttu-id="e768d-141">format d’argument incorrect</span><span class="sxs-lookup"><span data-stu-id="e768d-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="e768d-142">2</span><span class="sxs-lookup"><span data-stu-id="e768d-142">2</span></span>
</dt> <dd>

<span data-ttu-id="e768d-143">valeur d’argument incorrecte</span><span class="sxs-lookup"><span data-stu-id="e768d-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="e768d-144">3</span><span class="sxs-lookup"><span data-stu-id="e768d-144">3</span></span>
</dt> <dd>

<span data-ttu-id="e768d-145">erreur d’ouverture de ressource (Socket)</span><span class="sxs-lookup"><span data-stu-id="e768d-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="e768d-146">4</span><span class="sxs-lookup"><span data-stu-id="e768d-146">4</span></span>
</dt> <dd>

<span data-ttu-id="e768d-147">erreur de persistance (écriture de fichier)</span><span class="sxs-lookup"><span data-stu-id="e768d-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="e768d-148">5</span><span class="sxs-lookup"><span data-stu-id="e768d-148">5</span></span>
</dt> <dd>

<span data-ttu-id="e768d-149">erreur d’atomicité (l’ancien horodatage ne correspond pas)</span><span class="sxs-lookup"><span data-stu-id="e768d-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e768d-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e768d-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="e768d-151">0</span><span class="sxs-lookup"><span data-stu-id="e768d-151">0</span></span>

<span data-ttu-id="e768d-152">Échec</span><span class="sxs-lookup"><span data-stu-id="e768d-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e768d-153">1</span><span class="sxs-lookup"><span data-stu-id="e768d-153">1</span></span>

<span data-ttu-id="e768d-154">Succès</span><span class="sxs-lookup"><span data-stu-id="e768d-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e768d-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e768d-155">Requirements</span></span>



| <span data-ttu-id="e768d-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e768d-156">Requirement</span></span> | <span data-ttu-id="e768d-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="e768d-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e768d-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e768d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e768d-159">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e768d-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e768d-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e768d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e768d-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e768d-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="e768d-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e768d-162">Namespace</span></span><br/>                | <span data-ttu-id="e768d-163">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="e768d-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="e768d-164">MOF</span><span class="sxs-lookup"><span data-stu-id="e768d-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e768d-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e768d-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="e768d-166">DLL</span><span class="sxs-lookup"><span data-stu-id="e768d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e768d-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e768d-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e768d-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e768d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e768d-169">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="e768d-169">**Control**</span></span>](control.md)
</dt> </dl>

 


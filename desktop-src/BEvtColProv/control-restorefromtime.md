---
description: Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde, sélectionné par un horodateur.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Méthode RestoreFromTime de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516399"
---
# <a name="restorefromtime-method-of-the-control-class"></a><span data-ttu-id="0d6f2-103">Méthode RestoreFromTime de la classe Control</span><span class="sxs-lookup"><span data-stu-id="0d6f2-103">RestoreFromTime method of the Control class</span></span>

<span data-ttu-id="0d6f2-104">Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde, sélectionné par un horodateur.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-104">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d6f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d6f2-105">Syntax</span></span>


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
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



## <a name="parameters"></a><span data-ttu-id="0d6f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d6f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d6f2-107">*TargetTimestampLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-107">*TargetTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-108">Restaurez le fichier de sauvegarde à cet horodateur.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-108">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="0d6f2-109">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-110">*TargetTimestampHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-110">*TargetTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-111">Restaurez le fichier de sauvegarde à cet horodateur.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-111">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="0d6f2-112">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-113">*OldTimestampLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-113">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-114">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="0d6f2-115">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0d6f2-116">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-116">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-117">*OldTimestampHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-117">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-118">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-118">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="0d6f2-119">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-119">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0d6f2-120">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-121">*NewTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-121">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-122">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="0d6f2-123">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-123">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-124">*NewTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-124">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-125">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-125">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="0d6f2-126">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-126">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-127">*OriginalTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-127">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-128">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="0d6f2-129">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-129">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-130">*OriginalTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-130">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-131">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-131">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="0d6f2-132">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0d6f2-132">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-133">*ErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-133">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-134">Chaîne de texte avec une explication de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-134">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-135">*WarningString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-135">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-136">Chaîne de texte avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-136">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-137">*InfoString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-137">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-138">Chaîne de texte contenant des informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-138">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-139">*ErrorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-139">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-140">Type de l’erreur : Notez que 0 ou absent indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-140">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="0d6f2-141">0</span><span class="sxs-lookup"><span data-stu-id="0d6f2-141">0</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-142">Réussite.</span><span class="sxs-lookup"><span data-stu-id="0d6f2-142">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-143">1</span><span class="sxs-lookup"><span data-stu-id="0d6f2-143">1</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-144">format d’argument incorrect</span><span class="sxs-lookup"><span data-stu-id="0d6f2-144">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-145">2</span><span class="sxs-lookup"><span data-stu-id="0d6f2-145">2</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-146">valeur d’argument incorrecte</span><span class="sxs-lookup"><span data-stu-id="0d6f2-146">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-147">3</span><span class="sxs-lookup"><span data-stu-id="0d6f2-147">3</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-148">erreur d’ouverture de ressource (Socket)</span><span class="sxs-lookup"><span data-stu-id="0d6f2-148">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-149">4</span><span class="sxs-lookup"><span data-stu-id="0d6f2-149">4</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-150">erreur de persistance (écriture de fichier)</span><span class="sxs-lookup"><span data-stu-id="0d6f2-150">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="0d6f2-151">5</span><span class="sxs-lookup"><span data-stu-id="0d6f2-151">5</span></span>
</dt> <dd>

<span data-ttu-id="0d6f2-152">erreur d’atomicité (l’ancien horodatage ne correspond pas)</span><span class="sxs-lookup"><span data-stu-id="0d6f2-152">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d6f2-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d6f2-153">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0d6f2-154">0</span><span class="sxs-lookup"><span data-stu-id="0d6f2-154">0</span></span>

<span data-ttu-id="0d6f2-155">Échec</span><span class="sxs-lookup"><span data-stu-id="0d6f2-155">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0d6f2-156">1</span><span class="sxs-lookup"><span data-stu-id="0d6f2-156">1</span></span>

<span data-ttu-id="0d6f2-157">Succès</span><span class="sxs-lookup"><span data-stu-id="0d6f2-157">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d6f2-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d6f2-158">Requirements</span></span>



| <span data-ttu-id="0d6f2-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d6f2-159">Requirement</span></span> | <span data-ttu-id="0d6f2-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d6f2-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6f2-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d6f2-161">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6f2-162">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d6f2-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0d6f2-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d6f2-163">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6f2-164">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0d6f2-164">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="0d6f2-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d6f2-165">Namespace</span></span><br/>                | <span data-ttu-id="0d6f2-166">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="0d6f2-166">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="0d6f2-167">MOF</span><span class="sxs-lookup"><span data-stu-id="0d6f2-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d6f2-168"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d6f2-168"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d6f2-169">DLL</span><span class="sxs-lookup"><span data-stu-id="0d6f2-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d6f2-170"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d6f2-170"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0d6f2-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d6f2-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d6f2-172">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="0d6f2-172">**Control**</span></span>](control.md)
</dt> </dl>

 


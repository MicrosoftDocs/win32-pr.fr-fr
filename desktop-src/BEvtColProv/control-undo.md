---
description: Restaure la configuration active du collecteur à partir du fichier de sauvegarde précédent (déterminé par le retour à partir de l’horodateur d’origine actuel).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Méthode Undo de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514736"
---
# <a name="undo-method-of-the-control-class"></a><span data-ttu-id="668b1-103">Méthode Undo de la classe Control</span><span class="sxs-lookup"><span data-stu-id="668b1-103">Undo method of the Control class</span></span>

<span data-ttu-id="668b1-104">Restaure la configuration active du collecteur à partir du fichier de sauvegarde précédent (déterminé par le retour à partir de l’horodateur d’origine actuel).</span><span class="sxs-lookup"><span data-stu-id="668b1-104">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="668b1-105">Si la configuration a été définie, cela signifie que vous annulez cette modification.</span><span class="sxs-lookup"><span data-stu-id="668b1-105">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="668b1-106">Les appels consécutifs sont annulés à la configuration antérieure et antérieure.</span><span class="sxs-lookup"><span data-stu-id="668b1-106">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="668b1-107">Retourne 1 en cas de réussite, 0 en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="668b1-107">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="668b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="668b1-108">Syntax</span></span>


```mof
Uint32 Undo(
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



## <a name="parameters"></a><span data-ttu-id="668b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="668b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="668b1-110">*OldTimestampLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="668b1-110">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-111">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="668b1-111">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="668b1-112">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="668b1-112">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="668b1-113">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="668b1-113">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="668b1-114">*OldTimestampHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="668b1-114">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-115">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="668b1-115">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="668b1-116">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="668b1-116">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="668b1-117">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="668b1-117">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="668b1-118">*NewTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-118">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-119">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="668b1-119">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="668b1-120">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="668b1-120">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="668b1-121">*NewTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-121">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-122">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="668b1-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="668b1-123">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="668b1-123">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="668b1-124">*OriginalTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-124">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-125">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="668b1-125">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="668b1-126">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="668b1-126">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="668b1-127">*OriginalTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-127">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-128">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="668b1-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="668b1-129">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="668b1-129">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="668b1-130">*ErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-130">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-131">Chaîne de texte avec une explication de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="668b1-131">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="668b1-132">*WarningString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-132">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-133">Chaîne de texte avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="668b1-133">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="668b1-134">*InfoString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-134">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-135">Chaîne de texte contenant des informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="668b1-135">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="668b1-136">*ErrorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="668b1-136">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="668b1-137">Type de l’erreur : Notez que 0 ou absent indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="668b1-137">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="668b1-138">0</span><span class="sxs-lookup"><span data-stu-id="668b1-138">0</span></span>
</dt> <dd>

<span data-ttu-id="668b1-139">Réussite.</span><span class="sxs-lookup"><span data-stu-id="668b1-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="668b1-140">1</span><span class="sxs-lookup"><span data-stu-id="668b1-140">1</span></span>
</dt> <dd>

<span data-ttu-id="668b1-141">format d’argument incorrect</span><span class="sxs-lookup"><span data-stu-id="668b1-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="668b1-142">2</span><span class="sxs-lookup"><span data-stu-id="668b1-142">2</span></span>
</dt> <dd>

<span data-ttu-id="668b1-143">valeur d’argument incorrecte</span><span class="sxs-lookup"><span data-stu-id="668b1-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="668b1-144">3</span><span class="sxs-lookup"><span data-stu-id="668b1-144">3</span></span>
</dt> <dd>

<span data-ttu-id="668b1-145">erreur d’ouverture de ressource (Socket)</span><span class="sxs-lookup"><span data-stu-id="668b1-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="668b1-146">4</span><span class="sxs-lookup"><span data-stu-id="668b1-146">4</span></span>
</dt> <dd>

<span data-ttu-id="668b1-147">erreur de persistance (écriture de fichier)</span><span class="sxs-lookup"><span data-stu-id="668b1-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="668b1-148">5</span><span class="sxs-lookup"><span data-stu-id="668b1-148">5</span></span>
</dt> <dd>

<span data-ttu-id="668b1-149">erreur d’atomicité (l’ancien horodatage ne correspond pas)</span><span class="sxs-lookup"><span data-stu-id="668b1-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="668b1-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="668b1-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="668b1-151">0</span><span class="sxs-lookup"><span data-stu-id="668b1-151">0</span></span>

<span data-ttu-id="668b1-152">Échec</span><span class="sxs-lookup"><span data-stu-id="668b1-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="668b1-153">1</span><span class="sxs-lookup"><span data-stu-id="668b1-153">1</span></span>

<span data-ttu-id="668b1-154">Succès</span><span class="sxs-lookup"><span data-stu-id="668b1-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="668b1-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="668b1-155">Requirements</span></span>



| <span data-ttu-id="668b1-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="668b1-156">Requirement</span></span> | <span data-ttu-id="668b1-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="668b1-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668b1-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="668b1-158">Minimum supported client</span></span><br/> | <span data-ttu-id="668b1-159">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="668b1-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="668b1-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="668b1-160">Minimum supported server</span></span><br/> | <span data-ttu-id="668b1-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="668b1-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="668b1-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="668b1-162">Namespace</span></span><br/>                | <span data-ttu-id="668b1-163">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="668b1-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="668b1-164">MOF</span><span class="sxs-lookup"><span data-stu-id="668b1-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="668b1-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="668b1-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="668b1-166">DLL</span><span class="sxs-lookup"><span data-stu-id="668b1-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="668b1-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="668b1-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="668b1-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="668b1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="668b1-169">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="668b1-169">**Control**</span></span>](control.md)
</dt> </dl>

 


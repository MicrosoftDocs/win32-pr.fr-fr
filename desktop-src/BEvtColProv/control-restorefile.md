---
description: Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Méthode RestoreFile de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950407"
---
# <a name="restorefile-method-of-the-control-class"></a><span data-ttu-id="2ff47-103">Méthode RestoreFile de la classe Control</span><span class="sxs-lookup"><span data-stu-id="2ff47-103">RestoreFile method of the Control class</span></span>

<span data-ttu-id="2ff47-104">Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2ff47-104">Restore the active configuration of the collector from a backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff47-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ff47-105">Syntax</span></span>


```mof
Uint32 RestoreFile(
  [in]  string File,
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



## <a name="parameters"></a><span data-ttu-id="2ff47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ff47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff47-107">*Fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-107">*File* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-108">Nom du fichier de sauvegarde à restaurer, dans la liste retournée par ListBackups ().</span><span class="sxs-lookup"><span data-stu-id="2ff47-108">Name of the backup file to restore, from the list returned by ListBackups().</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-109">*OldTimestampLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-110">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="2ff47-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="2ff47-111">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="2ff47-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="2ff47-112">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2ff47-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-113">*OldTimestampHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-114">Horodateur de la définition de la configuration précédente.</span><span class="sxs-lookup"><span data-stu-id="2ff47-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="2ff47-115">Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="2ff47-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="2ff47-116">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2ff47-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-117">*NewTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-118">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ff47-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="2ff47-119">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2ff47-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-120">*NewTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-121">Horodateur de la définition de la nouvelle configuration, si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ff47-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="2ff47-122">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2ff47-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-123">*OriginalTimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-124">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="2ff47-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="2ff47-125">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2ff47-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-126">*OriginalTimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-127">Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="2ff47-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="2ff47-128">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="2ff47-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-129">*ErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-130">Chaîne de texte avec une explication de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2ff47-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-131">*WarningString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-132">Chaîne de texte avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="2ff47-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-133">*InfoString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-134">Chaîne de texte contenant des informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="2ff47-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-135">*ErrorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-136">Type de l’erreur : Notez que 0 ou absent indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="2ff47-136">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="2ff47-137">0</span><span class="sxs-lookup"><span data-stu-id="2ff47-137">0</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-138">Réussite.</span><span class="sxs-lookup"><span data-stu-id="2ff47-138">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-139">1</span><span class="sxs-lookup"><span data-stu-id="2ff47-139">1</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-140">format d’argument incorrect</span><span class="sxs-lookup"><span data-stu-id="2ff47-140">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-141">2</span><span class="sxs-lookup"><span data-stu-id="2ff47-141">2</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-142">valeur d’argument incorrecte</span><span class="sxs-lookup"><span data-stu-id="2ff47-142">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-143">3</span><span class="sxs-lookup"><span data-stu-id="2ff47-143">3</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-144">erreur d’ouverture de ressource (Socket)</span><span class="sxs-lookup"><span data-stu-id="2ff47-144">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-145">4</span><span class="sxs-lookup"><span data-stu-id="2ff47-145">4</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-146">erreur de persistance (écriture de fichier)</span><span class="sxs-lookup"><span data-stu-id="2ff47-146">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="2ff47-147">5</span><span class="sxs-lookup"><span data-stu-id="2ff47-147">5</span></span>
</dt> <dd>

<span data-ttu-id="2ff47-148">erreur d’atomicité (l’ancien horodatage ne correspond pas)</span><span class="sxs-lookup"><span data-stu-id="2ff47-148">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff47-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ff47-149">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="2ff47-150">0</span><span class="sxs-lookup"><span data-stu-id="2ff47-150">0</span></span>

<span data-ttu-id="2ff47-151">Échec</span><span class="sxs-lookup"><span data-stu-id="2ff47-151">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2ff47-152">1</span><span class="sxs-lookup"><span data-stu-id="2ff47-152">1</span></span>

<span data-ttu-id="2ff47-153">Succès</span><span class="sxs-lookup"><span data-stu-id="2ff47-153">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ff47-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ff47-154">Requirements</span></span>



| <span data-ttu-id="2ff47-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ff47-155">Requirement</span></span> | <span data-ttu-id="2ff47-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ff47-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff47-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ff47-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff47-158">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ff47-158">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2ff47-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ff47-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff47-160">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2ff47-160">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="2ff47-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ff47-161">Namespace</span></span><br/>                | <span data-ttu-id="2ff47-162">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="2ff47-162">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="2ff47-163">MOF</span><span class="sxs-lookup"><span data-stu-id="2ff47-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ff47-164"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ff47-164"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ff47-165">DLL</span><span class="sxs-lookup"><span data-stu-id="2ff47-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ff47-166"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2ff47-166"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2ff47-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ff47-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff47-168">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="2ff47-168">**Control**</span></span>](control.md)
</dt> </dl>

 


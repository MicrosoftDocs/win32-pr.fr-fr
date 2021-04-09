---
description: Si la configuration actuelle est un résultat de l’opération d’annulation/de rétablissement/restauration, le marque comme s’il avait été défini explicitement, afin que l’historique conserve l’heure à laquelle il a été défini, et un fichier de sauvegarde sera créé pour celui-ci lors de la prochaine modification de configuration.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Méthode Checkpoint de la classe Control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110063"
---
# <a name="checkpoint-method-of-the-control-class"></a><span data-ttu-id="d6e32-103">Méthode Checkpoint de la classe Control</span><span class="sxs-lookup"><span data-stu-id="d6e32-103">Checkpoint method of the Control class</span></span>

<span data-ttu-id="d6e32-104">Si la configuration actuelle est un résultat de l’opération d’annulation/de rétablissement/restauration, le marque comme s’il avait été défini explicitement, afin que l’historique conserve l’heure à laquelle il a été défini, et un fichier de sauvegarde sera créé pour celui-ci lors de la prochaine modification de configuration.</span><span class="sxs-lookup"><span data-stu-id="d6e32-104">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="d6e32-105">Si la configuration actuelle a déjà été définie explicitement, n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="d6e32-105">If the current configuration was already set explicitly, has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e32-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6e32-106">Syntax</span></span>


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="d6e32-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6e32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e32-108">*OldTimestampLow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6e32-108">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-109">Horodatage de la définition de la configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="d6e32-109">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="d6e32-110">Si la valeur est égale à 0, active la vérification de l’atomicité : l’action sera appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c’est-à-dire que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="d6e32-110">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="d6e32-111">Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="d6e32-111">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-112">*OldTimestampHigh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6e32-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-113">Horodatage de la définition de la configuration actuelle.</span><span class="sxs-lookup"><span data-stu-id="d6e32-113">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="d6e32-114">Si la valeur est égale à 0, active la vérification de l’atomicité : l’action sera appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c’est-à-dire que la configuration n’a pas été modifiée dans between).</span><span class="sxs-lookup"><span data-stu-id="d6e32-114">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="d6e32-115">Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="d6e32-115">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-116">*ErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6e32-116">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-117">Chaîne de texte avec une explication de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d6e32-117">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-118">*WarningString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6e32-118">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-119">Chaîne de texte avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="d6e32-119">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-120">*InfoString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6e32-120">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-121">Chaîne de texte contenant des informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="d6e32-121">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-122">*ErrorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6e32-122">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-123">Type de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="d6e32-123">The type of the error.</span></span> <span data-ttu-id="d6e32-124">Notez que 0 ou absent indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="d6e32-124">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="d6e32-125">0</span><span class="sxs-lookup"><span data-stu-id="d6e32-125">0</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-126">Réussite.</span><span class="sxs-lookup"><span data-stu-id="d6e32-126">Success.</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-127">1</span><span class="sxs-lookup"><span data-stu-id="d6e32-127">1</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-128">format d’argument incorrect</span><span class="sxs-lookup"><span data-stu-id="d6e32-128">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-129">2</span><span class="sxs-lookup"><span data-stu-id="d6e32-129">2</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-130">valeur d’argument incorrecte</span><span class="sxs-lookup"><span data-stu-id="d6e32-130">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-131">3</span><span class="sxs-lookup"><span data-stu-id="d6e32-131">3</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-132">erreur d’ouverture de ressource (Socket)</span><span class="sxs-lookup"><span data-stu-id="d6e32-132">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-133">4</span><span class="sxs-lookup"><span data-stu-id="d6e32-133">4</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-134">erreur de persistance (écriture de fichier)</span><span class="sxs-lookup"><span data-stu-id="d6e32-134">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="d6e32-135">5</span><span class="sxs-lookup"><span data-stu-id="d6e32-135">5</span></span>
</dt> <dd>

<span data-ttu-id="d6e32-136">erreur d’atomicité (l’ancien horodatage ne correspond pas)</span><span class="sxs-lookup"><span data-stu-id="d6e32-136">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e32-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6e32-137">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="d6e32-138">0</span><span class="sxs-lookup"><span data-stu-id="d6e32-138">0</span></span>

<span data-ttu-id="d6e32-139">Échec</span><span class="sxs-lookup"><span data-stu-id="d6e32-139">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d6e32-140">1</span><span class="sxs-lookup"><span data-stu-id="d6e32-140">1</span></span>

<span data-ttu-id="d6e32-141">Succès</span><span class="sxs-lookup"><span data-stu-id="d6e32-141">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6e32-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6e32-142">Requirements</span></span>



| <span data-ttu-id="d6e32-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6e32-143">Requirement</span></span> | <span data-ttu-id="d6e32-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6e32-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e32-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6e32-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e32-146">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6e32-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d6e32-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6e32-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e32-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d6e32-148">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="d6e32-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d6e32-149">Namespace</span></span><br/>                | <span data-ttu-id="d6e32-150">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="d6e32-150">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="d6e32-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6e32-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e32-152"><dt>Srrestoreptapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e32-152"><dt>Srrestoreptapi.h</dt></span></span> </dl>          |
| <span data-ttu-id="d6e32-153">MOF</span><span class="sxs-lookup"><span data-stu-id="d6e32-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6e32-154"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6e32-154"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6e32-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d6e32-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6e32-156"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6e32-156"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="d6e32-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6e32-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e32-158">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="d6e32-158">**Control**</span></span>](control.md)
</dt> </dl>

 


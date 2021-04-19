---
title: MpThreatOpen, fonction (MpClient. h)
description: Retourne un handle d’énumération à des fins de récupération des menaces.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpThreatOpen
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513784"
---
# <a name="mpthreatopen-function"></a><span data-ttu-id="5d2f6-104">MpThreatOpen fonction)</span><span class="sxs-lookup"><span data-stu-id="5d2f6-104">MpThreatOpen function</span></span>

<span data-ttu-id="5d2f6-105">Retourne un handle d’énumération à des fins de récupération des menaces.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-105">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="5d2f6-106">Cette fonction peut être utilisée pour ouvrir les menaces détectées par une analyse spécifique, toutes les menaces actives dans le système, l’historique de la désinfection des menaces ou toutes les menaces présentes dans la base de données de signature.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-106">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d2f6-107">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a><span data-ttu-id="5d2f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d2f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2f6-109">*hScanHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d2f6-109">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2f6-110">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="5d2f6-111">Peut être un handle vers une opération d’analyse terminée, retourné par la fonction [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f6-111">Can be a handle to a completed scan operation, returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="5d2f6-112">Ce paramètre peut également être défini sur le descripteur de l’interface du gestionnaire de protection contre les programmes malveillants renvoyé par [**MpManagerOpen**](mpmanageropen.md) pour énumérer toutes les menaces actives dans le système, l’historique de la désinfection des menaces ou les menaces provenant de la base de données de signatures.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-112">Alternately, this parameter can be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) to enumerate all active threats in the system, the history of threat disinfection, or threats from signature database.</span></span>

</dd> <dt>

<span data-ttu-id="5d2f6-113">*ThreatSource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d2f6-113">*ThreatSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2f6-114">Type : **MPTHREAT \_ source**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-114">Type: **MPTHREAT\_SOURCE**</span></span>

<span data-ttu-id="5d2f6-115">Utilisé pour contrôler la source de l’énumération des menaces.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-115">Used to control the source of threat enumeration.</span></span> <span data-ttu-id="5d2f6-116">Les valeurs possibles pour ce paramètre sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d2f6-116">The possible values for this parameter are:</span></span>



| <span data-ttu-id="5d2f6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d2f6-117">Value</span></span>                                                                                                                                                                                                 | <span data-ttu-id="5d2f6-118">Signification</span><span class="sxs-lookup"><span data-stu-id="5d2f6-118">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <span data-ttu-id="5d2f6-119"><dt>**analyse de la \_ source MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-119"><dt>**MPTHREAT\_SOURCE\_SCAN**</dt></span></span> </dl>                   | <span data-ttu-id="5d2f6-120">Menaces associées au descripteur de numérisation spécifique.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-120">Threats that are associated with the specific scan handle.</span></span><br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <span data-ttu-id="5d2f6-121"><dt>**\_source MPTHREAT \_ active**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-121"><dt>**MPTHREAT\_SOURCE\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="5d2f6-122">Les menaces qui sont actuellement actives dans le système.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-122">Threats that are currently active in the system.</span></span><br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <span data-ttu-id="5d2f6-123"><dt>**historique de la \_ source MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-123"><dt>**MPTHREAT\_SOURCE\_HISTORY**</dt></span></span> </dl>          | <span data-ttu-id="5d2f6-124">Menaces qui sont traitées et conservées en tant qu’historique.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-124">Threats that are acted upon and preserved as a history.</span></span><br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <span data-ttu-id="5d2f6-125"><dt>**mise en quarantaine de la \_ source MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-125"><dt>**MPTHREAT\_SOURCE\_QUARANTINE**</dt></span></span> </dl> | <span data-ttu-id="5d2f6-126">Menaces mises en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-126">Threats that are quarantined.</span></span><br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <span data-ttu-id="5d2f6-127"><dt>**\_signature source \_ MPTHREAT**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-127"><dt>**MPTHREAT\_SOURCE\_SIGNATURE**</dt></span></span> </dl>    | <span data-ttu-id="5d2f6-128">Menaces pouvant être détectées avec la base de données de signature actuelle.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-128">Threats that are possible to detect with the current signature database.</span></span><br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <span data-ttu-id="5d2f6-129"><dt>**État de la \_ source MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-129"><dt>**MPTHREAT\_SOURCE\_STATE**</dt></span></span> </dl>                | <span data-ttu-id="5d2f6-130">Menaces qui ont été traitées récemment.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-130">Threats that have been acted upon recently.</span></span> <span data-ttu-id="5d2f6-131">(« Récemment » est défini par un paramètre interne configurable.)</span><span class="sxs-lookup"><span data-stu-id="5d2f6-131">("Recently" is defined by a configurable internal setting.)</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5d2f6-132">*ThreatType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d2f6-132">*ThreatType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2f6-133">Type : **MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-133">Type: **MPTHREAT\_TYPE**</span></span>

<span data-ttu-id="5d2f6-134">Utilisé pour filtrer les menaces énumérées en fonction du type de détection.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-134">Used to filter enumerated threats based on the detection type.</span></span> <span data-ttu-id="5d2f6-135">Les valeurs possibles pour ce paramètre sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d2f6-135">The possible values for this parameter are:</span></span>



| <span data-ttu-id="5d2f6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d2f6-136">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="5d2f6-137">Signification</span><span class="sxs-lookup"><span data-stu-id="5d2f6-137">Meaning</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <span data-ttu-id="5d2f6-138"><dt>**MPTHREAT \_ type \_ KNOWNBAD**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-138"><dt>**MPTHREAT\_TYPE\_KNOWNBAD**</dt></span></span> </dl>       | <span data-ttu-id="5d2f6-139">La détection est effectuée sur la base d’une signature spécifique, d’une émulation ou d’une autre méthode de détection des menaces.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-139">Detection is performed based on a specific signature, emulation, or other threat detection method.</span></span><br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <span data-ttu-id="5d2f6-140"><dt>**TYPE de MPTHREAT \_ \_ suspect**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-140"><dt>**MPTHREAT\_TYPE\_SUSPICIOUS**</dt></span></span> </dl> | <span data-ttu-id="5d2f6-141">La détection est effectuée en fonction de l’analyse du comportement.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-141">Detection is performed based on behavior monitoring.</span></span><br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <span data-ttu-id="5d2f6-142"><dt>**\_type MPTHREAT \_ inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-142"><dt>**MPTHREAT\_TYPE\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="5d2f6-143">La détection est effectuée en fonction de menaces inconnues (non classifiées).</span><span class="sxs-lookup"><span data-stu-id="5d2f6-143">Detection is performed based on unknown threats (unclassified).</span></span><br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <span data-ttu-id="5d2f6-144"><dt>**MPTHREAT \_ type \_ KNOWNGOOD**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-144"><dt>**MPTHREAT\_TYPE\_KNOWNGOOD**</dt></span></span> </dl>    | <span data-ttu-id="5d2f6-145">La détection est effectuée sur la base de menaces connues.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-145">Detection is performed based on known safe threats.</span></span><br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <span data-ttu-id="5d2f6-146"><dt>**MPTHREAT \_ type \_ NIS**</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-146"><dt>**MPTHREAT\_TYPE\_NIS**</dt></span></span> </dl>                      | <span data-ttu-id="5d2f6-147">La détection est effectuée en fonction des menaces NIS.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-147">Detection is performed based on NIS threats.</span></span><br/>                                                       |



 

</dd> <dt>

<span data-ttu-id="5d2f6-148">*phThreatEnumHandle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5d2f6-148">*phThreatEnumHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2f6-149">Type : **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-149">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="5d2f6-150">Descripteur d’énumération des menaces retourné qui identifie le contexte de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-150">Returned threat enumeration handle which identifies the enumeration context.</span></span> <span data-ttu-id="5d2f6-151">Ce descripteur peut être utilisé pour énumérer les informations sur les menaces à l’aide de [**MpThreatEnumerate**](mpthreatenumerate.md).</span><span class="sxs-lookup"><span data-stu-id="5d2f6-151">This handle can be used to enumerate threat information using [**MpThreatEnumerate**](mpthreatenumerate.md).</span></span> <span data-ttu-id="5d2f6-152">Le descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2f6-152">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2f6-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d2f6-153">Return value</span></span>

<span data-ttu-id="5d2f6-154">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-154">Type: **HRESULT**</span></span>

<span data-ttu-id="5d2f6-155">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-155">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="5d2f6-156">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-156">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="5d2f6-157">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5d2f6-157">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2f6-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d2f6-158">Requirements</span></span>



| <span data-ttu-id="5d2f6-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d2f6-159">Requirement</span></span> | <span data-ttu-id="5d2f6-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d2f6-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2f6-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d2f6-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2f6-162">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d2f6-162">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5d2f6-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d2f6-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2f6-164">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d2f6-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d2f6-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d2f6-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d2f6-166"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-166"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d2f6-167">DLL</span><span class="sxs-lookup"><span data-stu-id="5d2f6-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d2f6-168"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d2f6-168"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2f6-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d2f6-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2f6-170">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-170">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="5d2f6-171">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-171">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="5d2f6-172">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-172">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="5d2f6-173">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-173">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="5d2f6-174">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="5d2f6-174">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> </dl>

 

 






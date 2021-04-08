---
description: La méthode Connect connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration sur la connexion.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: 'IESP :: Connect, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4fc9c88b0eb4671c61f268c5857dceba3dc500f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112214"
---
# <a name="iespconnect-method"></a><span data-ttu-id="a0588-103">IESP :: Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="a0588-103">IESP::Connect method</span></span>

<span data-ttu-id="a0588-104">La méthode **Connect** connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="a0588-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0588-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0588-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="a0588-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0588-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0588-107">*hInputBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0588-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-108">Handle vers l’objet BLOB qui spécifie la carte réseau à laquelle le NPP se connecte et les informations de configuration pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="a0588-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="a0588-109">*StatusCallbackProc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0588-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-110">Adresse de la fonction de rappel de l’utilisateur, qui reçoit les mises à jour d’État, telles que les déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="a0588-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="a0588-111">Si aucune fonction de rappel n’est utilisée, définissez ce paramètre et le paramètre *userContext* sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a0588-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0588-112">*UserContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0588-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-113">Valeur passée lorsque la fonction de rappel de l’utilisateur est appelée.</span><span class="sxs-lookup"><span data-stu-id="a0588-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="a0588-114">La valeur de ce paramètre est généralement HWND ou un pointeur’This'.</span><span class="sxs-lookup"><span data-stu-id="a0588-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="a0588-115">Si aucune fonction de rappel n’est spécifiée, affectez la valeur **null** à ce paramètre et au paramètre *StatusCallbackProc* .</span><span class="sxs-lookup"><span data-stu-id="a0588-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0588-116">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a0588-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0588-117">Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a0588-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0588-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0588-118">Return value</span></span>

<span data-ttu-id="a0588-119">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a0588-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a0588-120">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants (qui incluent les erreurs retournées par l’appel Internal **IESP :: configure** ) :</span><span class="sxs-lookup"><span data-stu-id="a0588-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IESP::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0588-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a0588-121">Return code</span></span></th>
<th><span data-ttu-id="a0588-122">Description</span><span class="sxs-lookup"><span data-stu-id="a0588-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="a0588-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-124">Cette instance de l’objet COM NPP est déjà connectée au réseau.</span><span class="sxs-lookup"><span data-stu-id="a0588-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a0588-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-126">L’objet BLOB de configuration est endommagé.</span><span class="sxs-lookup"><span data-stu-id="a0588-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="a0588-127">Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-127">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a0588-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-129">L’objet BLOB d’entrée spécifié par le paramètre <em>hInputBlob</em> n’a pas d’entrée nécessaire pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="a0588-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="a0588-130">Cette erreur peut être générée par l’appel de <strong>IESP :: Connect</strong> ou <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-130">This error might be generated by the <strong>IESP::Connect</strong> or <strong>IESP::Configure</strong> call.</span></span> <span data-ttu-id="a0588-131">Examinez l’objet BLOB d’erreur retourné par <em>hErrorBlob</em> pour déterminer quelle entrée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a0588-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a0588-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-133">La fonction <strong>CreateBlob</strong> n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="a0588-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="a0588-134">Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-134">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a0588-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-136">La chaîne ne se termine pas par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="a0588-136">The string is not null-terminated.</span></span> <span data-ttu-id="a0588-137">Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-137">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a0588-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-139">La partie déclencheur de l’objet BLOB d’entrée est endommagée.</span><span class="sxs-lookup"><span data-stu-id="a0588-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="a0588-140">Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-140">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a0588-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-142">L’objet spécifié dans <em>hInputBlob</em> n’est pas un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="a0588-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="a0588-143">Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-143">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a0588-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-145">Le répertoire de capture par défaut n’a pas été défini dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a0588-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="a0588-146">Utilisez le chemin d’accès suivant pour définir le répertoire de capture.</span><span class="sxs-lookup"><span data-stu-id="a0588-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a0588-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-148">La mémoire nécessaire pour effectuer cette opération n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a0588-148">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="a0588-149">Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-149">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="a0588-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-151">Le délai d’attente de la demande a expiré. Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-151">The request has timed out. This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="a0588-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a0588-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="a0588-153">Le numéro de version de l’objet BLOB spécifié dans <em>hInputBlob</em> est incorrect.</span><span class="sxs-lookup"><span data-stu-id="a0588-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="a0588-154">Cette erreur est générée par l’appel de <strong>IESP :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="a0588-154">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a0588-155">Notes</span><span class="sxs-lookup"><span data-stu-id="a0588-155">Remarks</span></span>

<span data-ttu-id="a0588-156">Lorsque la méthode **Connect** est appelée, moniteur réseau appelle automatiquement **IESP :: configure** à l’aide de l’objet BLOB fourni par le paramètre *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="a0588-156">When the **Connect** method is called, Network Monitor automatically calls **IESP::Configure** by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="a0588-157">Notez que les codes d’erreur retournés par l’appel à **IESP :: configure** sont passés en retour et retournés par l’appel de **IESP :: Connect** .</span><span class="sxs-lookup"><span data-stu-id="a0588-157">Note that any error codes returned by the call to **IESP::Configure** are passed back and returned by the **IESP::Connect** call.</span></span>

<span data-ttu-id="a0588-158">Cette méthode doit être appelée avant que vous ne puissiez commencer à capturer des frames.</span><span class="sxs-lookup"><span data-stu-id="a0588-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="a0588-159">Notez que lorsque vous vous connectez au réseau à l’aide de cette méthode, vous devez continuer à utiliser l’interface **IESP** pour capturer des frames.</span><span class="sxs-lookup"><span data-stu-id="a0588-159">Note that when you connect to the network by using this method, you must continue to use the **IESP** interface to capture frames.</span></span>

<span data-ttu-id="a0588-160">L’objet BLOB d’entrée spécifié par *hInputBlob* peut être obtenu en appelant **GetNPPBlobFromUI**, **GetNPPBlobTable** et **SelectNPPBlobFromTable**.</span><span class="sxs-lookup"><span data-stu-id="a0588-160">The input BLOB specified by *hInputBlob* can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="a0588-161">L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob d’entrée spécifié dans *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="a0588-161">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="a0588-162">L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="a0588-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="a0588-163">Par exemple, si l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée que Moniteur réseau n’a pas pu trouver est incluse dans l’objet blob d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="a0588-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="a0588-164">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="a0588-164">For information about</span></span>                          | <span data-ttu-id="a0588-165">Consultez</span><span class="sxs-lookup"><span data-stu-id="a0588-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a0588-166">Obtention de l’objet BLOB d’entrée qui représente une carte réseau</span><span class="sxs-lookup"><span data-stu-id="a0588-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="a0588-167">Sélection d’une carte d’interface réseau</span><span class="sxs-lookup"><span data-stu-id="a0588-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="a0588-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0588-168">Requirements</span></span>



| <span data-ttu-id="a0588-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0588-169">Requirement</span></span> | <span data-ttu-id="a0588-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0588-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0588-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0588-171">Minimum supported client</span></span><br/> | <span data-ttu-id="a0588-172">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0588-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a0588-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0588-173">Minimum supported server</span></span><br/> | <span data-ttu-id="a0588-174">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0588-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a0588-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0588-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0588-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0588-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a0588-177">DLL</span><span class="sxs-lookup"><span data-stu-id="a0588-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0588-178"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0588-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0588-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0588-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0588-180">IESP</span><span class="sxs-lookup"><span data-stu-id="a0588-180">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="a0588-181">IESP :: configure</span><span class="sxs-lookup"><span data-stu-id="a0588-181">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="a0588-182">IESP ::D éconnecter</span><span class="sxs-lookup"><span data-stu-id="a0588-182">IESP::Disconnect</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="a0588-183">IESP :: Start</span><span class="sxs-lookup"><span data-stu-id="a0588-183">IESP::Start</span></span>](iesp-start.md)
</dt> </dl>

 

 





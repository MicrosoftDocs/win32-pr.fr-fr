---
description: 'Méthode IStats :: Connect : la méthode Connect connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'IStats :: Connect, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0719b6ff56aaa8c0be02f86d62ac23d4003aa3d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098477"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="d2034-103">IStats :: Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="d2034-103">IStats::Connect method</span></span>

<span data-ttu-id="d2034-104">La méthode **Connect** connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="d2034-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2034-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2034-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d2034-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2034-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2034-107">*hInputBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2034-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2034-108">Handle vers l’objet BLOB qui spécifie la carte réseau à laquelle le NPP se connecte et les informations de configuration pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="d2034-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="d2034-109">*StatusCallbackProc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2034-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2034-110">Adresse de la fonction de rappel de l’utilisateur, qui reçoit les mises à jour d’État, telles que les déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="d2034-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="d2034-111">Si aucune fonction de rappel n’est utilisée, définissez ce paramètre et le paramètre *userContext* sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d2034-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2034-112">*UserContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2034-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2034-113">Valeur passée lorsque la fonction de rappel de l’utilisateur est appelée.</span><span class="sxs-lookup"><span data-stu-id="d2034-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="d2034-114">La valeur de ce paramètre est généralement HWND ou un pointeur’This'.</span><span class="sxs-lookup"><span data-stu-id="d2034-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="d2034-115">Si aucune fonction de rappel n’est spécifiée, affectez la valeur **null** à ce paramètre et au paramètre *StatusCallbackProc* .</span><span class="sxs-lookup"><span data-stu-id="d2034-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d2034-116">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d2034-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2034-117">Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d2034-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2034-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2034-118">Return value</span></span>

<span data-ttu-id="d2034-119">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d2034-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d2034-120">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants (qui incluent les erreurs retournées par l’appel Internal **IStats :: configure** ) :</span><span class="sxs-lookup"><span data-stu-id="d2034-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2034-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d2034-121">Return code</span></span></th>
<th><span data-ttu-id="d2034-122">Description</span><span class="sxs-lookup"><span data-stu-id="d2034-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="d2034-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-124">Cette instance de l’objet COM NPP est déjà connectée au réseau.</span><span class="sxs-lookup"><span data-stu-id="d2034-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d2034-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-126">L’objet BLOB de configuration est endommagé.</span><span class="sxs-lookup"><span data-stu-id="d2034-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="d2034-127">Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d2034-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-129">L’objet BLOB d’entrée spécifié par le paramètre <em>hInputBlob</em> n’a pas d’entrée nécessaire pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="d2034-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="d2034-130">Cette erreur peut être générée par l’appel de <strong>IStats :: Connect</strong> ou <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="d2034-131">Examinez l’objet BLOB d’erreur retourné par <em>hErrorBlob</em> pour déterminer quelle entrée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="d2034-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d2034-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-133">La fonction <strong>CreateBlob</strong> n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="d2034-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="d2034-134">Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d2034-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-136">La chaîne ne se termine pas par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="d2034-136">The string is not null-terminated.</span></span> <span data-ttu-id="d2034-137">Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d2034-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-139">La partie déclencheur de l’objet BLOB d’entrée est endommagée.</span><span class="sxs-lookup"><span data-stu-id="d2034-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="d2034-140">Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d2034-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-142">L’objet spécifié dans <em>hInputBlob</em> n’est pas un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="d2034-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="d2034-143">Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d2034-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-145">Le répertoire de capture par défaut n’a pas été défini dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d2034-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="d2034-146">Pour définir le répertoire de capture, utilisez le chemin d’accès suivant.</span><span class="sxs-lookup"><span data-stu-id="d2034-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d2034-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-148">La mémoire requise pour effectuer cette opération n’était pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d2034-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="d2034-149">Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="d2034-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-151">Le délai d’attente de la demande a expiré. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="d2034-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="d2034-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="d2034-153">Le numéro de version de l’objet BLOB spécifié dans <em>hInputBlob</em> est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d2034-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="d2034-154">Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .</span><span class="sxs-lookup"><span data-stu-id="d2034-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d2034-155">Notes </span><span class="sxs-lookup"><span data-stu-id="d2034-155">Remarks</span></span>

<span data-ttu-id="d2034-156">Lorsque la méthode **Connect** est appelée, moniteur réseau appelle automatiquement la méthode **IStats :: configure** à l’aide de l’objet BLOB fourni par le paramètre *hInputBlob* .</span><span class="sxs-lookup"><span data-stu-id="d2034-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="d2034-157">Notez que les codes d’erreur retournés par l’appel à **IStats :: configure** sont passés en retour et retournés par l’appel de **IStats :: Connect** .</span><span class="sxs-lookup"><span data-stu-id="d2034-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="d2034-158">Cette méthode doit être appelée avant que vous ne puissiez commencer à capturer des frames.</span><span class="sxs-lookup"><span data-stu-id="d2034-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="d2034-159">Notez que lorsque vous vous connectez au réseau à l’aide de cette méthode, vous devez continuer à utiliser l’interface **IStats** pour capturer des frames.</span><span class="sxs-lookup"><span data-stu-id="d2034-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="d2034-160">L’objet BLOB d’entrée spécifié par *hInputBlob* peut être obtenu en appelant les méthodes **GetNPPBlobFromUI**, **GetNPPBlobTable** et **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="d2034-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="d2034-161">L’objet BLOB d’erreur retourné par le paramètre *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob d’entrée spécifié dans *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="d2034-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="d2034-162">L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="d2034-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="d2034-163">Par exemple, si l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée que Moniteur réseau n’a pas pu trouver est incluse dans l’objet blob d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="d2034-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="d2034-164">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="d2034-164">For information about</span></span>                                             | <span data-ttu-id="d2034-165">Consultez</span><span class="sxs-lookup"><span data-stu-id="d2034-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d2034-166">Obtention de l’objet BLOB d’entrée qui représente une carte d’interface réseau</span><span class="sxs-lookup"><span data-stu-id="d2034-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="d2034-167">Sélection d’une carte d’interface réseau</span><span class="sxs-lookup"><span data-stu-id="d2034-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="d2034-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2034-168">Requirements</span></span>



| <span data-ttu-id="d2034-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2034-169">Requirement</span></span> | <span data-ttu-id="d2034-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2034-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2034-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2034-171">Minimum supported client</span></span><br/> | <span data-ttu-id="d2034-172">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2034-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d2034-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2034-173">Minimum supported server</span></span><br/> | <span data-ttu-id="d2034-174">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2034-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d2034-175">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2034-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2034-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2034-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d2034-177">DLL</span><span class="sxs-lookup"><span data-stu-id="d2034-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2034-178"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2034-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2034-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2034-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2034-180">IStats</span><span class="sxs-lookup"><span data-stu-id="d2034-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="d2034-181">IStats :: configure</span><span class="sxs-lookup"><span data-stu-id="d2034-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="d2034-182">IStats ::D éconnecter</span><span class="sxs-lookup"><span data-stu-id="d2034-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="d2034-183">OBJETS BLOB Moniteur réseau</span><span class="sxs-lookup"><span data-stu-id="d2034-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 





---
description: La méthode Connect connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'IRTC :: Connect, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536113"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="a5416-103">IRTC :: Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="a5416-103">IRTC::Connect method</span></span>

<span data-ttu-id="a5416-104">La méthode **Connect** connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="a5416-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5416-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5416-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="a5416-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5416-107">*hInputBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5416-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5416-108">Handle vers l’objet BLOB qui spécifie la carte réseau à laquelle vous vous connectez et les informations de configuration pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="a5416-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="a5416-109">*StatusCallbackProc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5416-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5416-110">Adresse de la fonction de rappel d’état de l’utilisateur, qui reçoit les mises à jour d’État, telles que les déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="a5416-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="a5416-111">Ce paramètre peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="a5416-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a5416-112">*FramesCallbackProc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5416-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5416-113">Adresse de la fonction de rappel de frame de l’utilisateur, qui est utilisée pour recevoir des mises à jour d’État, telles que les déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="a5416-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="a5416-114">Ce paramètre peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="a5416-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a5416-115">*UserContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a5416-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5416-116">Valeur passée lorsque l’état de l’utilisateur et la fonction de rappel de frame sont appelés.</span><span class="sxs-lookup"><span data-stu-id="a5416-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="a5416-117">Si les deux fonctions de rappel sont spécifiées, elles doivent utiliser la même valeur de contexte utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5416-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="a5416-118">La valeur de ce paramètre est généralement HWND ou un pointeur’This'.</span><span class="sxs-lookup"><span data-stu-id="a5416-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="a5416-119">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a5416-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5416-120">Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a5416-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="a5416-121">Pour plus d’informations sur ce qui se trouve dans l’objet BLOB d’erreurs, consultez la section Notes en bas de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a5416-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5416-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5416-122">Return value</span></span>

<span data-ttu-id="a5416-123">Si cette méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a5416-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a5416-124">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants (qui incluent les erreurs retournées par l’appel Internal **IRTC :: configure** ) :</span><span class="sxs-lookup"><span data-stu-id="a5416-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="a5416-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a5416-125">Return code</span></span>                                                                                                         | <span data-ttu-id="a5416-126">Description</span><span class="sxs-lookup"><span data-stu-id="a5416-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5416-127"><dt>**NMERR \_ déjà \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="a5416-128">Cette instance de l’objet COM NPP est déjà connectée au réseau.</span><span class="sxs-lookup"><span data-stu-id="a5416-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="a5416-129"><dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="a5416-130">L’objet BLOB de configuration est endommagé.</span><span class="sxs-lookup"><span data-stu-id="a5416-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="a5416-131">Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="a5416-132"><dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="a5416-133">L’objet BLOB d’entrée spécifié par le paramètre *hInputBlob* n’a pas d’entrée nécessaire pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="a5416-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="a5416-134">Cette erreur peut être générée par l’appel de **IRTC :: Connect** ou **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="a5416-135">Examinez l’objet BLOB d’erreur retourné par *hErrorBlob* pour déterminer quelle entrée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a5416-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="a5416-136"><dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="a5416-137">La fonction **CreateBlob** n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="a5416-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="a5416-138">Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="a5416-139"><dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="a5416-140">La chaîne ne se termine pas par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="a5416-140">The string is not null-terminated.</span></span> <span data-ttu-id="a5416-141">Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="a5416-142"><dt>**\_déclencheur NMERR non conforme \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="a5416-143">La partie déclencheur de l’objet BLOB d’entrée est endommagée.</span><span class="sxs-lookup"><span data-stu-id="a5416-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="a5416-144">Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="a5416-145"><dt>**NMERR \_ \_ objet blob non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="a5416-146">L’objet spécifié dans *hInputBlob* n’est pas un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="a5416-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="a5416-147">Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="a5416-148"><dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="a5416-149">La mémoire nécessaire pour effectuer cette opération n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a5416-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="a5416-150">Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="a5416-151"><dt>**\_délai d’expiration de NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="a5416-152">Le délai d’attente de la demande a expiré. Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="a5416-153"><dt>**NMERR \_ objet blob de niveau supérieur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="a5416-154">Le numéro de version de l’objet BLOB spécifié dans *hInputBlob* est incorrect.</span><span class="sxs-lookup"><span data-stu-id="a5416-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="a5416-155">Cette erreur est générée par l’appel de **IRTC :: configure** .</span><span class="sxs-lookup"><span data-stu-id="a5416-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="a5416-156">Notes</span><span class="sxs-lookup"><span data-stu-id="a5416-156">Remarks</span></span>

<span data-ttu-id="a5416-157">Lorsque la méthode **Connect** est appelée, le NPP appelle automatiquement la méthode **IRTC :: configure** à l’aide de l’objet BLOB fourni par *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="a5416-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="a5416-158">Notez que les codes d’erreur retournés par l’appel à **IRTC :: configure** sont passés en retour et retournés par l’appel de **IRTC :: Connect** .</span><span class="sxs-lookup"><span data-stu-id="a5416-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="a5416-159">Cette méthode doit être appelée avant que vous ne puissiez commencer à capturer des frames.</span><span class="sxs-lookup"><span data-stu-id="a5416-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="a5416-160">Notez que lorsque vous vous connectez au réseau à l’aide de cette méthode, vous devez continuer à utiliser l’interface **IRTC** pour capturer des frames.</span><span class="sxs-lookup"><span data-stu-id="a5416-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="a5416-161">Lorsque vous appelez cette fonction, vous devez spécifier une fonction de rappel d’État ou de frame, même si elle agit uniquement comme un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="a5416-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="a5416-162">L’objet BLOB d’entrée spécifié par *hInputBlob* peut être obtenu en appelant les méthodes **GetNPPBlobFromUI**, **GetNPPBlobTable** et **SelectNPPBlobFromTable** .</span><span class="sxs-lookup"><span data-stu-id="a5416-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="a5416-163">L’objet BLOB d’erreur retourné dans *hErrorBlob* contient des informations d’erreur que le développeur ou l’application peut utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="a5416-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="a5416-164">L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob d’entrée spécifié dans *hInputBlob*.</span><span class="sxs-lookup"><span data-stu-id="a5416-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="a5416-165">Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="a5416-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="a5416-166">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="a5416-166">For information about</span></span>                          | <span data-ttu-id="a5416-167">Consultez</span><span class="sxs-lookup"><span data-stu-id="a5416-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a5416-168">Obtention de l’objet BLOB d’entrée qui représente une carte réseau</span><span class="sxs-lookup"><span data-stu-id="a5416-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="a5416-169">Sélection d’une carte d’interface réseau</span><span class="sxs-lookup"><span data-stu-id="a5416-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="a5416-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5416-170">Requirements</span></span>



| <span data-ttu-id="a5416-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5416-171">Requirement</span></span> | <span data-ttu-id="a5416-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5416-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5416-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5416-173">Minimum supported client</span></span><br/> | <span data-ttu-id="a5416-174">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5416-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a5416-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5416-175">Minimum supported server</span></span><br/> | <span data-ttu-id="a5416-176">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5416-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a5416-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5416-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5416-178"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a5416-179">DLL</span><span class="sxs-lookup"><span data-stu-id="a5416-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5416-180"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5416-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5416-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5416-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5416-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="a5416-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="a5416-183">IRTC :: configure</span><span class="sxs-lookup"><span data-stu-id="a5416-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="a5416-184">IRTC ::D éconnecter</span><span class="sxs-lookup"><span data-stu-id="a5416-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="a5416-185">IRTC :: Start</span><span class="sxs-lookup"><span data-stu-id="a5416-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 





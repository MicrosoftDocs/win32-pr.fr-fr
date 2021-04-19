---
description: La méthode Configure envoie les informations de configuration utilisées pour une capture.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Méthode IDelaydCConfigure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484313"
---
# <a name="idelaydcconfigure-method"></a><span data-ttu-id="63c2f-103">IDelaydC :: configure, méthode</span><span class="sxs-lookup"><span data-stu-id="63c2f-103">IDelaydC::Configure method</span></span>

<span data-ttu-id="63c2f-104">La méthode **configure** envoie les informations de configuration utilisées pour une capture.</span><span class="sxs-lookup"><span data-stu-id="63c2f-104">The **Configure** method submits configuration information used for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c2f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63c2f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="63c2f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63c2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c2f-107">*hConfigurationBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63c2f-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c2f-108">Handle vers l’objet BLOB qui contient les informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="63c2f-108">Handle to the BLOB that contains the configuration information.</span></span>

</dd> <dt>

<span data-ttu-id="63c2f-109">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="63c2f-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63c2f-110">Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="63c2f-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="63c2f-111">Pour plus d’informations sur le contenu d’un objet BLOB d’erreur, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="63c2f-111">For information about the contents of an error BLOB, see the Remarks section in this topic .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c2f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63c2f-112">Return value</span></span>

<span data-ttu-id="63c2f-113">Si cette méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="63c2f-113">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="63c2f-114">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="63c2f-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="63c2f-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="63c2f-115">Return code</span></span>                                                                                                      | <span data-ttu-id="63c2f-116">Description</span><span class="sxs-lookup"><span data-stu-id="63c2f-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63c2f-117"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="63c2f-117"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                  | <span data-ttu-id="63c2f-118">Le NPP signale que la session de capture a démarré.</span><span class="sxs-lookup"><span data-stu-id="63c2f-118">The NPP reports that the capture session has started.</span></span><br/>                          |
| <dl> <span data-ttu-id="63c2f-119"><dt>**\_disque NMERR \_ non \_ local \_ fixe**</dt></span><span class="sxs-lookup"><span data-stu-id="63c2f-119"><dt>**NMERR\_DISK\_NOT\_LOCAL\_FIXED**</dt></span></span> </dl>    |                                                                                           |
| <dl> <span data-ttu-id="63c2f-120"><dt>**NMERR \_ n’a \_ pas pu \_ créer de \_ mémoire**</dt></span><span class="sxs-lookup"><span data-stu-id="63c2f-120"><dt>**NMERR\_COULD\_NOT\_CREATE\_MEMORY**</dt></span></span> </dl> |                                                                                           |
| <dl> <span data-ttu-id="63c2f-121"><dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="63c2f-121"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>            | <span data-ttu-id="63c2f-122">Aucune mémoire n’était disponible.</span><span class="sxs-lookup"><span data-stu-id="63c2f-122">No memory was available.</span></span> <span data-ttu-id="63c2f-123">Arrêtez Windows pour libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="63c2f-123">Shut down windows to free up resources.</span></span><br/>               |
| <dl> <span data-ttu-id="63c2f-124"><dt>**\_paramètre NMERR non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63c2f-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="63c2f-125">L’objet BLOB de configuration spécifié par le paramètre hConfiguration n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="63c2f-125">The configuration BLOB specified by the hConfiguration parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63c2f-126">Notes</span><span class="sxs-lookup"><span data-stu-id="63c2f-126">Remarks</span></span>

<span data-ttu-id="63c2f-127">Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré, arrêté, mais pas déconnecté.</span><span class="sxs-lookup"><span data-stu-id="63c2f-127">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="63c2f-128">L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans *hConfigurationBlob*.</span><span class="sxs-lookup"><span data-stu-id="63c2f-128">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="63c2f-129">L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="63c2f-129">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="63c2f-130">Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="63c2f-130">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="63c2f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63c2f-131">Requirements</span></span>



| <span data-ttu-id="63c2f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63c2f-132">Requirement</span></span> | <span data-ttu-id="63c2f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="63c2f-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c2f-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63c2f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="63c2f-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63c2f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="63c2f-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63c2f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="63c2f-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63c2f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="63c2f-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="63c2f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="63c2f-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="63c2f-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="63c2f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="63c2f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63c2f-141"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c2f-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c2f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63c2f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c2f-143">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="63c2f-143">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="63c2f-144">IDelaydC :: Connect</span><span class="sxs-lookup"><span data-stu-id="63c2f-144">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="63c2f-145">IDelaydC :: Start</span><span class="sxs-lookup"><span data-stu-id="63c2f-145">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="63c2f-146">IDelaydC :: Stop</span><span class="sxs-lookup"><span data-stu-id="63c2f-146">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 





---
description: Demande un point de terminaison utilisé pour se connecter à un service.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'IUpdateEndpointProvider :: GetServiceEndpoint, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536120"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a><span data-ttu-id="5e702-103">IUpdateEndpointProvider :: GetServiceEndpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="5e702-103">IUpdateEndpointProvider::GetServiceEndpoint method</span></span>

<span data-ttu-id="5e702-104">Demande un point de terminaison utilisé pour se connecter à un service.</span><span class="sxs-lookup"><span data-stu-id="5e702-104">Requests an endpoint that is used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e702-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e702-105">Syntax</span></span>


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a><span data-ttu-id="5e702-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e702-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e702-107">*ServiceId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e702-107">*ServiceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e702-108">Identifie le service à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="5e702-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="5e702-109">*endpointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e702-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e702-110">Identifie le type de point de terminaison implémenté par le service.</span><span class="sxs-lookup"><span data-stu-id="5e702-110">Identifies the type of endpoint implemented by the service.</span></span>

<span data-ttu-id="5e702-111">L’énumération [**UpdateEndpointType**](updateendpointtype.md) définit les constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e702-111">The [**UpdateEndpointType**](updateendpointtype.md) enumeration defines the following constants.</span></span>

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span data-ttu-id="5e702-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="5e702-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>


</dt> <dd>

<span data-ttu-id="5e702-113">Point de terminaison client-serveur utilisé pour se connecter au service de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5e702-113">A client-server endpoint that is used to connect to the update service.</span></span>

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span data-ttu-id="5e702-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="5e702-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>


</dt> <dd>

<span data-ttu-id="5e702-115">Point de terminaison de création de rapports utilisé lorsque le client signale les résultats des analyses, des téléchargements et des réinstallations dans le service de mise à jour</span><span class="sxs-lookup"><span data-stu-id="5e702-115">A Reporting endpoint that is used used when the client reports the results of scans, downloads, and installs back to the update service</span></span>

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span data-ttu-id="5e702-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="5e702-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>


</dt> <dd>

<span data-ttu-id="5e702-117">Point de terminaison de Self-Update utilisé lorsque l’ordinateur client contacte un service de mise à jour pour déterminer s’il existe une nouvelle version du logiciel client de l’agent Windows Update.</span><span class="sxs-lookup"><span data-stu-id="5e702-117">A Self-Update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span data-ttu-id="5e702-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="5e702-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>


</dt> <dd>

<span data-ttu-id="5e702-119">Point de terminaison de réglementation utilisé lorsque l’ordinateur client contacte le service de régulation pour agir sur une mise à jour particulière applicable à l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="5e702-119">A Regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span data-ttu-id="5e702-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="5e702-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>


</dt> <dd>

<span data-ttu-id="5e702-121">Simple-Targeting endoint utilisé uniquement avec les services privés (serveurs WSUS dans les environnements d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="5e702-121">A Simple-Targeting endoint that is used only with private services (WSUS servers in corporate environments).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e702-122">*proxySettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e702-122">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e702-123">Identifie les paramètres utilisés lors de la connexion à un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="5e702-123">Identifies the settings that are used when connecting to a proxy server.</span></span>

</dd> <dt>

<span data-ttu-id="5e702-124">*hUserToken* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e702-124">*hUserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e702-125">Contient un objet de handle de jeton qui représente l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5e702-125">Contains a token handle object that represents the user.</span></span> <span data-ttu-id="5e702-126">Le fournisseur de points de terminaison utilise ce jeton pour déterminer les paramètres de proxy et les informations d’identification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5e702-126">The endpoint provider uses this token to determine which proxy settings and credentials to use.</span></span>

</dd> <dt>

<span data-ttu-id="5e702-127">*fRefreshOnline* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e702-127">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e702-128">Indique que Weather WUA demande un nouveau jeton.</span><span class="sxs-lookup"><span data-stu-id="5e702-128">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="5e702-129">La valeur true indique qu’un nouveau jeton est demandé.</span><span class="sxs-lookup"><span data-stu-id="5e702-129">True indicates that a new token is requested.</span></span> <span data-ttu-id="5e702-130">False indique qu’un nouveau jeton ou un jeton mis en cache est demandé.</span><span class="sxs-lookup"><span data-stu-id="5e702-130">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="5e702-131">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5e702-131">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="5e702-132">*pbstrEndpointLoc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5e702-132">*pbstrEndpointLoc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e702-133">Spécifiez l’URL utilisée pour communiquer avec le service.</span><span class="sxs-lookup"><span data-stu-id="5e702-133">Specify the URL used to communicate with the service.</span></span> <span data-ttu-id="5e702-134">Par exemple, pour un point de terminaison sécurisés-Server, il s’agit de l’URL du service du serveur client.</span><span class="sxs-lookup"><span data-stu-id="5e702-134">For example, for a cleint-server endpoint this would be the URL to the client server service.</span></span> <span data-ttu-id="5e702-135">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5e702-135">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e702-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e702-136">Return value</span></span>

<span data-ttu-id="5e702-137">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="5e702-137">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="5e702-138">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="5e702-138">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e702-139">Notes</span><span class="sxs-lookup"><span data-stu-id="5e702-139">Remarks</span></span>

<span data-ttu-id="5e702-140">WUA affecte généralement la valeur false au paramètre *fRefreshOnline* lorsque cette méthode est appelée pour la première fois, puis, si une erreur de connexion se produit, WUA définit ce paramètre sur true lorsque la méthode est à nouveau appelée.</span><span class="sxs-lookup"><span data-stu-id="5e702-140">WUA typically sets the *fRefreshOnline* parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="5e702-141">Toutefois, l’implémentation de cette méthode peut demander un nouveau jeton auprès d’un service d’émission de jeton de sécurité (STS) ou fournir un jeton mis en cache à tout moment.</span><span class="sxs-lookup"><span data-stu-id="5e702-141">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

<span data-ttu-id="5e702-142">Si le point de terminaison n’a pas besoin d’authentification, l’appelant peut se connecter au service en utilisant uniquement l’URL spécifiée par le paramètre *pbstrEndpointLoc* .</span><span class="sxs-lookup"><span data-stu-id="5e702-142">If the endpoint does not need authentication, then the caller can connect to the service using only the URL specified by the *pbstrEndpointLoc* parameter.</span></span>

<span data-ttu-id="5e702-143">Si le point de terminaison a besoin d’une authentification, l’appelant peut utiliser l’URL spécifiée par le paramètre *pbstrEndpointLoc* et les données fournies par les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="5e702-143">If the endpoint does need authentication, then the caller can use the URL specified by the *pbstrEndpointLoc* parameter and the data provided by the other parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e702-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e702-144">Requirements</span></span>



| <span data-ttu-id="5e702-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e702-145">Requirement</span></span> | <span data-ttu-id="5e702-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e702-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e702-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e702-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5e702-148">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e702-148">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5e702-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e702-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5e702-150">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e702-150">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5e702-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e702-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e702-152"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e702-152"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e702-153">MIDL</span><span class="sxs-lookup"><span data-stu-id="5e702-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e702-154"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e702-154"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e702-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e702-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e702-156"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e702-156"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e702-157">DLL</span><span class="sxs-lookup"><span data-stu-id="5e702-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e702-158"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e702-158"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e702-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e702-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e702-160">**IUpdateEndpointProvider**</span><span class="sxs-lookup"><span data-stu-id="5e702-160">**IUpdateEndpointProvider**</span></span>](iupdateendpointprovider.md)
</dt> </dl>

 

 





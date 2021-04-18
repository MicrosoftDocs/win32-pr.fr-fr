---
title: Méthode IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: La méthode GetContentEnablersForRevocations récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats révoqués.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Méthode GetContentEnablersForRevocations format Windows Media
- Méthode GetContentEnablersForRevocations format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532843"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a><span data-ttu-id="748a0-106">IWMDRMSecurity :: GetContentEnablersForRevocations, méthode</span><span class="sxs-lookup"><span data-stu-id="748a0-106">IWMDRMSecurity::GetContentEnablersForRevocations method</span></span>

<span data-ttu-id="748a0-107">La méthode **GetContentEnablersForRevocations** récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats révoqués.</span><span class="sxs-lookup"><span data-stu-id="748a0-107">The **GetContentEnablersForRevocations** method retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="748a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="748a0-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="748a0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="748a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="748a0-110">*rgpbCerts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="748a0-110">*rgpbCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="748a0-111">Tableau de certificats pour lequel récupérer des activateurs de contenu.</span><span class="sxs-lookup"><span data-stu-id="748a0-111">Array of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="748a0-112">Le nombre d’éléments dans le tableau doit être spécifié par *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="748a0-112">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="748a0-113">*rgpdwCertSizes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="748a0-113">*rgpdwCertSizes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="748a0-114">Tableau contenant les tailles des certificats dans le tableau *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="748a0-114">Array containing the sizes of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="748a0-115">Le nombre d’éléments dans le tableau doit être spécifié par *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="748a0-115">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="748a0-116">*rgpguidCerts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="748a0-116">*rgpguidCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="748a0-117">Tableau contenant les types des certificats dans le tableau *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="748a0-117">Array containing the types of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="748a0-118">Le nombre d’éléments dans le tableau doit être spécifié par *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="748a0-118">The number of elements in the array must be specified by *cCerts*.</span></span> <span data-ttu-id="748a0-119">Pour chaque élément du tableau, utilisez l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="748a0-119">For each element of the array, use one of the following values.</span></span>



| <span data-ttu-id="748a0-120">GUID, constante</span><span class="sxs-lookup"><span data-stu-id="748a0-120">GUID constant</span></span>                 | <span data-ttu-id="748a0-121">Description</span><span class="sxs-lookup"><span data-stu-id="748a0-121">Description</span></span>                                                    |
|-------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="748a0-122">\_application REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="748a0-122">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="748a0-123">Spécifie un certificat d’application.</span><span class="sxs-lookup"><span data-stu-id="748a0-123">Specifies an application certificate.</span></span>                          |
| <span data-ttu-id="748a0-124">\_appareil REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="748a0-124">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="748a0-125">Spécifie un certificat d’appareil.</span><span class="sxs-lookup"><span data-stu-id="748a0-125">Specifies a device certificate.</span></span>                                |
| <span data-ttu-id="748a0-126">\_REVOCATIONTYPE WMDRM \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="748a0-126">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="748a0-127">Spécifie un certificat DRM Windows Media pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="748a0-127">Specifies a Windows Media DRM for Network Devices certificate.</span></span> |



 

</dd> <dt>

<span data-ttu-id="748a0-128">*cCerts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="748a0-128">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="748a0-129">Nombre de certificats pour lesquels récupérer des activateurs de contenu.</span><span class="sxs-lookup"><span data-stu-id="748a0-129">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="748a0-130">Il s’agit du nombre d’éléments dans le tableau *rgpbCerts* , du tableau *rgpdwCertSizes* et du tableau *rgpguidCerts* .</span><span class="sxs-lookup"><span data-stu-id="748a0-130">This is the number of elements in the *rgpbCerts* array, the *rgpdwCertSizes* array, and the *rgpguidCerts* array.</span></span>

</dd> <dt>

<span data-ttu-id="748a0-131">*hResultHint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="748a0-131">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="748a0-132">Valeur de retour reçue de l’opération qui a échoué en raison d’un certificat révoqué.</span><span class="sxs-lookup"><span data-stu-id="748a0-132">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="748a0-133">Si vous n’appelez pas en réponse à un appel de méthode qui a échoué, définissez sur S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="748a0-133">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="748a0-134">*prgContentEnablers* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="748a0-134">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="748a0-135">Tableau qui reçoit les adresses des interfaces **IMFContentEnabler** nouvellement créées.</span><span class="sxs-lookup"><span data-stu-id="748a0-135">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="748a0-136">Affectez la valeur **null** pour récupérer le nombre d’activateurs de contenu dans le paramètre *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="748a0-136">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="748a0-137">*pcContentEnablers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="748a0-137">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="748a0-138">Nombre d’éléments dans le tableau *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="748a0-138">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="748a0-139">Si *prgContentEnablers* a la valeur **null**, cette valeur est définie sur le nombre d’activateurs de contenu nécessaires sur la sortie.</span><span class="sxs-lookup"><span data-stu-id="748a0-139">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="748a0-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="748a0-140">Return value</span></span>

<span data-ttu-id="748a0-141">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="748a0-141">The method returns an **HRESULT**.</span></span> <span data-ttu-id="748a0-142">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="748a0-142">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="748a0-143">Code de retour</span><span class="sxs-lookup"><span data-stu-id="748a0-143">Return code</span></span>                                                                          | <span data-ttu-id="748a0-144">Description</span><span class="sxs-lookup"><span data-stu-id="748a0-144">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="748a0-145"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="748a0-145"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="748a0-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="748a0-146">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="748a0-147">Notes</span><span class="sxs-lookup"><span data-stu-id="748a0-147">Remarks</span></span>

<span data-ttu-id="748a0-148">Si vous utilisez l’interface **IMFContentEnabler** pour renouveler des composants révoqués, vous devez clarifier le processus pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="748a0-148">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="748a0-149">Cette clarification doit être apportée car le processus de mise à jour envoie des informations de l’ordinateur client vers un site Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="748a0-149">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="748a0-150">Quand vous appelez **IMFContentEnabler :: AutomaticEnable**, le activateur de contenu lance le navigateur par défaut avec l’adresse du service de mise à jour sur le site Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="748a0-150">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="748a0-151">Un identificateur unique qui identifie le composant révoqué est envoyé au service de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="748a0-151">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="748a0-152">Le service redirige ensuite le navigateur vers une page Web à partir de laquelle l’utilisateur peut être en mesure de télécharger et d’installer la nouvelle version du composant révoqué.</span><span class="sxs-lookup"><span data-stu-id="748a0-152">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="748a0-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="748a0-153">Requirements</span></span>



| <span data-ttu-id="748a0-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="748a0-154">Requirement</span></span> | <span data-ttu-id="748a0-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="748a0-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="748a0-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="748a0-156">Header</span></span><br/>  | <dl> <span data-ttu-id="748a0-157"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="748a0-157"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="748a0-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="748a0-158">Library</span></span><br/> | <dl> <span data-ttu-id="748a0-159"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="748a0-159"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="748a0-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="748a0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="748a0-161">**Révocation et renouvellement de composants automatisés**</span><span class="sxs-lookup"><span data-stu-id="748a0-161">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="748a0-162">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="748a0-162">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 






---
title: Méthode IWMDRMSecurity GetContentEnablersFromHashes (wmdrmsdk. h)
description: La méthode GetContentEnablersFromHashes récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats hachés.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Méthode GetContentEnablersFromHashes format Windows Media
- Méthode GetContentEnablersFromHashes format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetContentEnablersFromHashes
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528029"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a><span data-ttu-id="3a1d6-106">IWMDRMSecurity :: GetContentEnablersFromHashes, méthode</span><span class="sxs-lookup"><span data-stu-id="3a1d6-106">IWMDRMSecurity::GetContentEnablersFromHashes method</span></span>

<span data-ttu-id="3a1d6-107">La méthode **GetContentEnablersFromHashes** récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats hachés.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-107">The **GetContentEnablersFromHashes** method retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1d6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a1d6-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="3a1d6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a1d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a1d6-110">*rgpbCertHashes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a1d6-110">*rgpbCertHashes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1d6-111">Tableau de hachages de certificat pour lequel obtenir des activateurs de contenu.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-111">Array of certificate hashes to obtain content enablers for.</span></span>

</dd> <dt>

<span data-ttu-id="3a1d6-112">*cCerts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a1d6-112">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1d6-113">Nombre de certificats pour lesquels récupérer des activateurs de contenu.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-113">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="3a1d6-114">Il s’agit du nombre d’éléments dans le tableau *rgpbCertHashes* .</span><span class="sxs-lookup"><span data-stu-id="3a1d6-114">This is the number of elements in the *rgpbCertHashes* array.</span></span>

</dd> <dt>

<span data-ttu-id="3a1d6-115">*hResultHint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a1d6-115">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1d6-116">Valeur de retour reçue de l’opération qui a échoué en raison d’un certificat révoqué.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-116">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="3a1d6-117">Si vous n’appelez pas en réponse à un appel de méthode qui a échoué, définissez sur S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-117">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="3a1d6-118">*prgContentEnablers* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3a1d6-118">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1d6-119">Tableau qui reçoit les adresses des interfaces **IMFContentEnabler** nouvellement créées.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-119">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="3a1d6-120">Affectez la valeur **null** pour récupérer le nombre d’activateurs de contenu dans le paramètre *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="3a1d6-120">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3a1d6-121">*pcContentEnablers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3a1d6-121">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1d6-122">Nombre d’éléments dans le tableau *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="3a1d6-122">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="3a1d6-123">Si *prgContentEnablers* a la valeur **null**, cette valeur est définie sur le nombre d’activateurs de contenu nécessaires sur la sortie.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-123">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a1d6-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a1d6-124">Return value</span></span>

<span data-ttu-id="3a1d6-125">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3a1d6-126">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3a1d6-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3a1d6-127">Return code</span></span>                                                                          | <span data-ttu-id="3a1d6-128">Description</span><span class="sxs-lookup"><span data-stu-id="3a1d6-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3a1d6-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d6-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3a1d6-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a1d6-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a1d6-131">Notes</span><span class="sxs-lookup"><span data-stu-id="3a1d6-131">Remarks</span></span>

<span data-ttu-id="3a1d6-132">Si vous utilisez l’interface **IMFContentEnabler** pour renouveler des composants révoqués, vous devez clarifier le processus pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-132">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="3a1d6-133">Cette clarification doit être apportée car le processus de mise à jour envoie des informations de l’ordinateur client vers un site Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-133">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="3a1d6-134">Quand vous appelez **IMFContentEnabler :: AutomaticEnable**, le activateur de contenu lance le navigateur par défaut avec l’adresse du service de mise à jour sur le site Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-134">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="3a1d6-135">Un identificateur unique qui identifie le composant révoqué est envoyé au service de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-135">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="3a1d6-136">Le service redirige ensuite le navigateur vers une page Web à partir de laquelle l’utilisateur peut être en mesure de télécharger et d’installer la nouvelle version du composant révoqué.</span><span class="sxs-lookup"><span data-stu-id="3a1d6-136">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1d6-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a1d6-137">Requirements</span></span>



| <span data-ttu-id="3a1d6-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a1d6-138">Requirement</span></span> | <span data-ttu-id="3a1d6-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a1d6-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1d6-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a1d6-140">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1d6-141"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d6-141"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a1d6-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a1d6-142">Library</span></span><br/> | <dl> <span data-ttu-id="3a1d6-143"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d6-143"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1d6-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a1d6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1d6-145">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="3a1d6-145">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 






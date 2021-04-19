---
description: Retourne les informations d’identification pour authentifier un conteneur non joint à un domaine avec Active Directory.
title: 'ICcgDomainAuthCredentials :: GetPasswordCredentials, méthode (ccgplugins. h)'
ms.topic: reference
ms.date: 10/21/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials.GetPasswordCredentials
api_type:
- COM
api_location:
- ccgplugins.h
ms.openlocfilehash: abd70a109e491773b374ae32787760d265167baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542372"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="af53f-103">ICcgDomainAuthCredentials :: GetPasswordCredentials, méthode</span><span class="sxs-lookup"><span data-stu-id="af53f-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="af53f-104">Retourne les informations d’identification pour authentifier un conteneur non joint à un domaine avec Active Directory.</span><span class="sxs-lookup"><span data-stu-id="af53f-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="af53f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af53f-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="af53f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af53f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af53f-107">*pluginInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af53f-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af53f-108">Chaîne d’entrée passée par le runtime du conteneur.</span><span class="sxs-lookup"><span data-stu-id="af53f-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="af53f-109">L’implémentation cliente utilise la chaîne d’entrée fournie pour récupérer les informations d’authentification, généralement à partir d’un fournisseur de stockage sécurisé, qui sont retournées dans les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="af53f-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="af53f-110">La chaîne d’entrée est fournie au Compute Services hôte (HCS) dans un fichier de spécification d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="af53f-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="af53f-111">Pour plus d’informations, consultez la section **Notes** .</span><span class="sxs-lookup"><span data-stu-id="af53f-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="af53f-112">*nom_domaine* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af53f-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af53f-113">Nom de domaine pour les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="af53f-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="af53f-114">*nom d’utilisateur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af53f-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af53f-115">Nom d’utilisateur pour les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="af53f-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="af53f-116">*mot de passe* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af53f-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af53f-117">Mot de passe pour les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="af53f-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af53f-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af53f-118">Return value</span></span>

<span data-ttu-id="af53f-119">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="af53f-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="af53f-120">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="af53f-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="af53f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="af53f-121">Remarks</span></span>

<span data-ttu-id="af53f-122">L’API peut être appelée simultanément.</span><span class="sxs-lookup"><span data-stu-id="af53f-122">The API may be called concurrently.</span></span> <span data-ttu-id="af53f-123">Par conséquent, le développeur doit s’assurer que son implémentation est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="af53f-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="af53f-124">En outre, l’objet COM est activé hors processus et doit être enregistré de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="af53f-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="af53f-125">L’implémenteur doit ajouter une clé sous « HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses » pour son CLSID COM.</span><span class="sxs-lookup"><span data-stu-id="af53f-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="af53f-126">L’accès en écriture à « CCG\COMClasses » est limité aux comptes système et administrateur.</span><span class="sxs-lookup"><span data-stu-id="af53f-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="af53f-127">Voici un exemple de fichier de spécification d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="af53f-127">The following is an example credential specification file.</span></span> <span data-ttu-id="af53f-128">Pour plus d’informations sur la fourniture de ce fichier à l’ancrage, consultez [exécuter un conteneur avec un gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span><span class="sxs-lookup"><span data-stu-id="af53f-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

```json
{
    "CmsPlugins": [
        "ActiveDirectory"
    ],
    "DomainJoinConfig": {
        "Sid": "S-1-5-21-3700119848-2853083131-2094573802",
        "MachineAccountName": "gmsa1",
        "Guid": "630a7dd3-2d3e-4471-ae91-1d9ea2556cd5",
        "DnsTreeName": "contoso.com",
        "DnsName": "contoso.com",
        "NetBiosName": "CONTOSO"
    },
    "ActiveDirectoryConfig": {
        "GroupManagedServiceAccounts": [
            {
                "Name": "gmsa1",
                "Scope": "contoso.com"
            },
            {
                "Name": "gmsa1",
                "Scope": "CONTOSO"
            }
        ],
        "HostAccountConfig": {
            "PortableCcgVersion": "1",
            "PluginGUID": "{CFCA0441-511D-4B2A-862E-20348A78760B}",
            "PluginInput": "contoso.com:gmsaccg:<password>"
        }
    }
}

```

## <a name="examples"></a><span data-ttu-id="af53f-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="af53f-129">Examples</span></span>

<span data-ttu-id="af53f-130">L’exemple suivant illustre une implémentation simple de **ICcgDomainAuthCredentials**.</span><span class="sxs-lookup"><span data-stu-id="af53f-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="af53f-131">Notez que, à des fins d’illustration, cet exemple obtient les informations d’identification en analysant simplement la chaîne d’entrée.</span><span class="sxs-lookup"><span data-stu-id="af53f-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="af53f-132">Une implémentation réelle stocke les informations d’identification dans un magasin de données sécurisé et utilise la chaîne d’entrée pour localiser les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="af53f-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="af53f-133">En outre, les implémentations de la méthode COM standard ont été omises de cet exemple par souci de concision.</span><span class="sxs-lookup"><span data-stu-id="af53f-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


```C++
// UUID generated by the developer
[uuid("cfca0441-511d-4b2a-862e-20348a78760b")] 
class CCGStubPlugin : public RuntimeClass<RuntimeClassFlags<RuntimeClassType::ClassicCom>, ICcgDomainAuthCredentials >
{
   public:
    CCGStubPlugin() {}

    ~CCGStubPlugin() {}

    IFACEMETHODIMP GetPasswordCredentials(
        _In_ LPCWSTR pluginInput,
        _Outptr_ LPWSTR *domainName,
        _Outptr_ LPWSTR *username,
        _Outptr_ LPWSTR *password)
    {
        std::wstring domainParsed, userParsed, passwordParsed; 
        try
        {
            if(domainName == NULL || username == NULL || password == NULL)
            {
                return STG_E_INVALIDPARAMETER;
            }
            *domainName = NULL;
            *username = NULL;
            *password = NULL;
            wstring pluginInputString(pluginInput);
            if (count(pluginInputString.begin(), pluginInputString.end(), ':') < 2)
            {
                return CO_E_NOT_SUPPORTED;
            }
            // Extract creds of this format Domain:Username:Password
            size_t sep1 = pluginInputString.find(L":");
            size_t sep2 = pluginInputString.find(L":", sep1 + 1);
            domainParsed = pluginInputString.substr(0, sep1);
            userParsed = pluginInputString.substr(sep1 + 1, sep2 - sep1 - 1);
            passwordParsed = pluginInputString.substr(sep2 + 1);
        }
        catch (...)
        {
            return EVENT_E_INTERNALERROR;
        }

        auto userCo = wil::make_cotaskmem_string_nothrow(userParsed.c_str());
        auto passwordCo = wil::make_cotaskmem_string_nothrow(passwordParsed.c_str());
        auto domainCo = wil::make_cotaskmem_string_nothrow(domainParsed.c_str());
        if (userCo == nullptr || passwordCo == nullptr || domainCo == nullptr)
        {
            return STG_E_INSUFFICIENTMEMORY;
        }

        *domainName = domainCo.release();
        *username = userCo.release();
        *password = passwordCo.release();
        return S_OK;
    }
};
CoCreatableClass(CCGStubPlugin);

```



## <a name="requirements"></a><span data-ttu-id="af53f-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af53f-134">Requirements</span></span>




| <span data-ttu-id="af53f-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af53f-135">Requirement</span></span> | <span data-ttu-id="af53f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="af53f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af53f-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af53f-137">Minimum supported server</span></span> | <span data-ttu-id="af53f-138">Windows Server, version 2004</span><span class="sxs-lookup"><span data-stu-id="af53f-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="af53f-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="af53f-139">Header</span></span>                   | <span data-ttu-id="af53f-140">ccgplugins. h</span><span class="sxs-lookup"><span data-stu-id="af53f-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="af53f-141">IID</span><span class="sxs-lookup"><span data-stu-id="af53f-141">IID</span></span>                    | <span data-ttu-id="af53f-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="af53f-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 


---
description: Implémentation de IMFNetCredentialManager
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: Implémentation de IMFNetCredentialManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c026f2c12b2ff248032a56d9c48a0e0e1576c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543088"
---
# <a name="implementing-imfnetcredentialmanager"></a><span data-ttu-id="9e603-103">Implémentation de IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="9e603-103">Implementing IMFNetCredentialManager</span></span>

<span data-ttu-id="9e603-104">Dans la méthode [**IMFNetCredentialManager :: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9e603-104">In the [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method, do the following.</span></span>

1.  <span data-ttu-id="9e603-105">Si vous ne disposez pas déjà d’un pointeur [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , appelez [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) pour créer l’objet de cache des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9e603-105">If you do not have an [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) pointer already, call [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) to create the credential cache object.</span></span> <span data-ttu-id="9e603-106">Stocker ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="9e603-106">Store this pointer.</span></span>
2.  <span data-ttu-id="9e603-107">Appelez [**IMFNetCredentialCache :: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="9e603-107">Call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span> <span data-ttu-id="9e603-108">Définissez les indicateurs dans le paramètre *dwAuthenticationFlags* comme suit :</span><span class="sxs-lookup"><span data-stu-id="9e603-108">Set the flags in the *dwAuthenticationFlags* parameter as follows:</span></span>
    -   <span data-ttu-id="9e603-109">Si le membre **hrOp** de la structure [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) est égal **au \_ \_ \_ ACCESSDENIED proxy NS E**, définissez l’indicateur de **\_ \_ proxy d’authentification MFNET** .</span><span class="sxs-lookup"><span data-stu-id="9e603-109">If the **hrOp** member of the [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) structure equals **NS\_E\_PROXY\_ACCESSDENIED**, set the **MFNET\_AUTHENTICATION\_PROXY** flag.</span></span>
    -   <span data-ttu-id="9e603-110">Si **fClearTextPackage** a la **valeur true**, définissez l’indicateur de **\_ \_ \_ texte en clair d’authentification MFNET** .</span><span class="sxs-lookup"><span data-stu-id="9e603-110">If **fClearTextPackage** is **TRUE**, set the **MFNET\_AUTHENTICATION\_CLEAR\_TEXT** flag.</span></span>
    -   <span data-ttu-id="9e603-111">Si **fAllowLoggedOnUser** a la **valeur true**, définissez l’indicateur **de l' \_ \_ \_ \_ utilisateur connecté à l’authentification MFNET** .</span><span class="sxs-lookup"><span data-stu-id="9e603-111">If **fAllowLoggedOnUser** is **TRUE**, set the **MFNET\_AUTHENTICATION\_LOGGED\_ON\_USER** flag.</span></span>
3.  <span data-ttu-id="9e603-112">La méthode [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) retourne un pointeur [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) et éventuellement l’indicateur de \_ demande Require.</span><span class="sxs-lookup"><span data-stu-id="9e603-112">The [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) method returns an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer and possibly the REQUIRE\_PROMPT flag.</span></span> <span data-ttu-id="9e603-113">Stockez le pointeur **IMFNetCredential** .</span><span class="sxs-lookup"><span data-stu-id="9e603-113">Store the **IMFNetCredential** pointer.</span></span>
4.  <span data-ttu-id="9e603-114">Si [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) ne retourne pas l’indicateur de **\_ demande require** , vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="9e603-114">If [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) does not return the **REQUIRE\_PROMPT** flag, you are done.</span></span> <span data-ttu-id="9e603-115">Passez à l’étape 9.</span><span class="sxs-lookup"><span data-stu-id="9e603-115">Skip to step 9.</span></span>
5.  <span data-ttu-id="9e603-116">Sinon, si [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) retourne l’indicateur de **\_ demande require** , vous devez inviter l’utilisateur à entrer son nom d’utilisateur et son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9e603-116">Otherwise, if [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) returns the **REQUIRE\_PROMPT** flag, you must prompt the user for his or her user name and password.</span></span>
6.  <span data-ttu-id="9e603-117">Si **fClearTextPackage** a la **valeur false**, chiffrez les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9e603-117">If **fClearTextPackage** is **FALSE**, encrypt the credentials.</span></span>
7.  <span data-ttu-id="9e603-118">Appelez [**IMFNetCredential :: SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) et [**IMFNetCredential :: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) pour définir le nom et le mot de passe de l’utilisateur sur l’objet d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9e603-118">Call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) to set the user's name and password on the credentials object.</span></span>
8.  <span data-ttu-id="9e603-119">Si vous le souhaitez, appelez [**IMFNetCredentialCache :: SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) pour mettre à jour l’objet de cache des informations d’identification avec les préférences de l’utilisateur pour le stockage et l’envoi des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9e603-119">Optionally, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) to update the credential cache object with the user's preferences for storing and sending credentials.</span></span>
9.  <span data-ttu-id="9e603-120">Appelez le rappel [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) en appelant [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="9e603-120">Invoke the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>

<span data-ttu-id="9e603-121">Dans la méthode [**IMFNetCredentialManager :: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) , retournez le pointeur [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) obtenu dans la méthode [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="9e603-121">In the [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method, return the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer obtained in the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span>

<span data-ttu-id="9e603-122">Dans la méthode [**IMFNetCredentialManager :: SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) , transmettez les paramètres d’entrée directement à la méthode [**IMFNetCredentialCache :: SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) .</span><span class="sxs-lookup"><span data-stu-id="9e603-122">In the [**IMFNetCredentialManager::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) method, pass the input parameters directly to the [**IMFNetCredentialCache::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) method.</span></span> <span data-ttu-id="9e603-123">Cela indique au cache des informations d’identification si les informations d’identification ont été acceptées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="9e603-123">This notifies the credential cache whether the credentials were accepted by the server.</span></span>

<span data-ttu-id="9e603-124">Si vous avez besoin d’inviter l’utilisateur (étape 5) ou de chiffrer les informations d’identification (étape 6), vous devez le faire sur un thread de file d’attente de travail, afin de ne pas bloquer le pipeline Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9e603-124">If you need to prompt the user (step 5) or encrypt the credentials (step 6), you should do so on a work-queue thread, so that you do not block the Microsoft Media Foundation pipeline.</span></span> <span data-ttu-id="9e603-125">Appelez [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) , puis effectuez les étapes restantes à l’intérieur du rappel de file d’attente de travail.</span><span class="sxs-lookup"><span data-stu-id="9e603-125">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) and then perform the remaining steps inside the work-queue callback.</span></span>

> [!Note]  
> <span data-ttu-id="9e603-126">Sachez que [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) peut être appelé lors de la création de la source réseau.</span><span class="sxs-lookup"><span data-stu-id="9e603-126">Be aware that [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) might be invoked while the network source is being created.</span></span> <span data-ttu-id="9e603-127">Par conséquent, si vous créez la source réseau en appelant la méthode synchrone [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) , votre thread appelant peut se bloquer pendant l’acquisition des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="9e603-127">Therefore, if you create the network source by calling the synchronous [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method, your calling thread might block while the credentials are acquired.</span></span> <span data-ttu-id="9e603-128">Par conséquent, il est recommandé d’utiliser à la place la méthode asynchrone [**IMFSourceResolver :: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="9e603-128">Therefore, it is recommended to use the asynchronous [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method instead.</span></span>

 

## <a name="example"></a><span data-ttu-id="9e603-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="9e603-129">Example</span></span>

<span data-ttu-id="9e603-130">Cet exemple montre un type de comportement qu’un gestionnaire d’informations d’identification peut fournir.</span><span class="sxs-lookup"><span data-stu-id="9e603-130">This example shows one type of behavior that a credential manager could provide.</span></span>

<span data-ttu-id="9e603-131">Voici une déclaration de la classe qui implémente [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span><span class="sxs-lookup"><span data-stu-id="9e603-131">Here is a declaration of the class that implements [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span></span>


```C++
class CCredentialManager : public IMFNetCredentialManager, IMFAsyncCallback 
{
    long                    m_cRef;
    IMFNetCredentialCache   *m_pCredentialCache;

public:
    CCredentialManager () : m_cRef(1), m_pCredentialCache(NULL)
    { 
    }
    ~CCredentialManager()
    {
        SafeRelease(&m_pCredentialCache);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCredentialManager, IMFNetCredentialManager),
            QITABENT(CCredentialManager, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP BeginGetCredentials(
        MFNetCredentialManagerGetParam* pParam,
        IMFAsyncCallback* pCallback,
        IUnknown* pState
        );

    STDMETHODIMP EndGetCredentials(
        IMFAsyncResult* pResult, 
        IMFNetCredential** ppCred);

    STDMETHODIMP SetGood(IMFNetCredential* pCred, BOOL fGood)
    {
        if (!pCred)
        {
            return E_POINTER;
        }

        return m_pCredentialCache->SetGood(pCred, fGood);
    }


    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="9e603-132">Pour suivre l’état de l’opération [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) , la classe utilise l’objet d’assistance suivant :</span><span class="sxs-lookup"><span data-stu-id="9e603-132">To track the state of the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) operation, the class uses the following helper object:</span></span>


```C++
// Holds state information for the GetCredentials operation, so that work can 
// be moved to a work-queue thread.

struct CredentialOp : public IUnknown
{
    long                m_cRef;
    IMFNetCredential    *m_pCredential;
    DWORD               m_dwFlags;

    CredentialOp(IMFNetCredential *pCredential) 
        : m_cRef(1), m_dwFlags(0), m_pCredential(pCredential)
    {
        m_pCredential->AddRef();
    }

    ~CredentialOp()
    {
        SafeRelease(&m_pCredential);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CredentialOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="9e603-133">La méthode [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) crée le cache d’informations d’identification et obtient un pointeur [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="9e603-133">The [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method creates the credential cache and gets an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer.</span></span> <span data-ttu-id="9e603-134">Si l’utilisateur doit être invité (indiqué par l’indicateur **de \_ demande require** ), la méthode appelle [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) pour mettre en file d’attente un nouvel élément de travail :</span><span class="sxs-lookup"><span data-stu-id="9e603-134">If the user must be prompted (indicated by the **REQUIRE\_PROMPT** flag), the method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item:</span></span>


```C++
STDMETHODIMP CCredentialManager::BeginGetCredentials(
    MFNetCredentialManagerGetParam* pParam,
    IMFAsyncCallback* pCallback,
    IUnknown* pState
    )
{
    if (!pParam || !pCallback)
    {
        return E_POINTER;
    }

    DWORD dwAuthenticationFlags = 0;
    DWORD dwRequirementFlags = 0;

    if (pParam->hrOp == NS_E_PROXY_ACCESSDENIED)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_PROXY;
    }

    if (pParam->fAllowLoggedOnUser)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_LOGGED_ON_USER;
    }

    if (pParam->fClearTextPackage)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_CLEAR_TEXT;
    }

    IMFNetCredential *pCredential =  NULL;
    IMFAsyncResult* pResult = NULL;

    HRESULT hr = S_OK;

    if (m_pCredentialCache == NULL)
    {
        hr = MFCreateCredentialCache(&m_pCredentialCache);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    hr = m_pCredentialCache->GetCredential(
        pParam->pszUrl, 
        pParam->pszRealm, 
        dwAuthenticationFlags, 
        &pCredential, 
        &dwRequirementFlags
        );

    if (FAILED(hr))
    {
        goto done;
    }

    if( ( dwRequirementFlags & REQUIRE_PROMPT ) == 0 )
    {
        // The credential is good to use. Prompting the user is not required.
        hr = S_OK;
        goto done;
    }

    // The credential requires prompting the user. 
    CredentialOp *pOp = new (std::nothrow) CredentialOp(pCredential);

    if (pOp == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Set flags. Use these to inform the user if the credentials will
    // be sent in plaintext or saved in the credential cache.

    if (pParam->fClearTextPackage)
    {
        // Notify the user that credentials will be sent in plaintext.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT;
    }

    if(dwRequirementFlags & REQUIRE_SAVE_SELECTED )
    {
        // Credentials will be saved in the cache by default.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_SAVE;
    }

    // NOTE: The application should enable to user to deselect these two flags;
    // for example, through check boxes in the prompt dialog.


    // Now queue the work item.

    hr = MFCreateAsyncResult(pOp, pCallback, pState, &pResult);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION, this, pResult);

done:
    SafeRelease(&pResult);
    SafeRelease(&pCredential);
    SafeRelease(&pOp);
    return hr;
}
```



<span data-ttu-id="9e603-135">Le thread de file d’attente de travail appelle [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), qui invite l’utilisateur, puis appelle [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) pour appeler le pointeur de rappel fourni dans [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span><span class="sxs-lookup"><span data-stu-id="9e603-135">The work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), which prompts the user and then calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the callback pointer that was provided in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span></span>


```C++
STDMETHODIMP CCredentialManager::Invoke(IMFAsyncResult* pResult)
{
    IUnknown *pState = NULL;
    IMFAsyncResult *pGetCredentialsResult = NULL;
    IUnknown *pOpState = NULL;

    CredentialOp *pOp = NULL;   // not AddRef'd

    HRESULT hr = pResult->GetState(&pState);

    if (SUCCEEDED(hr))
    {
        hr = pState->QueryInterface(IID_PPV_ARGS(&pGetCredentialsResult));
    }

    if (SUCCEEDED(hr))
    {
        hr = pGetCredentialsResult->GetObject(&pOpState);
    }

    if (SUCCEEDED(hr))
    {
        pOp = static_cast<CredentialOp*>(pOpState);

        // Display a dialog for the user to enter user name and password.
        hr = PromptUserCredentials(pOp);
    }

    if (SUCCEEDED(hr) && m_pCredentialCache)
    {
        // Update with options set by the user.
        hr = m_pCredentialCache->SetUserOptions(
            pOp->m_pCredential, 
            pOp->m_dwFlags
            );
    }

    if (pGetCredentialsResult)
    {
        pGetCredentialsResult->SetStatus(hr);
        MFInvokeCallback(pGetCredentialsResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pGetCredentialsResult);
    SafeRelease(&pOpState);
    return S_OK;
}
```



<span data-ttu-id="9e603-136">La méthode [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) termine l’opération en retournant le pointeur [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="9e603-136">The [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method completes the operation by returning the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer to the caller.</span></span>


```C++
STDMETHODIMP CCredentialManager::EndGetCredentials(
    IMFAsyncResult* pResult, 
    IMFNetCredential** ppCred
    )
{
    if (!pResult || !ppCred)
    {
        return E_POINTER;
    }

    *ppCred = NULL;

    IUnknown *pUnk = NULL;

    // Check the result of the asynchronous operation.
    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        // The operation failed.
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    CredentialOp *pOp = static_cast<CredentialOp*>(pUnk);

    *ppCred = pOp->m_pCredential;
    pOp->m_pCredential = NULL;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9e603-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e603-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e603-138">Authentification de la source réseau</span><span class="sxs-lookup"><span data-stu-id="9e603-138">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 




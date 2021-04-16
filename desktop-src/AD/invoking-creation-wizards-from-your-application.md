---
title: Appel d’assistants de création à partir de votre application
description: Une application ou un composant peut utiliser les mêmes assistants de création d’objets de service d’annuaire que ceux utilisés par les composants logiciels enfichables MMC d’administration de Active Directory. Cela s’effectue à l’aide de l’interface IDsAdminCreateObj.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Appel d’assistants de création à partir de votre application AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa523d3b861d1d4a7588455b04c1a9633734253a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462847"
---
# <a name="invoking-creation-wizards-from-your-application"></a><span data-ttu-id="e25f9-104">Appel d’assistants de création à partir de votre application</span><span class="sxs-lookup"><span data-stu-id="e25f9-104">Invoking Creation Wizards from Your Application</span></span>

<span data-ttu-id="e25f9-105">Une application ou un composant peut utiliser les mêmes assistants de création d’objets de service d’annuaire que ceux utilisés par les composants logiciels enfichables MMC d’administration de Active Directory. Cela s’effectue à l’aide de l’interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="e25f9-105">An application or component can use the same directory service object creation wizards used by the Active Directory administrative MMC snap-ins. This is accomplished with the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface.</span></span>

## <a name="using-the-idsadmincreateobj-interface"></a><span data-ttu-id="e25f9-106">Utilisation de l’interface IDsAdminCreateObj</span><span class="sxs-lookup"><span data-stu-id="e25f9-106">Using the IDsAdminCreateObj Interface</span></span>

<span data-ttu-id="e25f9-107">Une application ou un composant (client) crée une instance de l’interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’identificateur de classe **CLSID \_ DsAdminCreateObj** .</span><span class="sxs-lookup"><span data-stu-id="e25f9-107">An application or component (client) creates an instance of the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsAdminCreateObj** class identifier.</span></span> <span data-ttu-id="e25f9-108">COM doit être initialisé en appelant [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) avant l’appel de **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="e25f9-108">COM must be initialized by calling [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before **CoCreateInstance** is called.</span></span>

<span data-ttu-id="e25f9-109">Le client appelle ensuite [**IDsAdminCreateObj :: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) pour initialiser l’objet [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="e25f9-109">The client then calls [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) to initialize the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object.</span></span> <span data-ttu-id="e25f9-110">**IDsAdminCreateObj :: Initialize** accepte un pointeur d’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) qui représente le conteneur dans lequel l’objet doit être créé, ainsi que le nom de classe de l’objet à créer.</span><span class="sxs-lookup"><span data-stu-id="e25f9-110">**IDsAdminCreateObj::Initialize** accepts an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface pointer that represents the container that the object should be created in, and the class name of the object to be created.</span></span> <span data-ttu-id="e25f9-111">Lors de la création d’objets utilisateur, il est également possible de spécifier un objet existant qui sera copié dans le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="e25f9-111">When creating user objects, it is also possible to specify an existing object that will be copied to the new object.</span></span>

<span data-ttu-id="e25f9-112">Lorsque l’objet [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) a été initialisé, le client appelle [**IDsAdminCreateObj :: CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) pour afficher l’Assistant Création d’objet.</span><span class="sxs-lookup"><span data-stu-id="e25f9-112">When the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object has been initialized, the client calls [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) to display the object creation wizard.</span></span>

<span data-ttu-id="e25f9-113">Contrairement à la plupart des identificateurs de classe et d’interface, les identificateurs **CLSID \_ DsAdminCreateObj** et **IID \_ ADsAdminCreateObj** ne sont pas définis dans un fichier bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e25f9-113">Unlike most class and interface identifiers, **CLSID\_DsAdminCreateObj** and **IID\_ADsAdminCreateObj** are not defined in a library file.</span></span> <span data-ttu-id="e25f9-114">Cela signifie que vous devez définir le stockage pour ces identificateurs dans votre application.</span><span class="sxs-lookup"><span data-stu-id="e25f9-114">This means you must define the storage for these identifiers within your application.</span></span> <span data-ttu-id="e25f9-115">Pour ce faire, vous devez inclure le fichier Initguid. h immédiatement avant d’inclure DSAdmin. h.</span><span class="sxs-lookup"><span data-stu-id="e25f9-115">To do this, you must include the file initguid.h immediately before including dsadmin.h.</span></span> <span data-ttu-id="e25f9-116">Le fichier Initguid. h doit être inclus une seule fois dans une application.</span><span class="sxs-lookup"><span data-stu-id="e25f9-116">The initguid.h file must only be included once in an application.</span></span> <span data-ttu-id="e25f9-117">L’exemple de code suivant montre comment inclure ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="e25f9-117">The following code example shows how to include these files.</span></span>


```C++
#include <initguid.h>
#include <dsadmin.h>
```



<span data-ttu-id="e25f9-118">L’exemple de code suivant montre comment l’interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) peut être créée et utilisée pour démarrer l’Assistant Création d’objet pour un objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e25f9-118">The following code example shows how the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface can be created and used to start the object creation wizard for a user object.</span></span>


```C++
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <atlbase.h>
#include <atlstr.h>
#include "activeds.h"
#include <initguid.h> // Only include this in one source file
#include <dsadmin.h>

//  GetUserContainer() function binds to the user container
IADsContainer* GetUserContainer(void)
{
    IADsContainer *pUsers = NULL;
    HRESULT hr;
    IADs *pRoot;

    //  Bind to the rootDSE.
    hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (LPVOID*)&pRoot);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        CComBSTR sbstr(L"defaultNamingContext");

        //  Get the default naming context (domain) DN.
        hr = pRoot->Get(sbstr, &var);
        if(SUCCEEDED(hr) && (VT_BSTR == var.vt))
        {
            CStringW sstr(L"LDAP://CN=Users,");
            sstr += var.bstrVal;

            //  Bind to the User container.
            hr = ADsGetObject(sstr, IID_IADsContainer, (LPVOID*)&pUsers);

            VariantClear(&var);
        }
    }

    return pUsers;
}


//  The LaunchNewUserWizard() function launches the user wizard.
HRESULT LaunchNewUserWizard(IADs** ppAdsOut)
{
    if(NULL == ppAdsOut)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IDsAdminCreateObj* pCreateObj = NULL;

    hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_IDsAdminCreateObj,
                            (void**)&pCreateObj);

    if(SUCCEEDED(hr))
    {
        IADsContainer *pContainer;

        pContainer = GetUserContainer();

        if(pContainer)
        {
            hr = pCreateObj->Initialize(pContainer, NULL, L"user");
            if(SUCCEEDED(hr))
            {
                HWND    hwndParent;

                hwndParent = GetDesktopWindow();

                hr = pCreateObj->CreateModal(hwndParent, ppAdsOut);
            }

            pContainer->Release();
        }

        pCreateObj->Release();
    }

    return hr;    
}

//  Entry point to the application
int main(void)
{
    HRESULT hr;
    IADs *pAds = NULL;

    CoInitialize(NULL);

    hr = LaunchNewUserWizard(&pAds);
    if((S_OK == hr) && (NULL != pAds))
    {
        pAds->Release();
    }

    CoUninitialize();

    return 0;
}
```



 

 
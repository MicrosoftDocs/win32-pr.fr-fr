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
# <a name="invoking-creation-wizards-from-your-application"></a>Appel d’assistants de création à partir de votre application

Une application ou un composant peut utiliser les mêmes assistants de création d’objets de service d’annuaire que ceux utilisés par les composants logiciels enfichables MMC d’administration de Active Directory. Cela s’effectue à l’aide de l’interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .

## <a name="using-the-idsadmincreateobj-interface"></a>Utilisation de l’interface IDsAdminCreateObj

Une application ou un composant (client) crée une instance de l’interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’identificateur de classe **CLSID \_ DsAdminCreateObj** . COM doit être initialisé en appelant [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) avant l’appel de **CoCreateInstance** .

Le client appelle ensuite [**IDsAdminCreateObj :: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) pour initialiser l’objet [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) . **IDsAdminCreateObj :: Initialize** accepte un pointeur d’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) qui représente le conteneur dans lequel l’objet doit être créé, ainsi que le nom de classe de l’objet à créer. Lors de la création d’objets utilisateur, il est également possible de spécifier un objet existant qui sera copié dans le nouvel objet.

Lorsque l’objet [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) a été initialisé, le client appelle [**IDsAdminCreateObj :: CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) pour afficher l’Assistant Création d’objet.

Contrairement à la plupart des identificateurs de classe et d’interface, les identificateurs **CLSID \_ DsAdminCreateObj** et **IID \_ ADsAdminCreateObj** ne sont pas définis dans un fichier bibliothèque. Cela signifie que vous devez définir le stockage pour ces identificateurs dans votre application. Pour ce faire, vous devez inclure le fichier Initguid. h immédiatement avant d’inclure DSAdmin. h. Le fichier Initguid. h doit être inclus une seule fois dans une application. L’exemple de code suivant montre comment inclure ces fichiers.


```C++
#include <initguid.h>
#include <dsadmin.h>
```



L’exemple de code suivant montre comment l’interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) peut être créée et utilisée pour démarrer l’Assistant Création d’objet pour un objet utilisateur.


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



 

 
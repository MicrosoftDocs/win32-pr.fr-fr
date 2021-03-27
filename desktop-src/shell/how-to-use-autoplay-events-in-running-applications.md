---
description: L’interface IHWEventHandler peut être inscrite dans la table ROT (Running Object Table) afin que les applications en cours d’exécution aient accès aux événements de lecture automatique.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Guide pratique pour utiliser des événements de lecture automatique dans des applications en cours d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951934"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a><span data-ttu-id="4f394-103">Guide pratique pour utiliser des événements de lecture automatique dans des applications en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="4f394-103">How to Use AutoPlay Events in Running Applications</span></span>

<span data-ttu-id="4f394-104">L’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) peut être inscrite dans la table ROT (Running Object Table) afin que les applications en cours d’exécution aient accès aux événements de lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="4f394-104">The [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface can be registered in the running object table (ROT) so that running applications have access to AutoPlay events.</span></span>

<span data-ttu-id="4f394-105">Les instructions suivantes décrivent comment utiliser des événements de lecture automatique dans des applications en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4f394-105">The following instructions describe how to use AutoPlay events in running applications.</span></span>

## <a name="instructions"></a><span data-ttu-id="4f394-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="4f394-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="4f394-107">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="4f394-107">Step 1:</span></span>

<span data-ttu-id="4f394-108">Créez un nouveau composant qui implémente l’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="4f394-108">Create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="4f394-109">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="4f394-109">Step 2:</span></span>

<span data-ttu-id="4f394-110">Initialisez le nouveau composant avec la valeur InitCmdLine à partir de l’entrée du gestionnaire particulier sous la clé des **gestionnaires** .</span><span class="sxs-lookup"><span data-stu-id="4f394-110">Initialize the new component with the InitCmdLine value from the particular handler's entry under the **Handlers** key.</span></span>

<span data-ttu-id="4f394-111">Cette étape est requise, car la lecture automatique n’appelle pas la méthode Initialize.</span><span class="sxs-lookup"><span data-stu-id="4f394-111">This step is required because Autoplay does not call the Initialize method.</span></span>

### <a name="step-3"></a><span data-ttu-id="4f394-112">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="4f394-112">Step 3:</span></span>

<span data-ttu-id="4f394-113">Appelez la fonction [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) pour obtenir un moniker qui représente votre composant et le gestionnaire d’événements que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="4f394-113">Call the [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) function to get a moniker that represents your component and the event handler that you want to call.</span></span>

### <a name="step-4"></a><span data-ttu-id="4f394-114">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="4f394-114">Step 4:</span></span>

<span data-ttu-id="4f394-115">Utilisez le paramètre *ppmoniker* pour inscrire votre composant dans la table ROT.</span><span class="sxs-lookup"><span data-stu-id="4f394-115">Use the *ppmoniker* parameter to register your component in the ROT.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f394-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4f394-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f394-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut poser des risques de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4f394-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) can pose security risks.</span></span> <span data-ttu-id="4f394-118">Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="4f394-118">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

<span data-ttu-id="4f394-119">L’appel à [**IRunningObjectTable :: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requiert que le composant ait les informations **AppID** suivantes dans le registre.</span><span class="sxs-lookup"><span data-stu-id="4f394-119">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that the component have the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a><span data-ttu-id="4f394-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f394-120">Related topics</span></span>

[<span data-ttu-id="4f394-121">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="4f394-121">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[<span data-ttu-id="4f394-122">**CreateHardwareEventMoniker**</span><span class="sxs-lookup"><span data-stu-id="4f394-122">**CreateHardwareEventMoniker**</span></span>](createhardwareeventmoniker.md)

---
title: Utilisation d’un moniker de session
description: L’activation de session à session permet à un processus client d’activer un processus serveur local sur une session spécifiée.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316182"
---
# <a name="using-a-session-moniker"></a><span data-ttu-id="efb7d-103">Utilisation d’un moniker de session</span><span class="sxs-lookup"><span data-stu-id="efb7d-103">Using a Session Moniker</span></span>

<span data-ttu-id="efb7d-104">L’activation de session à session permet à un processus client d’activer un processus serveur local sur une session spécifiée.</span><span class="sxs-lookup"><span data-stu-id="efb7d-104">Session-to-session activation allows a client process to activate a local server process on a specified session.</span></span> <span data-ttu-id="efb7d-105">Vous pouvez effectuer cette opération pour chaque session à l’aide d’un moniker de session fourni par le système.</span><span class="sxs-lookup"><span data-stu-id="efb7d-105">You can do this on a per-session basis by using a system-supplied session moniker.</span></span> <span data-ttu-id="efb7d-106">Pour plus d’informations sur la création d’un moniker de session, consultez Activation de session [à session à l’aide d’un moniker de session](session-to-session-activation-with-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="efb7d-106">For more information about creating a session moniker, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md).</span></span>

<span data-ttu-id="efb7d-107">L’exemple suivant montre comment activer un processus serveur local avec l’ID de classe « 10000013-0000-0000-0000-000000000001 » dans la session avec l’ID de session 3.</span><span class="sxs-lookup"><span data-stu-id="efb7d-107">The following example shows how to activate a local server process with the class ID "10000013-0000-0000-0000-000000000001" on the session with the session ID 3.</span></span>

<span data-ttu-id="efb7d-108">Tout d’abord, l’exemple appelle la fonction [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com.</span><span class="sxs-lookup"><span data-stu-id="efb7d-108">First, the sample calls the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function to initialize the COM library.</span></span> <span data-ttu-id="efb7d-109">L’exemple appelle ensuite [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) pour récupérer un pointeur vers une implémentation de l’interface [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="efb7d-109">Then the sample calls [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) to retrieve a pointer to an implementation of the [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="efb7d-110">Cet objet stocke des informations sur les opérations de liaison de moniker. le pointeur est requis pour appeler les méthodes de l’interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="efb7d-110">This object stores information about moniker-binding operations; the pointer is required to call methods of the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="efb7d-111">L’exemple appelle ensuite la fonction [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) pour créer le moniker de la session composite, puis la méthode [**IMoniker :: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) pour activer la connexion entre le client et le processus serveur, à l’aide du moniker de session nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="efb7d-111">Next the sample calls the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function to create the composite session moniker and then the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to activate the connection between the client and the server process, using the newly created session moniker.</span></span> <span data-ttu-id="efb7d-112">À ce stade, vous pouvez utiliser le pointeur d’interface pour effectuer les opérations souhaitées sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="efb7d-112">At this point you can use the interface pointer to perform the desired operations on the object.</span></span> <span data-ttu-id="efb7d-113">Enfin, l’exemple libère le contexte de liaison et appelle la fonction [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="efb7d-113">Finally, the sample releases the bind context and calls the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



<span data-ttu-id="efb7d-114">Comme « {ID de classe du moniker de classe} » est également un moyen de nommer un moniker de classe, vous pouvez utiliser la chaîne suivante pour nommer le moniker composite (le moniker de session composé du moniker de la classe) au lieu de la méthode illustrée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="efb7d-114">Because "{class id of the class moniker}" is also a way to name a class moniker, you can use the following string to name the composite moniker (the session moniker composed with the class moniker) instead of the way show in the preceding example.</span></span>

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> <span data-ttu-id="efb7d-115">Si le même utilisateur est connecté à chaque session pendant une activation inter-sessions, vous pouvez activer un processus serveur configuré pour s’exécuter dans le mode d’activation d’utilisateur interactif RunAs.</span><span class="sxs-lookup"><span data-stu-id="efb7d-115">If the same user is logged on to each session during a cross-session activation, you can successfully activate any server process configured to run in the RunAs Interactive User activation mode.</span></span> <span data-ttu-id="efb7d-116">Si différents utilisateurs sont connectés à chaque session, le serveur doit appeler la fonction [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir les droits d’utilisateur appropriés avant une activation réussie et la connexion peut se produire entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="efb7d-116">If different users are logged on to each session, the server must call the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function to set the appropriate user rights before a successful activation and connection can occur between the client and the server.</span></span> <span data-ttu-id="efb7d-117">Pour ce faire, le serveur doit implémenter une interface [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personnalisée et passer l’implémentation à la procédure **CoInitializeSecurity**.</span><span class="sxs-lookup"><span data-stu-id="efb7d-117">One way to accomplish this would be for the server to implement a custom [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) interface and pass the implementation to **CoInitializeSecurity**.</span></span> <span data-ttu-id="efb7d-118">Dans tous les cas, l’utilisateur client doit disposer des autorisations d' [**accès**](../com/accesspermission.md) et de [**lancement**](../com/launchpermission.md) appropriées spécifiées par l’application en cours d’exécution sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="efb7d-118">In any case, the client user must have the appropriate [**Launch**](../com/launchpermission.md) and [**Access Permissions**](../com/accesspermission.md) that are specified by the application running on the server.</span></span> <span data-ttu-id="efb7d-119">Pour plus d’informations [, consultez sécurité dans com](../com/security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="efb7d-119">For more information see [Security in COM](../com/security-in-com.md).</span></span>

 

<span data-ttu-id="efb7d-120">Pour plus d’informations sur les monikers et les modes d’activation fournis par le système, consultez [monikers](../com/monikers.md), l’interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) et la [clé AppID](/windows/desktop/com/appid-key) dans la documentation com du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="efb7d-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
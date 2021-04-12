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
# <a name="using-a-session-moniker"></a>Utilisation d’un moniker de session

L’activation de session à session permet à un processus client d’activer un processus serveur local sur une session spécifiée. Vous pouvez effectuer cette opération pour chaque session à l’aide d’un moniker de session fourni par le système. Pour plus d’informations sur la création d’un moniker de session, consultez Activation de session [à session à l’aide d’un moniker de session](session-to-session-activation-with-a-session-moniker.md).

L’exemple suivant montre comment activer un processus serveur local avec l’ID de classe « 10000013-0000-0000-0000-000000000001 » dans la session avec l’ID de session 3.

Tout d’abord, l’exemple appelle la fonction [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com. L’exemple appelle ensuite [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) pour récupérer un pointeur vers une implémentation de l’interface [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) . Cet objet stocke des informations sur les opérations de liaison de moniker. le pointeur est requis pour appeler les méthodes de l’interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) . L’exemple appelle ensuite la fonction [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) pour créer le moniker de la session composite, puis la méthode [**IMoniker :: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) pour activer la connexion entre le client et le processus serveur, à l’aide du moniker de session nouvellement créé. À ce stade, vous pouvez utiliser le pointeur d’interface pour effectuer les opérations souhaitées sur l’objet. Enfin, l’exemple libère le contexte de liaison et appelle la fonction [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


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



Comme « {ID de classe du moniker de classe} » est également un moyen de nommer un moniker de classe, vous pouvez utiliser la chaîne suivante pour nommer le moniker composite (le moniker de session composé du moniker de la classe) au lieu de la méthode illustrée dans l’exemple précédent.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Si le même utilisateur est connecté à chaque session pendant une activation inter-sessions, vous pouvez activer un processus serveur configuré pour s’exécuter dans le mode d’activation d’utilisateur interactif RunAs. Si différents utilisateurs sont connectés à chaque session, le serveur doit appeler la fonction [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir les droits d’utilisateur appropriés avant une activation réussie et la connexion peut se produire entre le client et le serveur. Pour ce faire, le serveur doit implémenter une interface [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personnalisée et passer l’implémentation à la procédure **CoInitializeSecurity**. Dans tous les cas, l’utilisateur client doit disposer des autorisations d' [**accès**](../com/accesspermission.md) et de [**lancement**](../com/launchpermission.md) appropriées spécifiées par l’application en cours d’exécution sur le serveur. Pour plus d’informations [, consultez sécurité dans com](../com/security-in-com.md).

 

Pour plus d’informations sur les monikers et les modes d’activation fournis par le système, consultez [monikers](../com/monikers.md), l’interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) et la [clé AppID](/windows/desktop/com/appid-key) dans la documentation com du kit de développement logiciel (SDK) de la plateforme.

 

 
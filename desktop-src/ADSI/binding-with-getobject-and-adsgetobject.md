---
title: Liaison avec GetObject et ADsGetObject
description: Les fonctions GetObject et ADsGetObject sont utilisées pour lier des objets de service d’annuaire sans authentification.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilisation de, liaison avec GetObject et ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941352"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Liaison avec GetObject et ADsGetObject

Les fonctions **GetObject** et [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) sont utilisées pour lier des objets de service d’annuaire sans authentification. L’application n’a pas besoin de fournir des informations d’identification lors de l’accès aux données du service d’annuaire. ADSI utilise le contexte de sécurité du thread appelant. Toutefois, en cas d’échec de l’authentification sécurisée, ADSI tente d’effectuer une liaison simple avec un nom d’utilisateur et un mot de passe Null. Si la liaison simple est réussie, le contexte utilisateur pour la liaison est Guest. Une liaison simple utilise l’authentification en texte clair. Étant donné qu’aucun nom d’utilisateur ou mot de passe n’est transmis sur le réseau, il ne s’agit pas d’un problème de sécurité.

La fonction **GetObject** est utilisée pour lier des objets de service d’annuaire dans des langages qui prennent en charge l’automatisation, comme Visual Basic. La fonction **GetObject** requiert une chaîne de moniker. Dans ADSI, la chaîne de liaison est la chaîne de moniker.

Dans les langages qui ne prennent pas directement en charge Automation, tels que C ou C++, ADSI fournit la fonction [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) pour la liaison aux objets de service d’annuaire. Vous pouvez également utiliser les fonctions [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) et [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) pour obtenir le même résultat que **GetObject**.

Pour un service s’exécutant sous le compte LocalSystem, le contexte de sécurité utilisé par **GetObject** et [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) dépend de l’ordinateur sur lequel le service s’exécute. Si le service s’exécute en tant que LocalSystem sur un contrôleur de domaine, le service dispose d’un accès complet au système pour Active Directory. Si le service n’est pas exécuté sur un contrôleur de périphérique, le service dispose des droits d’accès et des privilèges accordés au compte d’ordinateur de l’ordinateur sur lequel le service s’exécute. Cela est beaucoup moins puissant que l’accès au niveau du système.

## <a name="examples"></a>Exemples

L’exemple de code Visual Basic suivant montre comment utiliser la fonction **GetObject** pour établir une liaison à un objet.


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



L’exemple de code C++ suivant montre comment utiliser la fonction [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) pour effectuer une liaison à un objet.


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 
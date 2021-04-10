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
# <a name="binding-with-getobject-and-adsgetobject"></a><span data-ttu-id="8ad40-104">Liaison avec GetObject et ADsGetObject</span><span class="sxs-lookup"><span data-stu-id="8ad40-104">Binding With GetObject and ADsGetObject</span></span>

<span data-ttu-id="8ad40-105">Les fonctions **GetObject** et [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) sont utilisées pour lier des objets de service d’annuaire sans authentification.</span><span class="sxs-lookup"><span data-stu-id="8ad40-105">The **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) functions are used to bind to directory service objects with no authentication.</span></span> <span data-ttu-id="8ad40-106">L’application n’a pas besoin de fournir des informations d’identification lors de l’accès aux données du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8ad40-106">The application is not required to provide credentials when accessing directory service data.</span></span> <span data-ttu-id="8ad40-107">ADSI utilise le contexte de sécurité du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="8ad40-107">ADSI uses the security context of the calling thread.</span></span> <span data-ttu-id="8ad40-108">Toutefois, en cas d’échec de l’authentification sécurisée, ADSI tente d’effectuer une liaison simple avec un nom d’utilisateur et un mot de passe Null.</span><span class="sxs-lookup"><span data-stu-id="8ad40-108">However, if secure authentication fails, ADSI attempts to perform a simple bind with a null user name and null password.</span></span> <span data-ttu-id="8ad40-109">Si la liaison simple est réussie, le contexte utilisateur pour la liaison est Guest.</span><span class="sxs-lookup"><span data-stu-id="8ad40-109">If the simple bind succeeds, the user context for the binding is Guest.</span></span> <span data-ttu-id="8ad40-110">Une liaison simple utilise l’authentification en texte clair.</span><span class="sxs-lookup"><span data-stu-id="8ad40-110">A simple bind uses plaintext authentication.</span></span> <span data-ttu-id="8ad40-111">Étant donné qu’aucun nom d’utilisateur ou mot de passe n’est transmis sur le réseau, il ne s’agit pas d’un problème de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8ad40-111">Because no user name or password is transmitted over the network, this is not a security issue.</span></span>

<span data-ttu-id="8ad40-112">La fonction **GetObject** est utilisée pour lier des objets de service d’annuaire dans des langages qui prennent en charge l’automatisation, comme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8ad40-112">The **GetObject** function is used to bind to directory service objects in languages that support automation, such as Visual Basic.</span></span> <span data-ttu-id="8ad40-113">La fonction **GetObject** requiert une chaîne de moniker.</span><span class="sxs-lookup"><span data-stu-id="8ad40-113">The **GetObject** function requires a moniker string.</span></span> <span data-ttu-id="8ad40-114">Dans ADSI, la chaîne de liaison est la chaîne de moniker.</span><span class="sxs-lookup"><span data-stu-id="8ad40-114">In ADSI, the binding string is the moniker string.</span></span>

<span data-ttu-id="8ad40-115">Dans les langages qui ne prennent pas directement en charge Automation, tels que C ou C++, ADSI fournit la fonction [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) pour la liaison aux objets de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8ad40-115">In languages that do not directly support automation, such as C or C++, ADSI provides the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to directory service objects.</span></span> <span data-ttu-id="8ad40-116">Vous pouvez également utiliser les fonctions [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) et [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) pour obtenir le même résultat que **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="8ad40-116">Alternatively, the [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) and [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) functions can be used to achieve the same result as **GetObject**.</span></span>

<span data-ttu-id="8ad40-117">Pour un service s’exécutant sous le compte LocalSystem, le contexte de sécurité utilisé par **GetObject** et [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) dépend de l’ordinateur sur lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="8ad40-117">For a service running under the LocalSystem account, the security context used by **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depends on the computer on which the service is running.</span></span> <span data-ttu-id="8ad40-118">Si le service s’exécute en tant que LocalSystem sur un contrôleur de domaine, le service dispose d’un accès complet au système pour Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8ad40-118">If the service is running as LocalSystem on a domain controller, the service has full system-level access to Active Directory.</span></span> <span data-ttu-id="8ad40-119">Si le service n’est pas exécuté sur un contrôleur de périphérique, le service dispose des droits d’accès et des privilèges accordés au compte d’ordinateur de l’ordinateur sur lequel le service s’exécute. Cela est beaucoup moins puissant que l’accès au niveau du système.</span><span class="sxs-lookup"><span data-stu-id="8ad40-119">If the service is not running on a DC, the service has the access rights and privileges granted to the computer account for the computer on which the service is running; this is significantly less powerful than system-level access.</span></span>

## <a name="examples"></a><span data-ttu-id="8ad40-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="8ad40-120">Examples</span></span>

<span data-ttu-id="8ad40-121">L’exemple de code Visual Basic suivant montre comment utiliser la fonction **GetObject** pour établir une liaison à un objet.</span><span class="sxs-lookup"><span data-stu-id="8ad40-121">The following Visual Basic code example shows how to use the **GetObject** function to bind to an object.</span></span>


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



<span data-ttu-id="8ad40-122">L’exemple de code C++ suivant montre comment utiliser la fonction [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) pour effectuer une liaison à un objet.</span><span class="sxs-lookup"><span data-stu-id="8ad40-122">The following C++ code example shows how to use the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to an object.</span></span>


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



 

 
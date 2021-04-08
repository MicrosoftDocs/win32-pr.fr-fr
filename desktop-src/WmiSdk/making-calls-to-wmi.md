---
description: Les fournisseurs peuvent appeler des méthodes implémentées par WMI à partir de leurs implémentations de méthode.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Appels à WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034557"
---
# <a name="making-calls-to-wmi"></a><span data-ttu-id="ab660-103">Appels à WMI</span><span class="sxs-lookup"><span data-stu-id="ab660-103">Making Calls to WMI</span></span>

<span data-ttu-id="ab660-104">Les fournisseurs peuvent appeler des méthodes implémentées par WMI à partir de leurs implémentations de méthode.</span><span class="sxs-lookup"><span data-stu-id="ab660-104">Providers can call methods implemented by WMI from within their method implementations.</span></span> <span data-ttu-id="ab660-105">Toutefois, il existe des considérations spéciales lorsqu’un fournisseur appelle l’implémentation WMI d’une méthode [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) à partir de sa propre implémentation de la même méthode.</span><span class="sxs-lookup"><span data-stu-id="ab660-105">However, there are special considerations when a provider calls the WMI implementation of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method from within its own implementation of the same method.</span></span> <span data-ttu-id="ab660-106">Ces considérations sont importantes, que le fournisseur appelle la version synchrone ou asynchrone de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ab660-106">These considerations are important regardless of whether the provider calls the synchronous or asynchronous version of the method.</span></span>

<span data-ttu-id="ab660-107">Chaque méthode [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) qu’un fournisseur peut implémenter a un paramètre *pctX* , un pointeur vers une implémentation de l’interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="ab660-107">Each [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method that a provider can implement has a *pCtx* parameter, a pointer to an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface implementation.</span></span> <span data-ttu-id="ab660-108">Lorsque WMI appelle le fournisseur, WMI transmet un pointeur valide dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ab660-108">When WMI calls the provider, WMI passes a valid pointer in this parameter.</span></span> <span data-ttu-id="ab660-109">Un fournisseur doit toujours passer ce même pointeur dans tous les appels à WMI qu’il effectue lors du traitement des demandes.</span><span class="sxs-lookup"><span data-stu-id="ab660-109">A provider must always pass this same pointer in any calls to WMI that they make while servicing requests.</span></span> <span data-ttu-id="ab660-110">Le fait de définir *pctX* de manière appropriée peut entraîner le démarrage d’une boucle infinie par WMI.</span><span class="sxs-lookup"><span data-stu-id="ab660-110">Neglecting to set *pCtx* appropriately can cause WMI to start an infinite loop.</span></span>

<span data-ttu-id="ab660-111">L’exemple de code suivant montre la méthode correcte pour appeler l’implémentation WMI de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) à partir d’une implémentation de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="ab660-111">The following code example shows the correct way to call the WMI implementation of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) from within an implementation of [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



<span data-ttu-id="ab660-112">L’exemple de code C++ dans cette rubrique requiert les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="ab660-112">The C++ code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="ab660-113">Les fournisseurs d’instance, de classe et de propriété ne doivent émettre aucun appel à WMI demandant la modification de données pendant la maintenance d’une demande de lecture.</span><span class="sxs-lookup"><span data-stu-id="ab660-113">Instance, class, and property providers must not issue any calls to WMI requesting the modification of data while servicing a read request.</span></span> <span data-ttu-id="ab660-114">Les seuls fournisseurs qui sont des exceptions à cette règle sont des fournisseurs push.</span><span class="sxs-lookup"><span data-stu-id="ab660-114">The only providers that are exceptions to this rule are push providers.</span></span> <span data-ttu-id="ab660-115">Un fournisseur push est un fournisseur de classe qui stocke des données dans l’espace de stockage WMI et s’appuie sur WMI pour gérer les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="ab660-115">A push provider is a class provider that stores data in the WMI repository and relies on WMI to handle requests from clients.</span></span> <span data-ttu-id="ab660-116">Lors du traitement d’une demande de lecture, un fournisseur Push peut mettre à jour l’espace de stockage WMI, mais doit définir le paramètre *lFlags* sur la **\_ \_ \_ mise à jour du propriétaire de l’indicateur WBEM** dans l’appel [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) approprié.</span><span class="sxs-lookup"><span data-stu-id="ab660-116">While servicing a read request, a push provider can update the WMI repository, but must set the *lFlags* parameter to **WBEM\_FLAG\_OWNER\_UPDATE** in the appropriate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call.</span></span>

<span data-ttu-id="ab660-117">Les fournisseurs d’événements ne doivent pas apporter de modifications de classe lors de la maintenance d’un appel.</span><span class="sxs-lookup"><span data-stu-id="ab660-117">Event providers must not make any class changes while servicing a call.</span></span> <span data-ttu-id="ab660-118">Ils ne peuvent pas non plus émettre des appels liés aux événements, tels que la modification d’un filtre d’événement.</span><span class="sxs-lookup"><span data-stu-id="ab660-118">They also cannot issue any event-related calls, such as modifying an event filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab660-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab660-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab660-120">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="ab660-120">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="ab660-121">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="ab660-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="ab660-122">Sécurisation de votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="ab660-122">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 




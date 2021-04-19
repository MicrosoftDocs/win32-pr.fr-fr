---
description: Si le service Web XML auquel vous souhaitez accéder a été créé en exposant une application COM+, pensez à y accéder en mode de l’objet activé par le client (CAO), ce qui permet d’éviter la génération d’un proxy au moment de l’exécution et d’améliorer les performances à l’aide de connexions persistantes.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Accès aux services Web XML en mode CAO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544577"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a><span data-ttu-id="d2f2b-103">Accès aux services Web XML en mode CAO</span><span class="sxs-lookup"><span data-stu-id="d2f2b-103">Accessing XML Web Services in CAO Mode</span></span>

<span data-ttu-id="d2f2b-104">Si le service Web XML auquel vous souhaitez accéder a été créé en exposant une application COM+, pensez à y accéder en mode de l’objet activé par le client (CAO), ce qui permet d’éviter la génération d’un proxy au moment de l’exécution et d’améliorer les performances à l’aide de connexions persistantes.</span><span class="sxs-lookup"><span data-stu-id="d2f2b-104">If the XML web service you want to access was created by exposing a COM+ application, consider accessing it in client-activated object (CAO) mode, which avoids the run-time generation of a proxy and increases performance by using persistent connections.</span></span> <span data-ttu-id="d2f2b-105">Pour accéder à un service Web XML en mode CAO, commencez par [Exporter](exporting-a-soap-enabled-application.md) l’application compatible SOAP correspondante à partir de votre serveur en mode proxy, puis [importez](importing-a-soap-enabled-application.md) l’application dans le client à partir duquel vous souhaitez accéder à l’application en tant que service Web XML.</span><span class="sxs-lookup"><span data-stu-id="d2f2b-105">To access an XML web service in CAO mode, first [export](exporting-a-soap-enabled-application.md) the corresponding SOAP-enabled application from your server in proxy mode and then [import](importing-a-soap-enabled-application.md) the application into the client from which you want to access the application as an XML web service.</span></span> <span data-ttu-id="d2f2b-106">Les composants de l’application peuvent ensuite être instanciés sur le client comme les composants des applications locales, par exemple en utilisant **GetObject** et [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="d2f2b-106">The application's components can then be instantiated on the client just like the components of local applications—for example, using **GetObject** and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="user-interface"></a><span data-ttu-id="d2f2b-107">Interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d2f2b-107">User Interface</span></span>

<span data-ttu-id="d2f2b-108">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="d2f2b-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="d2f2b-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d2f2b-109">Visual Basic</span></span>

<span data-ttu-id="d2f2b-110">L’Visual Basic fragment de code suivant illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service Web XML en mode CAO.</span><span class="sxs-lookup"><span data-stu-id="d2f2b-110">The following Visual Basic code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a><span data-ttu-id="d2f2b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d2f2b-111">C/C++</span></span>

<span data-ttu-id="d2f2b-112">Le fragment de code suivant illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service Web XML en mode CAO.</span><span class="sxs-lookup"><span data-stu-id="d2f2b-112">The following code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a><span data-ttu-id="d2f2b-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2f2b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f2b-114">Accès aux services Web XML en mode WKO</span><span class="sxs-lookup"><span data-stu-id="d2f2b-114">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="d2f2b-115">Vue d’ensemble du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="d2f2b-115">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="d2f2b-116">Création de services Web XML</span><span class="sxs-lookup"><span data-stu-id="d2f2b-116">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="d2f2b-117">Sécurisation des services Web XML</span><span class="sxs-lookup"><span data-stu-id="d2f2b-117">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 

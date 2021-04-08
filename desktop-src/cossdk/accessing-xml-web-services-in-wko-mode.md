---
description: Vous pouvez accéder à un service Web XML et l’utiliser, même si ce service Web XML n’a pas été créé à l’aide de COM+ ou même de Microsoft Windows, à condition que le service Web XML publie une description WSDL de sa syntaxe.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Accès aux services Web XML en mode WKO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748196"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a><span data-ttu-id="57585-103">Accès aux services Web XML en mode WKO</span><span class="sxs-lookup"><span data-stu-id="57585-103">Accessing XML Web Services in WKO Mode</span></span>

<span data-ttu-id="57585-104">Vous pouvez accéder à un service Web XML et l’utiliser, même si ce service Web XML n’a pas été créé à l’aide de COM+ ou même de Microsoft Windows, à condition que le service Web XML publie une description WSDL de sa syntaxe.</span><span class="sxs-lookup"><span data-stu-id="57585-104">You can access and use any XML web service, even if that XML web service was not created using COM+ or even Microsoft Windows, as long as the XML Web Service publishes a WSDL description of its syntax.</span></span> <span data-ttu-id="57585-105">Il vous suffit de créer une instance du composant à l’aide du moniker SOAP : WSDL = URL, où URL est l’URL de la description WSDL du service Web XML auquel vous souhaitez accéder.</span><span class="sxs-lookup"><span data-stu-id="57585-105">Just create an instance of the component by using the soap:wsdl=URL moniker, where URL is the URL of the WSDL description of the XML web service you want to access.</span></span> <span data-ttu-id="57585-106">Il s’agit du mode d’objet WKO (bien connu) qui consiste à accéder aux services Web XML.</span><span class="sxs-lookup"><span data-stu-id="57585-106">This is the well-known object (WKO) mode of accessing XML web services.</span></span>

<span data-ttu-id="57585-107">Les méthodes de l’objet peuvent être appelées sans considérations particulières.</span><span class="sxs-lookup"><span data-stu-id="57585-107">The object's methods can be called without any special considerations.</span></span> <span data-ttu-id="57585-108">Le service Web XML est accessible via une requête SOAP et la réponse est interprétée en toute transparence.</span><span class="sxs-lookup"><span data-stu-id="57585-108">The XML web service is accessed via a SOAP query, and the response is interpreted transparently.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="57585-109">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="57585-109">Component Services Administrative Tool</span></span>

<span data-ttu-id="57585-110">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="57585-110">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="57585-111">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="57585-111">Visual Basic</span></span>

<span data-ttu-id="57585-112">Le fragment de code Microsoft Visual Basic suivant illustre l’utilisation d’un service Web XML en mode WKO.</span><span class="sxs-lookup"><span data-stu-id="57585-112">The following Microsoft Visual Basic code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



<span data-ttu-id="57585-113">Dans ce fragment de code qui illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service Web XML, ServerName est le nom de domaine complet du serveur qui offre le service Web XML. vroot est le répertoire racine virtuel IIS à partir duquel le service Web XML est exposé. et progID est le ProgID du composant que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="57585-113">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="cc"></a><span data-ttu-id="57585-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="57585-114">C/C++</span></span>

<span data-ttu-id="57585-115">Le fragment de code suivant illustre l’utilisation d’un service Web XML en mode WKO.</span><span class="sxs-lookup"><span data-stu-id="57585-115">The following code fragment illustrates the use of an XML web service in WKO mode.</span></span>


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



<span data-ttu-id="57585-116">Dans ce fragment de code qui illustre l’utilisation d’un composant d’une application COM+ exposée en tant que service Web XML, ServerName est le nom de domaine complet du serveur qui offre le service Web XML. vroot est le répertoire racine virtuel IIS à partir duquel le service Web XML est exposé. et progID est le ProgID du composant que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="57585-116">In this code fragment, which illustrates the use of a component of a COM+ application that has been exposed as an XML web service, servername is the fully qualified domain name of the server offering the XML web service; vroot is the IIS virtual root directory from which the XML web service is exposed; and progID is the ProgID of the component you want to use.</span></span>

## <a name="remarks"></a><span data-ttu-id="57585-117">Notes</span><span class="sxs-lookup"><span data-stu-id="57585-117">Remarks</span></span>

<span data-ttu-id="57585-118">Lors du premier accès à un service Web XML en mode WKO, COM+ génère un client proxy et le compile en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="57585-118">When an XML web service is first accessed in WKO mode, COM+ generates a proxy client and compiles it in the background.</span></span> <span data-ttu-id="57585-119">Cette génération au moment de l’exécution et l’absence de connexions persistantes en mode WKO entraînent une réduction significative des performances par rapport au mode CAO.</span><span class="sxs-lookup"><span data-stu-id="57585-119">This run-time generation and the lack of persistent connections in WKO mode results in significantly reduced performance in comparison to CAO mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57585-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57585-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57585-121">Accès aux services Web XML en mode CAO</span><span class="sxs-lookup"><span data-stu-id="57585-121">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="57585-122">Vue d’ensemble du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="57585-122">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="57585-123">Création de services Web XML</span><span class="sxs-lookup"><span data-stu-id="57585-123">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="57585-124">Sécurisation des services Web XML</span><span class="sxs-lookup"><span data-stu-id="57585-124">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 




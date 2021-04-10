---
title: Inscription du fournisseur de services
description: Inscription du fournisseur de services
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Gestionnaire de périphériques, inscrire des fournisseurs de services
- Gestionnaire de périphériques, inscrire des fournisseurs de services
- Guide de programmation, inscrire des fournisseurs de services
- fournisseurs de services, inscrire des fournisseurs de services
- création de fournisseurs de services, inscription de fournisseurs de services
- inscription des fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028748"
---
# <a name="registering-the-service-provider"></a><span data-ttu-id="4e288-109">Inscription du fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="4e288-109">Registering the Service Provider</span></span>

<span data-ttu-id="4e288-110">En plus d’être inscrit en tant qu’objet COM, un fournisseur de services doit être inscrit en tant que plug-in pour Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="4e288-110">In addition to being registered as a COM object, a service provider must be registered as a plug-in to Windows Media Device Manager.</span></span> <span data-ttu-id="4e288-111">Pour s’inscrire, un fournisseur de services doit créer la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="4e288-111">To register, a service provider must create the following registry key:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

<span data-ttu-id="4e288-112">Dans cette clé, < le nom de votre *fournisseur de services* > est le nom de votre dll ; par exemple, l’exemple de fournisseur de services utilise MsHDSP.</span><span class="sxs-lookup"><span data-stu-id="4e288-112">In this key, < *your service provider name* > is the name of your DLL; for example, the sample service provider uses MsHDSP.</span></span> <span data-ttu-id="4e288-113">La clé ProgID doit avoir une valeur de chaîne qui correspond au CLSID de votre fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4e288-113">The ProgID key should have a string value that corresponds to the CLSID of your service provider.</span></span> <span data-ttu-id="4e288-114">Par exemple, l’exemple de fournisseur de services a la valeur « MDServiceProviderHD. MDServiceProviderHD ».</span><span class="sxs-lookup"><span data-stu-id="4e288-114">For instance, the sample service provider has the value "MDServiceProviderHD.MDServiceProviderHD".</span></span>

<span data-ttu-id="4e288-115">L’exemple d’implémentation du fournisseur de services de DLLRegisterServer dans MDSP. cpp ajoute cette clé de registre lorsque vous inscrivez l’exemple de DLL du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="4e288-115">The sample service provider's implementation of DLLRegisterServer in Mdsp.cpp adds this registry key when you register the sample service provider DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e288-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e288-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e288-117">**Création d’un fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="4e288-117">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 





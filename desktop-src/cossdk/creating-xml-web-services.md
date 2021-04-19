---
description: Toutes les applications COM+ peuvent être exposées en tant que service Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Création de services Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516781"
---
# <a name="creating-xml-web-services"></a><span data-ttu-id="5aa50-103">Création de services Web XML</span><span class="sxs-lookup"><span data-stu-id="5aa50-103">Creating XML Web Services</span></span>

<span data-ttu-id="5aa50-104">Toutes les applications COM+ peuvent être exposées en tant que service Web XML.</span><span class="sxs-lookup"><span data-stu-id="5aa50-104">Any COM+ application can be exposed as an XML web service.</span></span> <span data-ttu-id="5aa50-105">Les méthodes des interfaces par défaut des composants d’applications configurés (composants dans le catalogue COM+ serveurs) peuvent ensuite être appelées à distance.</span><span class="sxs-lookup"><span data-stu-id="5aa50-105">The methods in the default interfaces of the applications configured components (components in the servers COM+ catalog) can then be called remotely.</span></span> <span data-ttu-id="5aa50-106">Vous pouvez utiliser l’outil d’administration Services de composants pour créer un répertoire racine virtuel IIS à partir duquel les méthodes de composant peuvent être appelées à l’aide de SOAP.</span><span class="sxs-lookup"><span data-stu-id="5aa50-106">You can use the Component Services administrative tool to create an IIS virtual root directory from which the component methods can be called by using SOAP.</span></span>

> [!Note]  
> <span data-ttu-id="5aa50-107">Le .NET Framework doit être installé sur votre ordinateur afin d’exposer une application COM+ en tant que service Web XML.</span><span class="sxs-lookup"><span data-stu-id="5aa50-107">The .NET Framework must be installed on your computer in order to expose a COM+ application as an XML web service.</span></span>

 

<span data-ttu-id="5aa50-108">**Pour exposer une application COM+ en tant que service Web XML**</span><span class="sxs-lookup"><span data-stu-id="5aa50-108">**To expose a COM+ application as an XML web service**</span></span>

1.  <span data-ttu-id="5aa50-109">Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="5aa50-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="5aa50-110">Cliquez avec le bouton droit sur l’application que vous souhaitez exposer en tant que service Web XML, puis choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="5aa50-110">Right-click the application you want to expose as an XML web service, and choose **Properties**.</span></span>

3.  <span data-ttu-id="5aa50-111">Dans la boîte de dialogue Propriétés, cliquez sur l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="5aa50-111">Click the **Activation** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="5aa50-112">Activez la case à cocher **utilise le protocole SOAP** .</span><span class="sxs-lookup"><span data-stu-id="5aa50-112">Select the **Uses SOAP** check box.</span></span>

5.  <span data-ttu-id="5aa50-113">Dans la zone de texte **vroot SOAP** , entrez le nom du répertoire racine virtuel IIS à partir duquel vous pouvez accéder à distance aux méthodes des composants.</span><span class="sxs-lookup"><span data-stu-id="5aa50-113">In the **SOAP VRoot** text box, enter the name of the IIS virtual root directory from which the components methods can be accessed remotely.</span></span> <span data-ttu-id="5aa50-114">Notez qu’un VRoot SOAP ne peut pas être un sous-répertoire d’un autre répertoire VRoot SOAP.</span><span class="sxs-lookup"><span data-stu-id="5aa50-114">Note that a SOAP VRoot cannot be a subdirectory of another SOAP VRoot directory.</span></span>

6.  <span data-ttu-id="5aa50-115">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5aa50-115">Click **OK**.</span></span>

    <span data-ttu-id="5aa50-116">Si vous spécifiez le répertoire racine virtuel IIS en tant que *vroot* et si le nom de domaine complet de votre serveur est *ServerName*, l’URL où votre composant est exposé en tant que service Web XML est https://*ServerName* / *vroot*/.</span><span class="sxs-lookup"><span data-stu-id="5aa50-116">If you specify the IIS virtual root directory as *vroot* and if your servers fully qualified domain name is *servername*, the URL where your component is exposed as an XML web service is https://*servername*/*vroot*/.</span></span>

    <span data-ttu-id="5aa50-117">Le répertoire correspondant dans votre système de fichiers est \\ Windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ; COM+ place plusieurs fichiers de configuration et des programmes ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="5aa50-117">The corresponding directory in your file system is \\windows\\system32\\com\\SoapVRoots\\*vroot*\\; COM+ places several configuration files and ASP.NET programs there.</span></span> <span data-ttu-id="5aa50-118">Pour un service Web XML soumis à une charge importante, vous pouvez ajuster les paramètres stockés dans le web.config de fichiers. Pour plus d’informations sur ce fichier, consultez la documentation d’IIS.</span><span class="sxs-lookup"><span data-stu-id="5aa50-118">For an XML web service under heavy load, you may want to adjust the parameters stored in the file web.config. For information about this file, consult the IIS documentation.</span></span>

    <span data-ttu-id="5aa50-119">Les paramètres de sécurité par défaut d’une application COM+ exposée en tant que service Web XML varient en fonction de la version du .NET Framework installée.</span><span class="sxs-lookup"><span data-stu-id="5aa50-119">The default security settings for a COM+ application exposed as an XML web service differ depending on which version of the .NET Framework is installed.</span></span> <span data-ttu-id="5aa50-120">Si la version 1,0 est installée, les services Web XML ne sont pas sécurisés par défaut. tous les appels sont acceptés et aucun chiffrement n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5aa50-120">If version 1.0 is installed, XML web services are nonsecure by default; all calls are accepted and no encryption is used.</span></span> <span data-ttu-id="5aa50-121">Si la version 1,1 ou une version ultérieure est installée, les services Web XML sont sécurisés par défaut. les appelants doivent être authentifiés et le chiffrement est requis.</span><span class="sxs-lookup"><span data-stu-id="5aa50-121">If version 1.1 or later is installed, XML web services are secure by default; callers must be authenticated and encryption is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa50-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5aa50-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa50-123">Accès aux services Web XML en mode CAO</span><span class="sxs-lookup"><span data-stu-id="5aa50-123">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="5aa50-124">Accès aux services Web XML en mode WKO</span><span class="sxs-lookup"><span data-stu-id="5aa50-124">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="5aa50-125">Vue d’ensemble du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="5aa50-125">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="5aa50-126">Sécurisation des services Web XML</span><span class="sxs-lookup"><span data-stu-id="5aa50-126">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 




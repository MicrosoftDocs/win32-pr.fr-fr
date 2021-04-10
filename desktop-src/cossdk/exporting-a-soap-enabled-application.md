---
description: Lorsque vous utilisez COM+ pour créer un service Web XML, ce service peut être utilisé par n’importe quel client autorisé, y compris ceux qui n’utilisent pas COM+ ou même Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportation d’une application SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861373"
---
# <a name="exporting-a-soap-enabled-application"></a><span data-ttu-id="cc5e8-103">Exportation d’une application SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="cc5e8-103">Exporting a SOAP-Enabled Application</span></span>

<span data-ttu-id="cc5e8-104">Lorsque vous utilisez COM+ pour créer un service Web XML, ce service peut être utilisé par n’importe quel client autorisé, y compris ceux qui n’utilisent pas COM+ ou même Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-104">When you use COM+ to create an XML web service, that service can be used by any authorized client, including those not using COM+ or even Microsoft Windows.</span></span> <span data-ttu-id="cc5e8-105">Toutefois, l’utilisation d’un service Web COM+ en mode CAO (client-Activated Object) à partir d’une application cliente COM+ est particulièrement simple.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-105">However, using a COM+ web service in client-activated object (CAO) mode from a COM+ client application is especially easy.</span></span> <span data-ttu-id="cc5e8-106">Exportez simplement l’application compatible SOAP en mode proxy, puis [importez](importing-a-soap-enabled-application.md) -la dans le client pour lequel vous souhaitez accéder au service Web XML correspondant.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-106">Just export the SOAP-enabled application in proxy mode, and then [import](importing-a-soap-enabled-application.md) it into the client for which you want to access the corresponding XML web service.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="cc5e8-107">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="cc5e8-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="cc5e8-108">Pour exporter une application compatible SOAP à partir d’un serveur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cc5e8-108">To export a SOAP-enabled application from a server, use the following steps:</span></span>

1.  <span data-ttu-id="cc5e8-109">Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-109">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you want to manage.</span></span>

2.  <span data-ttu-id="cc5e8-110">Cliquez avec le bouton droit sur le composant que vous souhaitez exposer en tant que service Web XML, puis choisissez **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-110">Right-click the component you want to expose as an XML web service, and choose **Export**.</span></span> <span data-ttu-id="cc5e8-111">L' **Assistant exportation d’application com+** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-111">The **COM+ Application Export Wizard** appears.</span></span>

3.  <span data-ttu-id="cc5e8-112">Dans la zone de texte intitulée **Entrez le chemin d’accès complet et le nom du fichier d’application à créer**, entrez le chemin d’accès complet et le nom du fichier MSI qui contiendra l’application exportée, ou cliquez sur **Parcourir** pour sélectionner le chemin d’accès complet et le nom de fichier à l’aide d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-112">In the text box labeled **Enter the full path and filename for the application file to be created**, enter the full path and filename for the MSI file that will contain the exported application, or click **Browse** to select the full path and filename using a dialog box.</span></span>

4.  <span data-ttu-id="cc5e8-113">Sous **Exporter en tant que**, sélectionnez la case **d’option proxy d’application-installer sur d’autres ordinateurs pour activer l’accès à cet ordinateur** .</span><span class="sxs-lookup"><span data-stu-id="cc5e8-113">Under **Export As**, select the **Application Proxy – Install on other machines to enable access to this machine** radio button.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="cc5e8-114">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cc5e8-114">Visual Basic</span></span>

<span data-ttu-id="cc5e8-115">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-115">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="cc5e8-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="cc5e8-116">C/C++</span></span>

<span data-ttu-id="cc5e8-117">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-117">Does not apply.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc5e8-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc5e8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc5e8-119">Vue d’ensemble du service SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="cc5e8-119">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="cc5e8-120">Création de services Web XML</span><span class="sxs-lookup"><span data-stu-id="cc5e8-120">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="cc5e8-121">Importation d’une application SOAP-Enabled</span><span class="sxs-lookup"><span data-stu-id="cc5e8-121">Importing a SOAP-Enabled Application</span></span>](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 




---
description: Deux exemples WSDAPI sont inclus avec le SDK Windows pour Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Exemples WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754957"
---
# <a name="wsdapi-samples"></a><span data-ttu-id="13520-103">Exemples WSDAPI</span><span class="sxs-lookup"><span data-stu-id="13520-103">WSDAPI Samples</span></span>

<span data-ttu-id="13520-104">Deux exemples WSDAPI sont inclus avec le SDK Windows pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="13520-104">There are two WSDAPI samples included with the Windows SDK for Windows Server 2008.</span></span> <span data-ttu-id="13520-105">Le code source des exemples se trouve dans <Windows SDK Install Folder> \\ Samples \\ Web \\ wsdapi.</span><span class="sxs-lookup"><span data-stu-id="13520-105">The source code for the samples can be found in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI.</span></span> <span data-ttu-id="13520-106">Cette version du kit de développement logiciel (SDK) est disponible à partir du [Centre de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="13520-106">This version of the SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span> <span data-ttu-id="13520-107">Les exemples ne sont pas disponibles dans le kit de développement logiciel (SDK) Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13520-107">The samples are not available in the Windows Vista SDK.</span></span>

<span data-ttu-id="13520-108">L’exemple Stock Quote (situé dans <Windows SDK Install Folder> \\ Samples \\ Web \\ wsdapi \\ StockQuote) illustre un service avec des fonctionnalités de messagerie de base.</span><span class="sxs-lookup"><span data-stu-id="13520-108">The stock quote sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\StockQuote) demonstrates a service with basic messaging functionality.</span></span> <span data-ttu-id="13520-109">L’exemple de service de fichiers (situé dans <Windows SDK Install Folder> \\ Samples \\ Web \\ wsdapi \\ FileService) illustre un service avec des fonctionnalités avancées, telles que la messagerie asynchrone, les pièces jointes et les événements.</span><span class="sxs-lookup"><span data-stu-id="13520-109">The file service sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\FileService) demonstrates a service with advanced functionality, such as asynchronous messaging, attachments, and eventing.</span></span>

<span data-ttu-id="13520-110">Les deux exemples incluent les types de fichiers suivants.</span><span class="sxs-lookup"><span data-stu-id="13520-110">Both samples include the following types of files.</span></span>

-   <span data-ttu-id="13520-111">Fichiers WSDL qui contiennent les descriptions de service.</span><span class="sxs-lookup"><span data-stu-id="13520-111">WSDL files that contain the service descriptions.</span></span>
-   <span data-ttu-id="13520-112">[Fichiers de configuration WsdCodeGen](wsdcodegen-configuration-file.md) utilisés pour générer le code wsdapi.</span><span class="sxs-lookup"><span data-stu-id="13520-112">[WsdCodeGen configuration files](wsdcodegen-configuration-file.md) used to generate WSDAPI code.</span></span>
-   <span data-ttu-id="13520-113">Fichiers sources et d’en-tête C++ générés.</span><span class="sxs-lookup"><span data-stu-id="13520-113">Generated C++ header and source files.</span></span>
-   <span data-ttu-id="13520-114">Fichiers d’implémentation du client et du service.</span><span class="sxs-lookup"><span data-stu-id="13520-114">Client and service implementation files.</span></span>
-   <span data-ttu-id="13520-115">Fichiers projet et solution Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="13520-115">Visual Studio project and solution files.</span></span>

<span data-ttu-id="13520-116">Les deux exemples implémentent les hôtes d’appareils ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), les proxys d’appareil ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) et les proxys de service ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span><span class="sxs-lookup"><span data-stu-id="13520-116">Both samples implement device hosts ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), device proxies ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)), and service proxies ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span></span> <span data-ttu-id="13520-117">En outre, l’exemple de service de fichiers montre l’utilisation de la messagerie asynchrone ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), des pièces jointes ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) et des événements.</span><span class="sxs-lookup"><span data-stu-id="13520-117">In addition, the file service sample demonstrates the use of asynchronous messaging ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), attachments ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) and eventing.</span></span>

<span data-ttu-id="13520-118">Les fichiers FileServiceContract. vcproj et StockQuoteContract. vcproj inclus avec les exemples appellent [WsdCodeGen](web-services-for-devices-code-generator.md) pour générer des fichiers d’en-tête C++ et des fichiers sources à partir du fichier WSDL spécifié dans le fichier de configuration WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="13520-118">The FileServiceContract.vcproj and StockQuoteContract.vcproj files included with the samples call [WsdCodeGen](web-services-for-devices-code-generator.md) to generate C++ header and source files from the WSDL file specified in the WsdCodeGen configuration file.</span></span> <span data-ttu-id="13520-119">Cela signifie que si l’exemple de fichier de configuration WSDL ou WsdCodeGen est modifié et que l’exemple de projet est régénéré, WsdCodeGen génère automatiquement de nouveaux fichiers d’en-tête et sources qui reflètent les modifications.</span><span class="sxs-lookup"><span data-stu-id="13520-119">This means that if the sample WSDL or WsdCodeGen configuration file is changed and the sample project is rebuilt, WsdCodeGen automatically generates new header and source files that reflect the changes.</span></span> <span data-ttu-id="13520-120">Il s’agit de la méthode recommandée pour générer des applications WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="13520-120">This is the preferred method for building WSDAPI applications.</span></span> <span data-ttu-id="13520-121">WsdCodeGen est généralement appelé à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="13520-121">WsdCodeGen is usually called from the command line.</span></span> <span data-ttu-id="13520-122">Ouvrez le \* fichier. vcproj approprié pour afficher les exemples d’appels de ligne de commande WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="13520-122">Open the relevant \*.vcproj file to view the example WsdCodeGen command line calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13520-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13520-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13520-124">Développement d’applications WSD sur Windows</span><span class="sxs-lookup"><span data-stu-id="13520-124">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> </dl>

 

 




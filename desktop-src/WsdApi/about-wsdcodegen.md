---
description: Décrit les fichiers d’entrée utilisés par WsdCodeGen et les fichiers de sortie générés par WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: À propos de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034306"
---
# <a name="about-wsdcodegen"></a><span data-ttu-id="30456-103">À propos de WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="30456-103">About WsdCodeGen</span></span>

<span data-ttu-id="30456-104">WsdCodeGen utilise un fichier de configuration XML pour déterminer l’emplacement des métadonnées du service.</span><span class="sxs-lookup"><span data-stu-id="30456-104">WsdCodeGen uses an XML configuration file to determine the location of the service metadata.</span></span> <span data-ttu-id="30456-105">Le fichier de configuration est également utilisé pour définir les noms d’interface, les GUID d’interface, les noms de classe, les noms de méthodes et d’autres identificateurs.</span><span class="sxs-lookup"><span data-stu-id="30456-105">The configuration file is also used to define interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> <span data-ttu-id="30456-106">Pour plus d’informations sur ce fichier, consultez [WsdCodeGen configuration file](wsdcodegen-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="30456-106">For more information about this file, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span></span>

<span data-ttu-id="30456-107">WsdCodeGen requiert deux types de fichiers d’entrée : un fichier de configuration XML et un ou plusieurs fichiers de description de service (fichiers WSDL et/ou XSD).</span><span class="sxs-lookup"><span data-stu-id="30456-107">WsdCodeGen requires two types of input files: an XML configuration file and one or more service description files (WSDL and/or XSD files).</span></span> <span data-ttu-id="30456-108">WsdCodeGen traite ces fichiers d’entrée et génère deux types de fichiers de sortie : les fichiers d’interface et les fichiers d’en-tête/source.</span><span class="sxs-lookup"><span data-stu-id="30456-108">WsdCodeGen processes these input files and generates two type of output files: interface files and header/source files.</span></span>

## <a name="input-files"></a><span data-ttu-id="30456-109">Fichiers d’entrée</span><span class="sxs-lookup"><span data-stu-id="30456-109">Input Files</span></span>



| <span data-ttu-id="30456-110">Type</span><span class="sxs-lookup"><span data-stu-id="30456-110">Type</span></span>                      | <span data-ttu-id="30456-111">Description</span><span class="sxs-lookup"><span data-stu-id="30456-111">Description</span></span>                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30456-112">Fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="30456-112">Configuration file</span></span>        | <span data-ttu-id="30456-113">Fichier XML qui indique l’emplacement des métadonnées du service et définit les noms d’interface, les GUID d’interface, les noms de classe, les noms de méthodes et d’autres identificateurs.</span><span class="sxs-lookup"><span data-stu-id="30456-113">An XML file that indicates the location of the service metadata and defines interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> |
| <span data-ttu-id="30456-114">Fichiers de description de service</span><span class="sxs-lookup"><span data-stu-id="30456-114">Service description files</span></span> | <span data-ttu-id="30456-115">Un ou plusieurs fichiers WSDL ou XSD qui décrivent les services à implémenter sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="30456-115">One or more WSDL or XSD files that describes the services to implement on the device.</span></span>                                                                           |



 

## <a name="output-files"></a><span data-ttu-id="30456-116">Fichiers de sortie</span><span class="sxs-lookup"><span data-stu-id="30456-116">Output Files</span></span>



| <span data-ttu-id="30456-117">Type</span><span class="sxs-lookup"><span data-stu-id="30456-117">Type</span></span>                        | <span data-ttu-id="30456-118">Description</span><span class="sxs-lookup"><span data-stu-id="30456-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30456-119">Fichiers d’interface</span><span class="sxs-lookup"><span data-stu-id="30456-119">Interface files</span></span>             | <span data-ttu-id="30456-120">Fichier IDL (Interface Definition Language) qui peut être utilisé avec le compilateur MIDL pour produire un fichier d’en-tête d’interface.</span><span class="sxs-lookup"><span data-stu-id="30456-120">An IDL (Interface Definition Language) file that can be used with the MIDL compiler to produce an interface header file.</span></span> <span data-ttu-id="30456-121">Les clients WSDAPI et les services WSDAPI peuvent utiliser ce fichier d’interface.</span><span class="sxs-lookup"><span data-stu-id="30456-121">WSDAPI clients and WSDAPI services can use this interface file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="30456-122">Fichiers source et en-tête C++</span><span class="sxs-lookup"><span data-stu-id="30456-122">C++ header and source files</span></span> | <span data-ttu-id="30456-123">Fichiers C++ qui décrivent le contrat de message, l’espace de noms et les informations de type.</span><span class="sxs-lookup"><span data-stu-id="30456-123">C++ files that describe the message contract, namespace, and type information.</span></span> <span data-ttu-id="30456-124">Ils peuvent contenir du code proxy et/ou du code stub.</span><span class="sxs-lookup"><span data-stu-id="30456-124">They may contain proxy code and/or stub code.</span></span> <span data-ttu-id="30456-125">Le code proxy implémente l’interface d’un service et traduit les appels de méthode de service en opérations WSDAPI qui effectuent des demandes de service.</span><span class="sxs-lookup"><span data-stu-id="30456-125">Proxy code implements a service's interface and translates service method calls into WSDAPI operations that make service requests.</span></span> <span data-ttu-id="30456-126">Le code stub traduit les demandes du service WSDAPI en code qui appelle les méthodes de service.</span><span class="sxs-lookup"><span data-stu-id="30456-126">Stub code translates WSDAPI service requests into code that calls service methods.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="30456-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30456-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30456-128">Générateur de code des services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="30456-128">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="30456-129">Utilisation de WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="30456-129">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




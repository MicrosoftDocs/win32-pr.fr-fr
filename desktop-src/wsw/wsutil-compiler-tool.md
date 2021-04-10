---
title: Outil compilateur WsUtil
description: L’outil compilateur de services Web Windows, WsUtil.exe, prend en charge le modèle de service et la sérialisation des types de données. Il traite les documents WSDL, de schéma et de stratégie XML et génère des en-têtes et des fichiers sources C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Services Web de l’outil compilateur WsUtil pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941485"
---
# <a name="wsutil-compiler-tool"></a><span data-ttu-id="30eb8-107">Outil compilateur WsUtil</span><span class="sxs-lookup"><span data-stu-id="30eb8-107">WsUtil Compiler tool</span></span>

<span data-ttu-id="30eb8-108">L’outil compilateur de services Web Windows, WsUtil.exe, prend en charge le [modèle de service](service-model-layer-overview.md) et la [sérialisation](serialization.md) des types de données.</span><span class="sxs-lookup"><span data-stu-id="30eb8-108">The Windows Web Services compiler tool, WsUtil.exe, supports the [service model](service-model-layer-overview.md) and [serialization](serialization.md) of data types.</span></span> <span data-ttu-id="30eb8-109">Il traite les documents WSDL, de schéma et de stratégie XML et génère des en-têtes et des fichiers sources C.</span><span class="sxs-lookup"><span data-stu-id="30eb8-109">It processes WSDL, XML schema and policy documents, and generates C headers and source files.</span></span> <span data-ttu-id="30eb8-110">Cet outil est similaire à l’outil compilateur WSDL pour le code managé, mais il est destiné au code natif à la place.</span><span class="sxs-lookup"><span data-stu-id="30eb8-110">This tool is similar to WSDL compiler tool for managed code but is aimed at native code instead.</span></span>

<span data-ttu-id="30eb8-111">Pour prendre en charge le [modèle de service](service-model-layer-overview.md), WsUtil.exe génère des en-têtes à utiliser à la fois pour le client et le service.</span><span class="sxs-lookup"><span data-stu-id="30eb8-111">To support the [service model](service-model-layer-overview.md), WsUtil.exe generates headers to be used for both client and service.</span></span> <span data-ttu-id="30eb8-112">Il génère un fichier proxy C pour le côté client et des fichiers stub C pour le côté service, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="30eb8-112">It generates C proxy file for the client side, and C stub files for the service side, as needed.</span></span>

<span data-ttu-id="30eb8-113">Pour prendre en charge la [sérialisation](serialization.md), le compilateur génère des en-têtes pour les descriptions d’éléments pour les définitions d’éléments globaux et toutes les informations de définition de type dans les fichiers de proxy qui sont consommés par le moteur de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="30eb8-113">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all the type definition information in the proxy files that is consumed by the serialization engine.</span></span>


<span data-ttu-id="30eb8-114">Pour obtenir des options de ligne de commande pour le traitement des fichiers WSDL, des fichiers de schéma XML et des fichiers de stratégie de service Web, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="30eb8-114">For command line options for processing WSDL files, XML Schema files, and web service policy files, see the following topics:</span></span>

-   [<span data-ttu-id="30eb8-115">Outil du compilateur de service Web</span><span class="sxs-lookup"><span data-stu-id="30eb8-115">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
-   [<span data-ttu-id="30eb8-116">WSDL et contrats de service</span><span class="sxs-lookup"><span data-stu-id="30eb8-116">WSDL and Service Contracts</span></span>](wsdl-support.md)
-   [<span data-ttu-id="30eb8-117">Prise en charge des schémas</span><span class="sxs-lookup"><span data-stu-id="30eb8-117">Schema support</span></span>](schema-support.md)
-   [<span data-ttu-id="30eb8-118">Prise en charge des stratégies</span><span class="sxs-lookup"><span data-stu-id="30eb8-118">Policy support</span></span>](policy-support.md)

## <a name="security"></a><span data-ttu-id="30eb8-119">Sécurité</span><span class="sxs-lookup"><span data-stu-id="30eb8-119">Security</span></span>

<span data-ttu-id="30eb8-120">Lorsque vous utilisez WsUtil, tenez compte des points suivants et observez les précautions appropriées :</span><span class="sxs-lookup"><span data-stu-id="30eb8-120">When you use WsUtil, be aware of the following issues and observe the appropriate precautions:</span></span>

-   <span data-ttu-id="30eb8-121">Wsutil ne récupère pas les métadonnées XML sur le réseau et Wsutil ne résout pas les instructions import et/ou include dans les fichiers de métadonnées d’entrée.</span><span class="sxs-lookup"><span data-stu-id="30eb8-121">Wsutil does not retrieve XML metadata over the network, and wsutil does not resolve import and/or include statements in the input metadata files.</span></span> <span data-ttu-id="30eb8-122">Wsutil ouvre et lit les fichiers WSDL, XSD et de stratégie.</span><span class="sxs-lookup"><span data-stu-id="30eb8-122">Wsutil opens and reads wsdl, xsd, and policy files.</span></span> <span data-ttu-id="30eb8-123">Les métadonnées XML ne sont pas résistantes aux falsifications.</span><span class="sxs-lookup"><span data-stu-id="30eb8-123">XML metadata is not tamper resistant.</span></span> <span data-ttu-id="30eb8-124">Veillez à utiliser uniquement WSDL, XSD et les fichiers de stratégie sont acquis à partir de la source approuvée et veillez à protéger les fichiers contre toute falsification avant et après les avoir utilisés.</span><span class="sxs-lookup"><span data-stu-id="30eb8-124">Ensure that you only use wsdl, xsd and policy files are acquired from trusted source and make sure to protect the files from tampering before and after using them.</span></span> <span data-ttu-id="30eb8-125">Examinez attentivement le contenu des fichiers d’entrée et vérifiez que le contenu des fichiers est sécurisé pour une utilisation dans l’application.</span><span class="sxs-lookup"><span data-stu-id="30eb8-125">Carefully review the contents of the input files and validate that the contents of files are safe for use in the application.</span></span> <span data-ttu-id="30eb8-126">Wsutil.exe n’effectue aucune vérification de l’authenticité des fichiers de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="30eb8-126">Wsutil.exe does not do any verification of authenticity of the metadata files.</span></span>
-   <span data-ttu-id="30eb8-127">Wsutil génère des fichiers d’en-tête et stub, qui ne sont pas résistants aux falsifications.</span><span class="sxs-lookup"><span data-stu-id="30eb8-127">Wsutil generates header and stub files, which are not tamper resistant.</span></span> <span data-ttu-id="30eb8-128">Vous devez définir les droits d’accès au niveau corrects sur les fichiers sources générés par wsutil.exe pour empêcher l’accès unauthoritized à ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="30eb8-128">You need to set the correct level access rights on source files generated by wsutil.exe to prevent unauthoritized access to those files.</span></span> <span data-ttu-id="30eb8-129">Wsutil utilise System. IO. StreamWriter pour créer les fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="30eb8-129">Wsutil uses System.IO.StreamWriter to create the output files.</span></span>
-   <span data-ttu-id="30eb8-130">Les utilisateurs doivent savoir que Wsutil peut remplacer leurs fichiers locaux et qu’ils doivent veiller à spécifier des noms de fichiers sûrs et des répertoires pour les fichiers de sortie à l’aide du commutateur/out.</span><span class="sxs-lookup"><span data-stu-id="30eb8-130">Users need to be aware that Wsutil can overwrite their local files, and they should be careful to specify safe file names and directories for output files using the /out switch.</span></span>
-   <span data-ttu-id="30eb8-131">Wsutil ou wsutilhelper.dll chargées dans wsutil.exe peut s’arrêter de manière inattendue ou consommer une grande quantité de ressources système lors d’une attaque ou lors du traitement d’une très grande quantité de métadonnées d’entrée.</span><span class="sxs-lookup"><span data-stu-id="30eb8-131">Wsutil or wsutilhelper.dll loaded in wsutil.exe, may terminate unexpectedly or consume large amount of system resources when under attack or in processing a very large amount of input metadata.</span></span> <span data-ttu-id="30eb8-132">L’outil est conçu pour être utilisé au moment du développement uniquement. cet outil ne doit être utilisé qu’en tant qu’outil de développement.</span><span class="sxs-lookup"><span data-stu-id="30eb8-132">The tool is designed to be used during development time only This tool should be used as a development time tool only.</span></span> <span data-ttu-id="30eb8-133">Il se peut qu’il ne soit pas possible de l’utiliser dans la couche intermédiaire pour traiter les informations de stratégie.</span><span class="sxs-lookup"><span data-stu-id="30eb8-133">It may not be safe for use in the middle tier to process policy information.</span></span>
-   <span data-ttu-id="30eb8-134">Wsutilhelper.dll DLL d’assistance est chargée dans les wsutil.exe managées pour traiter les informations de stratégie.</span><span class="sxs-lookup"><span data-stu-id="30eb8-134">Wsutilhelper.dll helper DLL is loaded into managed wsutil.exe to process policy information.</span></span> <span data-ttu-id="30eb8-135">L’utilisateur doit s’assurer qu’aucun fichier binaire malveillant portant le même nom de fichier n’existe dans le chemin d’accès binaire.</span><span class="sxs-lookup"><span data-stu-id="30eb8-135">User should make sure no malicious binary with same filename exists in the binary path.</span></span> <span data-ttu-id="30eb8-136">De même, l’utilisateur doit s’assurer que dans l’environnement de génération, le chemin d’accès binaire est correctement configuré et qu’il n’existe aucun fichier binaire malveillant portant le même nom de « wsutil.exe ».</span><span class="sxs-lookup"><span data-stu-id="30eb8-136">Similarly, user should make sure in the build environment, the binary path is setup correctly that there is no malicious binary with same "wsutil.exe" name exists.</span></span>
-   <span data-ttu-id="30eb8-137">Wsutil génère une annotation SAL pour les opérations et les champs de structure lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="30eb8-137">Wsutil generates SAL annotation for operations and structure fields when possible.</span></span> <span data-ttu-id="30eb8-138">L’utilisateur des fichiers générés par Wsutil doit respecter les exigences spécifiées par le biais de l’annotation SAL.</span><span class="sxs-lookup"><span data-stu-id="30eb8-138">User of wsutil generated files should follow the requirement specified through SAL annotation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30eb8-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30eb8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30eb8-140">Vue d’ensemble de la couche de modèle de service</span><span class="sxs-lookup"><span data-stu-id="30eb8-140">Service Model Layer Overview</span></span>](service-model-layer-overview.md)
</dt> <dt>

[<span data-ttu-id="30eb8-141">Sérialisation</span><span class="sxs-lookup"><span data-stu-id="30eb8-141">Serialization</span></span>](serialization.md)
</dt> <dt>

[<span data-ttu-id="30eb8-142">Outil du compilateur de service Web</span><span class="sxs-lookup"><span data-stu-id="30eb8-142">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
</dt> <dt>

[<span data-ttu-id="30eb8-143">Prise en charge WSDL</span><span class="sxs-lookup"><span data-stu-id="30eb8-143">WSDL support</span></span>](wsdl-support.md)
</dt> <dt>

[<span data-ttu-id="30eb8-144">Prise en charge des schémas</span><span class="sxs-lookup"><span data-stu-id="30eb8-144">Schema support</span></span>](schema-support.md)
</dt> <dt>

[<span data-ttu-id="30eb8-145">Prise en charge des stratégies</span><span class="sxs-lookup"><span data-stu-id="30eb8-145">Policy Support</span></span>](policy-support.md)
</dt> </dl>

 

 





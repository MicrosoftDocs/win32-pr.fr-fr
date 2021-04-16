---
title: Outil du compilateur de service Web
description: Pour prendre en charge le modèle de service, wsutil.exe génère un en-tête à utiliser à la fois côté client et côté service. Il génère un fichier proxy C pour le côté client et un fichier stub C pour le côté service, si nécessaire.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Services Web de l’outil de compilateur de service Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383336"
---
# <a name="web-service-compiler-tool"></a><span data-ttu-id="9e707-107">Outil du compilateur de service Web</span><span class="sxs-lookup"><span data-stu-id="9e707-107">Web Service Compiler Tool</span></span>

<span data-ttu-id="9e707-108">Pour prendre en charge le modèle de service, wsutil.exe génère un en-tête à utiliser à la fois côté client et côté service.</span><span class="sxs-lookup"><span data-stu-id="9e707-108">To support service model, wsutil.exe generates header to be used in both client and service side.</span></span> <span data-ttu-id="9e707-109">Il génère un fichier proxy C pour le côté client et un fichier stub C pour le côté service, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9e707-109">It generates C proxy file for client side, and C stub file for service side, as needed.</span></span>


<span data-ttu-id="9e707-110">Pour prendre en charge la [sérialisation](serialization.md), le compilateur génère des en-têtes pour les descriptions d’éléments pour les définitions d’éléments globaux et toutes les informations de définition de type dans le fichier proxy à consommer par le moteur de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="9e707-110">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all type definition information in proxy file to be consumed by the serialization engine.</span></span>

<span data-ttu-id="9e707-111">Utilisation</span><span class="sxs-lookup"><span data-stu-id="9e707-111">Usage</span></span>

<span data-ttu-id="9e707-112">**Commutateur de commutateurs de \[ ligne de commandeWsUtil.exe \[ -options \] :\]<filename>**</span><span class="sxs-lookup"><span data-stu-id="9e707-112">**WsUtil.exe \[command-line-switches \[switch-options\]:\]<filename>**</span></span>

<span data-ttu-id="9e707-113">commutateurs de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="9e707-113">command-line-switches</span></span>

<span data-ttu-id="9e707-114">Spécifie WsUtil.exe options du compilateur.</span><span class="sxs-lookup"><span data-stu-id="9e707-114">Specifies WsUtil.exe compiler options.</span></span> <span data-ttu-id="9e707-115">Les commutateurs peuvent apparaître dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="9e707-115">Switches can appear in any order.</span></span> <span data-ttu-id="9e707-116">Les tirets (« - ») et les barres obliques (« / ») sont traités comme les mêmes.</span><span class="sxs-lookup"><span data-stu-id="9e707-116">Dash ('-') and slash ('/') are treated as the same.</span></span>

<span data-ttu-id="9e707-117">Liste des options de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="9e707-117">List of command line options</span></span>

-   <span data-ttu-id="9e707-118">@filename Spécifie que le fichier d’entrée doit être traité comme un fichier réponse.</span><span class="sxs-lookup"><span data-stu-id="9e707-118">@filename Specifies that the input file should be treated as a response file.</span></span> <span data-ttu-id="9e707-119">Cette option peut être utilisée plusieurs fois, à n’importe quel endroit de la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="9e707-119">This option can be used multiple times, in any places in the argument list.</span></span>
-   <span data-ttu-id="9e707-120">/wsdl : <filename> : <\_ url facultative> spécifie que le fichier d’entrée doit être traité en tant que fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="9e707-120">/wsdl:<filename>:<optional\_url> Specifies that the input file should be treated as a wsdl file.</span></span> <span data-ttu-id="9e707-121">Plusieurs entrées WSDL sont autorisées et tous les fichiers WSDL spécifiés sont traités.</span><span class="sxs-lookup"><span data-stu-id="9e707-121">Multiple wsdl inputs are allowed and all specified wsdl files are processed.</span></span> <span data-ttu-id="9e707-122">L' \_ URL facultative spécifie l’emplacement à partir duquel les métadonnées ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="9e707-122">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="9e707-123">Si aucune \_ URL facultative n’est spécifiée, Wsutil génère une URL unique en interne.</span><span class="sxs-lookup"><span data-stu-id="9e707-123">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="9e707-124">Voir aussi [prise en charge des stratégies](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="9e707-124">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="9e707-125">/xsd : <filename> spécifie que le nom de fichier d’entrée doit être traité comme un fichier de schéma.</span><span class="sxs-lookup"><span data-stu-id="9e707-125">/xsd:<filename> Specifies that the input filename should be treated as a schema file.</span></span> <span data-ttu-id="9e707-126">Plusieurs entrées XSD sont autorisées et tous les fichiers de schéma spécifiés sont traités.</span><span class="sxs-lookup"><span data-stu-id="9e707-126">Multiple xsd inputs are allowed and all specified schema files are processed.</span></span>
-   <span data-ttu-id="9e707-127">/wsp : <filename> : <\_ url facultative> spécifie que le nom de fichier d’entrée doit être traité en tant que métadonnées de stratégie.</span><span class="sxs-lookup"><span data-stu-id="9e707-127">/wsp:<filename>:<optional\_url> Specifies that the input filename should be treated as policy metadata.</span></span> <span data-ttu-id="9e707-128">Plusieurs entrées wsp sont autorisées et tous les fichiers de stratégie spécifiés sont traités.</span><span class="sxs-lookup"><span data-stu-id="9e707-128">Multiple wsp inputs are allowed and all specified policy files are processed.</span></span> <span data-ttu-id="9e707-129">L' \_ URL facultative spécifie l’emplacement à partir duquel les métadonnées ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="9e707-129">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="9e707-130">Si aucune \_ URL facultative n’est spécifiée, Wsutil génère une URL unique en interne.</span><span class="sxs-lookup"><span data-stu-id="9e707-130">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="9e707-131">Les fichiers de stratégie sont ignorés si l’indicateur/nopolicy est spécifié.</span><span class="sxs-lookup"><span data-stu-id="9e707-131">Policy files are ignored if /nopolicy flag is specified.</span></span> <span data-ttu-id="9e707-132">Voir aussi [prise en charge des stratégies](policy-support.md).</span><span class="sxs-lookup"><span data-stu-id="9e707-132">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="9e707-133">/nopolicy désactive le traitement de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9e707-133">/nopolicy Disable policy processing.</span></span>
-   <span data-ttu-id="9e707-134">/out : <dirname> spécifie le nom du répertoire pour les fichiers de sortie</span><span class="sxs-lookup"><span data-stu-id="9e707-134">/out:<dirname> Specifies directory name for output files</span></span>
-   <span data-ttu-id="9e707-135">/NoClient ne pas générer le stub côté client.</span><span class="sxs-lookup"><span data-stu-id="9e707-135">/noclient Do not generate the client side stub.</span></span>
-   <span data-ttu-id="9e707-136">/noservice ne pas générer le stub côté service.</span><span class="sxs-lookup"><span data-stu-id="9e707-136">/noservice Do not generate the service side stub.</span></span>
-   <span data-ttu-id="9e707-137">/Prefix : <string> ajoute la chaîne spécifiée à tous les identificateurs générés.</span><span class="sxs-lookup"><span data-stu-id="9e707-137">/prefix:<string> Prepend specified string to all generated identifiers.</span></span>
-   <span data-ttu-id="9e707-138">/FullName ajoute un nom de fichier normalisé aux identificateurs générés.</span><span class="sxs-lookup"><span data-stu-id="9e707-138">/fullname Prepend normalized filename to generated identifiers.</span></span> <span data-ttu-id="9e707-139">Par défaut, seul le nom spécifié dans l’attribut « Name » est utilisé pour générer des identificateurs pour les descriptions associées.</span><span class="sxs-lookup"><span data-stu-id="9e707-139">By default only name specified in "name" attribute will be used to generate identifiers for related descriptions.</span></span>
-   <span data-ttu-id="9e707-140">/String : <WS \_ string>\|<WCHAR \*> par défaut, Wsutil génère WCHAR \* pour le type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="9e707-140">/string:<WS\_STRING>\|<WCHAR\*> By default, wsutil generates WCHAR\* for xsd:string type.</span></span> <span data-ttu-id="9e707-141">L’application peut utiliser cet indicateur pour remplacer ce comportement et génère à la \_ place WS String pour xsd : type.</span><span class="sxs-lookup"><span data-stu-id="9e707-141">Application can use this flag to overwrite that behavior, and generates WS\_STRING for xsd:type instead.</span></span>
-   <span data-ttu-id="9e707-142">/help afficher le message d’aide</span><span class="sxs-lookup"><span data-stu-id="9e707-142">/help Display help message</span></span>
-   <span data-ttu-id="9e707-143">/?</span><span class="sxs-lookup"><span data-stu-id="9e707-143">/?</span></span> <span data-ttu-id="9e707-144">Identique à/help</span><span class="sxs-lookup"><span data-stu-id="9e707-144">Same as /help</span></span>
-   <span data-ttu-id="9e707-145">/W : x options de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="9e707-145">/W:x Error handling options.</span></span> <span data-ttu-id="9e707-146">Peut être W :0-W : 4 \| WX</span><span class="sxs-lookup"><span data-stu-id="9e707-146">Could be W:0-W:4 \| WX</span></span>
-   <span data-ttu-id="9e707-147">/nologo ne pas générer d’informations spécifiques au compilateur sur la sortie de la console.</span><span class="sxs-lookup"><span data-stu-id="9e707-147">/nologo Do not generate compiler specific information on console output.</span></span>
-   <span data-ttu-id="9e707-148">les/nostamp ne génèrent pas d’informations spécifiques au compilateur sur les fichiers générés.</span><span class="sxs-lookup"><span data-stu-id="9e707-148">/nostamp Do not generate compiler specific information on generated files.</span></span>

<span data-ttu-id="9e707-149">Par défaut, le compilateur génère les fichiers suivants pour le fichier WSDL, ou WSDL retourné à partir de l’échange de métadonnées :</span><span class="sxs-lookup"><span data-stu-id="9e707-149">By default, the compiler generates the following files for WSDL file, or WSDL returned from metadata exchange:</span></span>

-   <span data-ttu-id="9e707-150">Proxy client ({InputFileName}. c)</span><span class="sxs-lookup"><span data-stu-id="9e707-150">Client proxy ({inputfilename}.c)</span></span>
-   <span data-ttu-id="9e707-151">Service stub ({InputFileName}. c)</span><span class="sxs-lookup"><span data-stu-id="9e707-151">Service Stub ({inputfilename}.c)</span></span>
-   <span data-ttu-id="9e707-152">Fichier d’en-tête ({InputFileName}. h)</span><span class="sxs-lookup"><span data-stu-id="9e707-152">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="9e707-153">La racine du nom de fichier généré est le nom du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9e707-153">The root of the generated filename is the input file name.</span></span> <span data-ttu-id="9e707-154">Les extensions de fichier d’entrée d’origine sont conservées pour empêcher la collision de nom de fichier pour les fichiers générés.</span><span class="sxs-lookup"><span data-stu-id="9e707-154">Original input file extensions are preserved to prevent file name collision for generated files.</span></span> <span data-ttu-id="9e707-155">Par défaut, les stubs de client et de service sont générés dans le même fichier, avec le code stub de service généré après le code proxy.</span><span class="sxs-lookup"><span data-stu-id="9e707-155">By default client and service stubs are generated in the same file, with service stub code generated after the proxy code.</span></span>

    <span data-ttu-id="9e707-156">Par défaut, le compilateur génère les fichiers suivants pour un fichier XSD pour le schéma retourné par l’échange de métadonnées :</span><span class="sxs-lookup"><span data-stu-id="9e707-156">By default, the compiler generates the following files for a XSD file for schema returned from metadata exchange:</span></span>

-   <span data-ttu-id="9e707-157">descriptions de sérialisation ({InputFileName}. c)</span><span class="sxs-lookup"><span data-stu-id="9e707-157">serialization descriptions ({inputfilename}.c)</span></span>
-   <span data-ttu-id="9e707-158">Fichier d’en-tête ({InputFileName}. h)</span><span class="sxs-lookup"><span data-stu-id="9e707-158">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="9e707-159">La racine du nom de fichier est le nom du service.</span><span class="sxs-lookup"><span data-stu-id="9e707-159">The root of the filename is the service name.</span></span>

<span data-ttu-id="9e707-160">Wsutil.exe génère une section « tampon » au début de tous les fichiers générés, indiquant l’option de compilateur, la version de l’outil, l’option de ligne de commande applicable, etc. Cette section peut être désactivée à l’aide de l’option/nostamp pour éviter le bruit lors de la comparaison des fichiers générés.</span><span class="sxs-lookup"><span data-stu-id="9e707-160">Wsutil.exe generates a "stamp" section at the beginning of all the generated files, indicating the compiler option, tool version, command line option applicable, etc. This section can be turned off by using /nostamp option to avoid noise with comparing generated files.</span></span>

<span data-ttu-id="9e707-161">Wsutil ne prend pas en charge le téléchargement de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9e707-161">Wsutil does not support downloading metadata</span></span>

<span data-ttu-id="9e707-162">Le compilateur Wsutil fonctionne uniquement à partir du fichier de métadonnées local.</span><span class="sxs-lookup"><span data-stu-id="9e707-162">Wsutil compiler works from local metadata file only.</span></span> <span data-ttu-id="9e707-163">L’outil ne prend pas en charge le téléchargement de métadonnées à partir de services Web en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9e707-163">The tool does not support downloading metadata from running web services.</span></span> <span data-ttu-id="9e707-164">Les développeurs peuvent utiliser d’autres outils de service Web pris en charge, tels que Svcutil, pour télécharger des métadonnées sur l’ordinateur local, inspecter les fichiers enregistrés et transmettre ces fichiers à wsutil.exe pour la compilation.</span><span class="sxs-lookup"><span data-stu-id="9e707-164">Developers can use other supported webservice tools, like svcutil, to download metadata to local machine, inspect the saved files, and pass those files to wsutil.exe for compilation.</span></span>

<span data-ttu-id="9e707-165">Prise en charge de plusieurs fichiers d’entrée/sortie</span><span class="sxs-lookup"><span data-stu-id="9e707-165">Multiple input/output file support</span></span>

<span data-ttu-id="9e707-166">Le schéma WSDL et XML permet d’inclure ou d’importer des définitions d’autres espaces de noms spécifiés dans d’autres emplacements/fichiers.</span><span class="sxs-lookup"><span data-stu-id="9e707-166">WSDL and XML schema allows including/importing definitions from other name spaces specified in other location/files.</span></span> <span data-ttu-id="9e707-167">Wsutil prend en charge plusieurs entrées de schéma/WSDL/de stratégie et génère un jeu d’en-tête/stub pour chaque fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9e707-167">Wsutil supports multiple schema/wsdl/policy input, and generate one set of stub/header for each input files.</span></span> <span data-ttu-id="9e707-168">Wsutil ne suit pas les instructions include et import.</span><span class="sxs-lookup"><span data-stu-id="9e707-168">Wsutil does not follow through the include and import statements.</span></span> <span data-ttu-id="9e707-169">Au lieu de cela, l’application doit transmettre des fichiers contenant tous les espaces de noms nécessaires à Wsutil afin que l’outil puisse résoudre toutes les dépendances lors de la compilation.</span><span class="sxs-lookup"><span data-stu-id="9e707-169">Instead, application should pass in files containing all necessary namespaces to wsutil such that the tool can resolve all dependencies during compilation.</span></span>

<span data-ttu-id="9e707-170">**WsUtil.exe/xsd : StockQuote. xsd/wsdl : StockQuote. wsdl/wsdl : StockQuoteService. wsdl**</span><span class="sxs-lookup"><span data-stu-id="9e707-170">**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**</span></span>

<span data-ttu-id="9e707-171">Wsutil génère trois ensembles de fichiers de sortie :</span><span class="sxs-lookup"><span data-stu-id="9e707-171">wsutil generates three sets of output files:</span></span>

-   <span data-ttu-id="9e707-172">StockQuote. xsd. c StockQuote. xsd. h</span><span class="sxs-lookup"><span data-stu-id="9e707-172">stockquote.xsd.c stockquote.xsd.h</span></span>
-   <span data-ttu-id="9e707-173">StockQuote. wsdl. c StockQuote. wsdl. h</span><span class="sxs-lookup"><span data-stu-id="9e707-173">stockquote.wsdl.c stockquote.wsdl.h</span></span>
-   <span data-ttu-id="9e707-174">StockQuoteService. wsdl. h stockquoteservices. wsdl. c</span><span class="sxs-lookup"><span data-stu-id="9e707-174">stockquoteservice.wsdl.h stockquoteservices.wsdl.c</span></span>

<span data-ttu-id="9e707-175">Format des fichiers de sortie</span><span class="sxs-lookup"><span data-stu-id="9e707-175">Output file format</span></span>

<span data-ttu-id="9e707-176">Pour chaque fichier de sortie, Wsutil génère des définitions disponibles en externe dans le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="9e707-176">For each output file, wsutil generates externally available definitions in the header file.</span></span> <span data-ttu-id="9e707-177">Outre les définitions de structure C et les prototypes de fonction stub, toutes les autres définitions associées aux services Web sont encapsulées dans une structure globale nommée avec un nom de fichier normalisé.</span><span class="sxs-lookup"><span data-stu-id="9e707-177">Other than C structure definitions and stub function prototypes, all the other web services related definitions are encapsulated in a global structure named with normalized filename.</span></span>

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="9e707-178">Notez que tous les champs ne sont pas générés pour la structure globale.</span><span class="sxs-lookup"><span data-stu-id="9e707-178">Notice that not all the fields are generated for the global structure.</span></span> <span data-ttu-id="9e707-179">Un champ de niveau supérieur est généré uniquement lorsque les définitions associées sont spécifiées dans le fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9e707-179">A top level field is generated only when the related definitions are specified in the input file.</span></span> <span data-ttu-id="9e707-180">Par exemple, aucun champ de message, d’opération et de contrat n’est généré pour les fichiers XSD.</span><span class="sxs-lookup"><span data-stu-id="9e707-180">For example, no message, operations, and contracts fields are generated for xsd files.</span></span>

<span data-ttu-id="9e707-181">Niveaux d’avertissement et niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="9e707-181">Warning Levels and error level</span></span>

<span data-ttu-id="9e707-182">Comme pour le compilateur C, WsUtil.exe prend en charge quatre niveaux d’avertissement et un niveau d’erreur :</span><span class="sxs-lookup"><span data-stu-id="9e707-182">Similar to C compiler, WsUtil.exe supports four warning levels and one error level:</span></span>

-   <span data-ttu-id="9e707-183">WsUtil.exe génère des erreurs avec des échecs irrécupérables, comme un fichier WSDL non valide, des options de compilateur non valides, etc.</span><span class="sxs-lookup"><span data-stu-id="9e707-183">WsUtil.exe generates errors with unrecoverable failures, like invalid wsdl file, invalid compiler options etc.</span></span>
-   <span data-ttu-id="9e707-184">WsUtil génère des avertissements W1 avec des problèmes récupérables graves.</span><span class="sxs-lookup"><span data-stu-id="9e707-184">WsUtil generates W1 warnings with serious recoverable issues.</span></span> <span data-ttu-id="9e707-185">Le compilateur peut passer à, mais l’utilisateur doit être conscient du problème.</span><span class="sxs-lookup"><span data-stu-id="9e707-185">The compiler can go on but user should be aware of the issue.</span></span> <span data-ttu-id="9e707-186">Par exemple, un avertissement W1 est généré s’il existe des attributs non pris en charge, tels que des facettes WSDL, en WSDL qui n’affectent pas la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9e707-186">For example, a W1 warning will be generated if there are unsupported attributes, like some WSDL facets, in wsdl that does not affect code generation.</span></span>
-   <span data-ttu-id="9e707-187">WsUtil génère des avertissements W2 avec des problèmes moins graves.</span><span class="sxs-lookup"><span data-stu-id="9e707-187">WsUtil generates W2 warnings with less serious problems.</span></span> <span data-ttu-id="9e707-188">Il n’y a aucune perte de fonctionnalité, mais le développeur d’applications peut souhaiter le savoir.</span><span class="sxs-lookup"><span data-stu-id="9e707-188">There is no lost of functionality, but application developer might want to know that.</span></span> <span data-ttu-id="9e707-189">Comme les comportements qui peuvent être différents des autres plateformes.</span><span class="sxs-lookup"><span data-stu-id="9e707-189">Like behaviors that might be different from other platforms.</span></span>
-   <span data-ttu-id="9e707-190">WsUtil génère des avertissements W3 avec un impact minimal sur le code généré.</span><span class="sxs-lookup"><span data-stu-id="9e707-190">WsUtil generates W3 warnings with minimal impact on generated code.</span></span> <span data-ttu-id="9e707-191">Par exemple, wsutil.exe génère un avertissement W3 quand une chaîne normalisée est différente de la chaîne d’origine.</span><span class="sxs-lookup"><span data-stu-id="9e707-191">For example, wsutil.exe generates a W3 warning when normalized string is different from original string.</span></span>
-   <span data-ttu-id="9e707-192">L’avertissement W4 ressemble davantage à des avertissements « informatifs » et WsUtil à un problème de type W4 dans des cas comme l’ignorance de l’attribut de documentation dans WSDL.</span><span class="sxs-lookup"><span data-stu-id="9e707-192">W4 warning is more like "informational" warnings, and WsUtil issue W4 in cases like ignoring documentation attribute in WSDL.</span></span>
-   <span data-ttu-id="9e707-193">WX indique que le compilateur traite l’avertissement comme une erreur.</span><span class="sxs-lookup"><span data-stu-id="9e707-193">WX indicates the compiler treats warning as error.</span></span> <span data-ttu-id="9e707-194">Par exemple, Wsutil génère une erreur pour tous les avertissements W1 si/W : 1/WX est spécifié.</span><span class="sxs-lookup"><span data-stu-id="9e707-194">For example, wsutil generates error for all W1 warnings if /W:1 /WX is specified.</span></span>

<span data-ttu-id="9e707-195">/W : {N} spécifiez le niveau de message d’avertissement qui doit être généré.</span><span class="sxs-lookup"><span data-stu-id="9e707-195">/W:{N} specify which level of warning message should be generated.</span></span> <span data-ttu-id="9e707-196">/W : 1 signifie que les avertissements de niveau 1 doivent être générés et que les avertissements de niveau 2 et inférieur doivent être masqués et non générés par l’outil.</span><span class="sxs-lookup"><span data-stu-id="9e707-196">/W:1 means warning level 1 warnings should be generated, and warnings of warning level 2 and below should be masked and not generated by the tool.</span></span>

## <a name="fullname"></a><span data-ttu-id="9e707-197">/fullname</span><span class="sxs-lookup"><span data-stu-id="9e707-197">/fullname</span></span>

<span data-ttu-id="9e707-198">Cette option indique que WsUtil.exe génère un nom complet pour les identificateurs afin d’éviter une éventuelle collision de noms.</span><span class="sxs-lookup"><span data-stu-id="9e707-198">This option indicates that WsUtil.exe generates full name for identifiers to avoid potential name collision.</span></span> <span data-ttu-id="9e707-199">Par exemple, dans l’exemple. xsd, nous avons :</span><span class="sxs-lookup"><span data-stu-id="9e707-199">For example, in example.xsd we have:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="9e707-200">Par défaut WsUtil.exe génère :</span><span class="sxs-lookup"><span data-stu-id="9e707-200">By default WsUtil.exe generates:</span></span>

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

<span data-ttu-id="9e707-201">Toutefois, si l’option de ligne de commande/FullName est spécifiée, WsUtil.exe génère la définition de structure suivante à la place :</span><span class="sxs-lookup"><span data-stu-id="9e707-201">But if /fullname command line option is specified, WsUtil.exe generates the following structure definition instead:</span></span>

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a><span data-ttu-id="9e707-202">Globalisation</span><span class="sxs-lookup"><span data-stu-id="9e707-202">Globalization</span></span>

<span data-ttu-id="9e707-203">L’outil est indépendant de la langue et peut être localisé dans différentes langues.</span><span class="sxs-lookup"><span data-stu-id="9e707-203">The tool is language neutral and can be localized to different languages.</span></span> <span data-ttu-id="9e707-204">Tous les messages d’erreur/la sortie de la console peuvent être localisés.</span><span class="sxs-lookup"><span data-stu-id="9e707-204">All error messages / console output can be localized.</span></span> <span data-ttu-id="9e707-205">Toutefois, les options de ligne de commande restent en anglais.</span><span class="sxs-lookup"><span data-stu-id="9e707-205">However, the command line options remain in English.</span></span>

## <a name="environment-variable"></a><span data-ttu-id="9e707-206">Variable d’environnement</span><span class="sxs-lookup"><span data-stu-id="9e707-206">Environment Variable</span></span>

<span data-ttu-id="9e707-207">WsUtil.exe n’utilise pas de variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="9e707-207">WsUtil.exe does not use any environment variables.</span></span>

## <a name="platform-independent"></a><span data-ttu-id="9e707-208">Indépendant de la plateforme</span><span class="sxs-lookup"><span data-stu-id="9e707-208">Platform independent</span></span>

<span data-ttu-id="9e707-209">Les fichiers de sortie de WsUtil.exe sont indépendants de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="9e707-209">Output files from WsUtil.exe are platform independent.</span></span> <span data-ttu-id="9e707-210">Aucun code dépendant de l’architecture n’est généré dans le stub ; tout ce qui est spécifique à l’architecture est pris en charge par le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="9e707-210">There is no architecture dependent code generated in the stub; anything architecture specific will be taken care of by the C compiler.</span></span> <span data-ttu-id="9e707-211">Le stub peut être utilisé dans toutes les plateformes que nous prenons en charge.</span><span class="sxs-lookup"><span data-stu-id="9e707-211">The stub can be used in all the platforms we support.</span></span>

<span data-ttu-id="9e707-212">Pour obtenir une description de wsutil.exe, consultez la section prise en charge de [WSDL](wsdl-support.md) et du [support de schéma](schema-support.md) .</span><span class="sxs-lookup"><span data-stu-id="9e707-212">Description for wsutil.exe output can be found at [WSDL support](wsdl-support.md) and [Schema support](schema-support.md) part.</span></span>

 

 





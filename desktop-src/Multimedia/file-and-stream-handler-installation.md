---
title: Installation du gestionnaire de fichiers et de flux
description: Installation du gestionnaire de fichiers et de flux
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675265"
---
# <a name="file-and-stream-handler-installation"></a><span data-ttu-id="af762-103">Installation du gestionnaire de fichiers et de flux</span><span class="sxs-lookup"><span data-stu-id="af762-103">File and Stream Handler Installation</span></span>

<span data-ttu-id="af762-104">La bibliothèque AVIFile utilise des gestionnaires de fichiers et de flux installés pour la lecture et l’écriture de fichiers AVI et de flux.</span><span class="sxs-lookup"><span data-stu-id="af762-104">The AVIFile library uses installed stream and file handlers for reading and writing AVI files and streams.</span></span> <span data-ttu-id="af762-105">Un gestionnaire est installé lorsqu’il se trouve dans le répertoire système de Windows et le registre contient les informations suivantes requises pour décrire et identifier un gestionnaire :</span><span class="sxs-lookup"><span data-stu-id="af762-105">A handler is installed when it resides in the Windows SYSTEM directory and the registry contains the following information needed to describe and identify a handler:</span></span>

-   <span data-ttu-id="af762-106">Identificateur de classe de 16 octets pour le gestionnaire</span><span class="sxs-lookup"><span data-stu-id="af762-106">The 16-byte class identifier for the handler</span></span>
-   <span data-ttu-id="af762-107">Brève description du gestionnaire</span><span class="sxs-lookup"><span data-stu-id="af762-107">A brief description of the handler</span></span>
-   <span data-ttu-id="af762-108">Nom du fichier contenant le gestionnaire</span><span class="sxs-lookup"><span data-stu-id="af762-108">The name of the file containing the handler</span></span>
-   <span data-ttu-id="af762-109">Extension de fichier qu’un gestionnaire de fichiers peut traiter</span><span class="sxs-lookup"><span data-stu-id="af762-109">The file extension that a file handler can process</span></span>
-   <span data-ttu-id="af762-110">Accès aux fichiers et autres propriétés associés à un gestionnaire de fichiers</span><span class="sxs-lookup"><span data-stu-id="af762-110">File-access and other properties associated with a file handler</span></span>
-   <span data-ttu-id="af762-111">Codes à quatre caractères identifiant les types de flux qu’un gestionnaire de flux peut traiter</span><span class="sxs-lookup"><span data-stu-id="af762-111">Four-character codes identifying stream types that a stream handler can process</span></span>

<span data-ttu-id="af762-112">La bibliothèque AVIFile interroge le registre pour les gestionnaires qui sont externes à une application lors de l’ouverture de fichiers et de l’accès aux flux.</span><span class="sxs-lookup"><span data-stu-id="af762-112">The AVIFile library queries the registry for handlers that are external to an application when opening files and accessing streams.</span></span> <span data-ttu-id="af762-113">Le résultat d’une requête réussie retourne le nom de fichier d’un gestionnaire qui peut traiter le fichier ou le type de flux spécifié dans la requête.</span><span class="sxs-lookup"><span data-stu-id="af762-113">The result of a successful query returns the filename of a handler that can process the file or stream type specified in the query.</span></span> <span data-ttu-id="af762-114">Le Registre répertorie chaque gestionnaire en créant trois entrées de la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="af762-114">The registry lists each handler by creating three entries that have the following form:</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



<span data-ttu-id="af762-115">Ces entrées se composent des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="af762-115">These entries consist of the following parts.</span></span>



| <span data-ttu-id="af762-116">Partie</span><span class="sxs-lookup"><span data-stu-id="af762-116">Part</span></span>                                   | <span data-ttu-id="af762-117">Description</span><span class="sxs-lookup"><span data-stu-id="af762-117">Description</span></span>                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af762-118">\_racine des classes HKEY \_</span><span class="sxs-lookup"><span data-stu-id="af762-118">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="af762-119">Identifie l’entrée racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="af762-119">Identifies the root entry of the registry.</span></span>                                                                                                                                               |
| <span data-ttu-id="af762-120">Clsid</span><span class="sxs-lookup"><span data-stu-id="af762-120">Clsid</span></span>                                  | <span data-ttu-id="af762-121">Identifie cette entrée en tant qu’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="af762-121">Identifies this entry as a class identifier.</span></span>                                                                                                                                             |
| <span data-ttu-id="af762-122">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="af762-122">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="af762-123">Spécifie un identificateur d’interface (IID) ou un identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="af762-123">Specifies an interface identifier (IID) or class identifier.</span></span> <span data-ttu-id="af762-124">Cette valeur est un identificateur unique de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="af762-124">This value is a unique 16-byte identifier.</span></span> <span data-ttu-id="af762-125">(L’identificateur peut également être appelé GUID ou UUID dans d’autres manuels.)</span><span class="sxs-lookup"><span data-stu-id="af762-125">(The identifier might also be referred to as a GUID or a UUID in other manuals.)</span></span> |
| <span data-ttu-id="af762-126">Lecteur/enregistreur de fichier Wave</span><span class="sxs-lookup"><span data-stu-id="af762-126">Wave File reader/writer</span></span>                | <span data-ttu-id="af762-127">Spécifie une chaîne pour décrire le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="af762-127">Specifies a string to describe the handler.</span></span> <span data-ttu-id="af762-128">Cette chaîne peut être affichée dans les boîtes de dialogue permettant de sélectionner des gestionnaires de fichiers et de flux.</span><span class="sxs-lookup"><span data-stu-id="af762-128">This string can be displayed in dialog boxes for selecting stream and file handlers.</span></span>                                                         |
| <span data-ttu-id="af762-129">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="af762-129">InProcServer32</span></span>                         | <span data-ttu-id="af762-130">Spécifie le fichier (dans cet exemple, WAVEFILE.DLL) qui peut être chargé pour gérer cette classe.</span><span class="sxs-lookup"><span data-stu-id="af762-130">Specifies the file (in this example, WAVEFILE.DLL) that can be loaded to handle this class.</span></span>                                                                                              |
| <span data-ttu-id="af762-131">AVIFile</span><span class="sxs-lookup"><span data-stu-id="af762-131">AVIFile</span></span>                                | <span data-ttu-id="af762-132">Spécifie les propriétés d’un gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="af762-132">Specifies the properties of a file handler.</span></span> <span data-ttu-id="af762-133">Dans cet exemple, le gestionnaire peut lire et écrire dans un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="af762-133">In this example, the handler can read and write to an AVI file.</span></span>                                                                              |



 

<span data-ttu-id="af762-134">Un gestionnaire de fichiers peut avoir une ou plusieurs de ses propriétés stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="af762-134">A file handler can have one or more of its properties stored in the registry.</span></span> <span data-ttu-id="af762-135">Les constantes suivantes identifient les propriétés actuellement associées à un fichier.</span><span class="sxs-lookup"><span data-stu-id="af762-135">The following constants identify the properties currently associated with a file.</span></span>



| <span data-ttu-id="af762-136">Constante</span><span class="sxs-lookup"><span data-stu-id="af762-136">Constant</span></span>                        | <span data-ttu-id="af762-137">Description</span><span class="sxs-lookup"><span data-stu-id="af762-137">Description</span></span>                                                          |
|---------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="af762-138">AVIFILEHANDLER \_ CANACCEPTNONRGB</span><span class="sxs-lookup"><span data-stu-id="af762-138">AVIFILEHANDLER\_CANACCEPTNONRGB</span></span> | <span data-ttu-id="af762-139">Indique qu’un gestionnaire de fichiers peut traiter des données d’image autres que RVB.</span><span class="sxs-lookup"><span data-stu-id="af762-139">Indicates that a file handler can process image data other than RGB.</span></span> |
| <span data-ttu-id="af762-140">AVIFILEHANDLER \_ CANREAD</span><span class="sxs-lookup"><span data-stu-id="af762-140">AVIFILEHANDLER\_CANREAD</span></span>         | <span data-ttu-id="af762-141">Indique qu’un gestionnaire de fichiers peut ouvrir un fichier avec un accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="af762-141">Indicates that a file handler can open a file with read access.</span></span>      |
| <span data-ttu-id="af762-142">AVIFILEHANDLER \_ CANWRITE</span><span class="sxs-lookup"><span data-stu-id="af762-142">AVIFILEHANDLER\_CANWRITE</span></span>        | <span data-ttu-id="af762-143">Indique qu’un gestionnaire de fichiers peut ouvrir un fichier avec un accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="af762-143">Indicates that a file handler can open a file with write access.</span></span>     |



 

<span data-ttu-id="af762-144">Lorsque vous créez un gestionnaire de fichiers ou de flux, vous pouvez obtenir un nouvel identificateur en exécutant UUIDGEN.EXE.</span><span class="sxs-lookup"><span data-stu-id="af762-144">When creating a file or stream handler, you can obtain a new identifier by running UUIDGEN.EXE.</span></span> <span data-ttu-id="af762-145">Utilisez toujours UUIDGEN.EXE pour créer un nouvel identificateur.</span><span class="sxs-lookup"><span data-stu-id="af762-145">Always use UUIDGEN.EXE to create a new identifier.</span></span> <span data-ttu-id="af762-146">Le nombre hexadécimal de 16 octets créé par cet exécutable identifie de manière unique votre gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="af762-146">The 16-byte hexadecimal number created by this executable will uniquely identify your handler.</span></span>

<span data-ttu-id="af762-147">La bibliothèque AVIFile utilise des entrées supplémentaires dans le registre pour identifier un identificateur de classe en fonction de l’extension de fichier qu’un gestionnaire de fichiers peut traiter ou d’un code à quatre caractères qu’un gestionnaire de fichiers ou de flux peut traiter.</span><span class="sxs-lookup"><span data-stu-id="af762-147">The AVIFile library uses additional entries in the registry to identify a class identifier based on the file extension that a file handler can process or a four-character code that a file or stream handler can process.</span></span> <span data-ttu-id="af762-148">Par exemple, les entrées suivantes associent un identificateur de classe à l’extension de fichier. WAV et le code à quatre caractères « WAVE » :</span><span class="sxs-lookup"><span data-stu-id="af762-148">For example, the following entries associate a class identifier with the file extension .WAV and the four-character code "WAVE":</span></span>


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



<span data-ttu-id="af762-149">Ces entrées se composent des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="af762-149">These entries consist of the following parts.</span></span>



| <span data-ttu-id="af762-150">Partie</span><span class="sxs-lookup"><span data-stu-id="af762-150">Part</span></span>                                   | <span data-ttu-id="af762-151">Description</span><span class="sxs-lookup"><span data-stu-id="af762-151">Description</span></span>                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af762-152">\_racine des classes HKEY \_</span><span class="sxs-lookup"><span data-stu-id="af762-152">HKEY\_CLASSES\_ROOT</span></span>                    | <span data-ttu-id="af762-153">Identifie l’entrée racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="af762-153">Identifies the root entry of the registry.</span></span>                                                        |
| <span data-ttu-id="af762-154">AVIFile</span><span class="sxs-lookup"><span data-stu-id="af762-154">AVIFile</span></span>                                | <span data-ttu-id="af762-155">Identifie cette entrée en tant qu’entrée utilisée par AVIFile.</span><span class="sxs-lookup"><span data-stu-id="af762-155">Identifies this entry as an entry used by AVIFile.</span></span>                                                |
| <span data-ttu-id="af762-156">Extensions</span><span class="sxs-lookup"><span data-stu-id="af762-156">Extensions</span></span>                             | <span data-ttu-id="af762-157">Spécifie l’extension de fichier (dans cet exemple,. WAV) qu’un gestionnaire de fichiers peut traiter.</span><span class="sxs-lookup"><span data-stu-id="af762-157">Specifies the file extension (in this example, .WAV) that a file handler can process.</span></span>             |
| <span data-ttu-id="af762-158">RIFFHandlers</span><span class="sxs-lookup"><span data-stu-id="af762-158">RIFFHandlers</span></span>                           | <span data-ttu-id="af762-159">Spécifie le code à quatre caractères (dans cet exemple, « WAVE ») qu’un gestionnaire de fichiers ou de flux peut traiter.</span><span class="sxs-lookup"><span data-stu-id="af762-159">Specifies the four-character code (in this example, "WAVE") a file or stream handler can process.</span></span> |
| <span data-ttu-id="af762-160">{00010023-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="af762-160">{00010023-0000-0000-C000-000000000046}</span></span> | <span data-ttu-id="af762-161">Spécifie un identificateur d’interface (IID) ou un identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="af762-161">Specifies an interface identifier (IID) or class identifier.</span></span>                                      |



 

<span data-ttu-id="af762-162">Si vous distribuez votre flux ou votre gestionnaire de fichiers sans application d’installation pour l’installer dans le système de l’utilisateur, vous devez inclure un. Fichier REG pour que l’utilisateur puisse installer le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="af762-162">If you distribute your stream or file handler without a setup application to install it in the user's system, you must include a .REG file so the user can install the handler.</span></span> <span data-ttu-id="af762-163">L’utilisateur utilisera l’éditeur du Registre pour créer des entrées de Registre pour votre flux ou votre gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="af762-163">The user will use the registry editor to create registry entries for your stream or file handler.</span></span>

<span data-ttu-id="af762-164">L’exemple suivant montre le contenu d’un type standard. Fichier REG.</span><span class="sxs-lookup"><span data-stu-id="af762-164">The following example shows the contents of a typical .REG file.</span></span> <span data-ttu-id="af762-165">La première entrée de l’exemple suivant est la chaîne descriptive du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="af762-165">The first entry in the following example is the descriptive string for the handler.</span></span> <span data-ttu-id="af762-166">La deuxième entrée identifie le fichier contenant le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="af762-166">The second entry identifies the file containing the handler.</span></span> <span data-ttu-id="af762-167">La troisième entrée identifie les propriétés du gestionnaire de fichiers (dans ce cas, l’accès en lecture seule aux fichiers).</span><span class="sxs-lookup"><span data-stu-id="af762-167">The third entry identifies the properties of the file handler (in this case, read-only access to files).</span></span> <span data-ttu-id="af762-168">La quatrième entrée associe le type de fichier traité par le gestionnaire (dans ce cas, les fichiers avec un. Extension de nom de fichier JPG) avec l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="af762-168">The fourth entry associates the type of file the handler processes (in this case, files with a .JPG filename extension) with the class identifier.</span></span>


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



<span data-ttu-id="af762-169">Lors de la création de ce fichier, enregistrez-le avec un. Extension REG pour l’identifier comme fichier de mise à jour du Registre.</span><span class="sxs-lookup"><span data-stu-id="af762-169">When creating this file, save it with a .REG extension to identify it as an update file for the registry.</span></span> <span data-ttu-id="af762-170">Remplacez également un IID unique pour le code de 16 octets utilisé dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="af762-170">Also, substitute a unique IID for the 16-byte code used in the example.</span></span>

 

 





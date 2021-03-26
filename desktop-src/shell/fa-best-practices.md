---
description: La liste suivante répertorie les meilleures pratiques recommandées pour l’utilisation des associations de fichiers.
title: Meilleures pratiques pour les associations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525797"
---
# <a name="best-practices-for-file-associations"></a><span data-ttu-id="3d8ec-103">Meilleures pratiques pour les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-103">Best Practices for File Associations</span></span>

<span data-ttu-id="3d8ec-104">La liste suivante répertorie les meilleures pratiques recommandées pour l’utilisation des associations de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-104">The following list are recommended best practices you should use when working with file associations.</span></span>

-   [<span data-ttu-id="3d8ec-105">Ne pas copier les associations de fichiers à partir du Registre</span><span class="sxs-lookup"><span data-stu-id="3d8ec-105">Do Not Copy File Associations from the Registry</span></span>](#do-not-copy-file-associations-from-the-registry)
-   [<span data-ttu-id="3d8ec-106">Évitez les chemins d’accès Hard-Coding dans le registre, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-106">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [<span data-ttu-id="3d8ec-107">Toujours encapsuler les chaînes de développement entre guillemets</span><span class="sxs-lookup"><span data-stu-id="3d8ec-107">Always Wrap Expanding Strings in Quotation Marks</span></span>](#always-wrap-expanding-strings-in-quotation-marks)
-   [<span data-ttu-id="3d8ec-108">Ne confondez pas l’exécution automatique/la lecture automatique avec les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-108">Do Not Confuse Autoplay/Autorun with File Associations</span></span>](#do-not-confuse-autoplayautorun-with-file-associations)
-   [<span data-ttu-id="3d8ec-109">Ne confondez pas la base de données MIME d’Internet Explorer avec les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-109">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [<span data-ttu-id="3d8ec-110">Utiliser des ProgID correctement formés et avec version</span><span class="sxs-lookup"><span data-stu-id="3d8ec-110">Use Properly Formed and Versioned ProgIDs</span></span>](#use-properly-formed-and-versioned-progids)
-   [<span data-ttu-id="3d8ec-111">Ne pas utiliser les extensions de nom de fichier courtes</span><span class="sxs-lookup"><span data-stu-id="3d8ec-111">Do Not Use Short File Name Extensions</span></span>](#do-not-use-short-file-name-extensions)
-   [<span data-ttu-id="3d8ec-112">Inscrire de nouveaux types de fichiers dans la base de données MIME IANA</span><span class="sxs-lookup"><span data-stu-id="3d8ec-112">Register New File Types in the IANA MIME Database</span></span>](#register-new-file-types-in-the-iana-mime-database)
-   [<span data-ttu-id="3d8ec-113">S’inscrire auprès du service Web Windows pour les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-113">Sign Up with the Windows Web Service for File Associations</span></span>](#sign-up-with-the-windows-web-service-for-file-associations)
-   [<span data-ttu-id="3d8ec-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d8ec-114">Related topics</span></span>](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a><span data-ttu-id="3d8ec-115">Ne pas copier les associations de fichiers à partir du Registre</span><span class="sxs-lookup"><span data-stu-id="3d8ec-115">Do Not Copy File Associations from the Registry</span></span>

<span data-ttu-id="3d8ec-116">Nous vous recommandons de ne pas copier les associations de fichiers existantes à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-116">We recommended that you do not copy existing file associations from the registry.</span></span> <span data-ttu-id="3d8ec-117">Cela provoque souvent la propagation d’associations de fichiers mal formés.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-117">This often leads to the propagation of poorly formed file associations.</span></span> <span data-ttu-id="3d8ec-118">Au lieu de cela, vous devez suivre les étapes décrites dans [scénario d’exemple d’association de fichiers](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ec-118">Instead, you should follow the steps outlined in [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a><span data-ttu-id="3d8ec-119">Évitez les chemins d’accès Hard-Coding dans le registre, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-119">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>

<span data-ttu-id="3d8ec-120">Tout comme les chemins d’accès codés en dur dans les programmes peuvent entraîner des problèmes, les chemins d’accès codés en dur dans le registre peuvent également entraîner des problèmes.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-120">Just as hard-coding paths into programs can cause problems, hard-coding paths into the registry can also lead to problems.</span></span> <span data-ttu-id="3d8ec-121">Au lieu de cela, vous devez utiliser des chaînes d’expansion du Registre (REG \_ expand \_ SZ) pour fournir l’indépendance du chemin d’accès, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-121">Instead, you should use registry expansion strings (REG\_EXPAND\_SZ) to provide path independence where applicable.</span></span> <span data-ttu-id="3d8ec-122">Par exemple, au lieu d’utiliser cette méthode :</span><span class="sxs-lookup"><span data-stu-id="3d8ec-122">For example, instead of using this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

<span data-ttu-id="3d8ec-123">Vous devez utiliser cette méthode :</span><span class="sxs-lookup"><span data-stu-id="3d8ec-123">You should use this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a><span data-ttu-id="3d8ec-124">Toujours encapsuler les chaînes de développement entre guillemets</span><span class="sxs-lookup"><span data-stu-id="3d8ec-124">Always Wrap Expanding Strings in Quotation Marks</span></span>

<span data-ttu-id="3d8ec-125">Le développement de chaînes peut contenir des espaces quand ils se développent.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-125">Expanding strings can contain spaces when they expand.</span></span> <span data-ttu-id="3d8ec-126">Étant donné que les espaces sont souvent interprétés comme des délimiteurs d’arguments, ils entraînent des problèmes dans certaines circonstances.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-126">Because spaces are often interpreted as argument delimiters, they cause problems under certain circumstances.</span></span> <span data-ttu-id="3d8ec-127">Par exemple, une commande permettant d’appeler MyProgram peut être stockée dans le registre comme suit :</span><span class="sxs-lookup"><span data-stu-id="3d8ec-127">For example, a command to invoke MyProgram can be stored in the registry as:</span></span>

`%SYSTEMROOT%\MyProgram %1 %2`

<span data-ttu-id="3d8ec-128">MyProgram s’attend à ce que %1 soit le chemin d’accès complet à un nom de fichier et %2 un commutateur pour indiquer une action.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-128">MyProgram expects that %1 is the full path to a file name, and %2 is a switch to indicate some action.</span></span> <span data-ttu-id="3d8ec-129">Si cette commande est exécutée avec les arguments **C : \\ Program Files \\ My documents \\document.txt** et **/Print**, et en supposant que la racine du lecteur c : \\ WinNT, elle se développe en :</span><span class="sxs-lookup"><span data-stu-id="3d8ec-129">If this command is executed with arguments **C:\\Program Files\\My Documents\\document.txt** and **/print**, and assuming a SYSTEMROOT of C:\\WINNT, it expands to:</span></span>

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

<span data-ttu-id="3d8ec-130">Dans ce cas, MyProgram interprète que le premier argument est C : \\ Program et le deuxième argument est Files \\ My, qui n’est pas le comportement prévu.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-130">In this case, MyProgram interprets that the first argument is C:\\Program, and the second argument is Files\\My, which is not the intended behavior.</span></span> <span data-ttu-id="3d8ec-131">Les arguments sont interprétés correctement, toutefois, qu’ils contiennent ou non des espaces, si les chaînes de développement sont encapsulées entre guillemets comme suit :</span><span class="sxs-lookup"><span data-stu-id="3d8ec-131">The arguments are interpreted correctly, however, regardless of whether they contain spaces, if the expanding strings are wrapped in quotation marks as follows:</span></span>

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a><span data-ttu-id="3d8ec-132">Ne confondez pas l’exécution automatique/la lecture automatique avec les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-132">Do Not Confuse Autoplay/Autorun with File Associations</span></span>

<span data-ttu-id="3d8ec-133">Les associations de fichiers sont similaires à la lecture automatique/exécution automatique d’une certaine manière.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-133">File Associations are similar to Autoplay/Autorun in some ways.</span></span> <span data-ttu-id="3d8ec-134">Toutefois, l’exécution automatique/autorun offre des fonctionnalités distinctes et distinctes de celles fournies par les associations de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-134">However, Autoplay/Autorun offers separate and distinct facilities from those provided by file associations.</span></span> <span data-ttu-id="3d8ec-135">Pour plus d’informations, consultez [création d’une application de CD-ROM compatible avec l’exécution automatique](autoplay.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ec-135">For more information see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).</span></span>

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a><span data-ttu-id="3d8ec-136">Ne confondez pas la base de données MIME d’Internet Explorer avec les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-136">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>

<span data-ttu-id="3d8ec-137">Les associations de fichiers sont similaires à la base de données MIME de Windows Internet Explorer, dans la mesure où les types de fichiers peuvent (et doivent) inclure une définition de type MIME.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-137">File Associations are similar to the Windows Internet Explorer MIME database, in that file types can (and should) include a MIME type definition.</span></span> <span data-ttu-id="3d8ec-138">Toutefois, la base de données MIME d’Internet Explorer est séparée et distincte des associations de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-138">However, the Internet Explorer MIME database is separate and distinct from file associations.</span></span>

## <a name="use-properly-formed-and-versioned-progids"></a><span data-ttu-id="3d8ec-139">Utiliser des ProgID correctement formés et avec version</span><span class="sxs-lookup"><span data-stu-id="3d8ec-139">Use Properly Formed and Versioned ProgIDs</span></span>

<span data-ttu-id="3d8ec-140">Utilisez toujours des [ProgID avec version](fa-progids.md), même s’il n’existe qu’une seule version du ProgID.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-140">Always use [versioned ProgIDs](fa-progids.md), even if there is only one version of the ProgID.</span></span> <span data-ttu-id="3d8ec-141">Les ProgID avec version permettent d’éviter les conflits de ProgID et les remplacements.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-141">Versioned ProgIDs help to avoid ProgID conflicts and overwrites.</span></span> <span data-ttu-id="3d8ec-142">Ils permettent également aux différentes versions d’une application de coexister.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-142">They also enable different versions of an application to co-exist.</span></span>

## <a name="do-not-use-short-file-name-extensions"></a><span data-ttu-id="3d8ec-143">Ne pas utiliser les extensions de nom de fichier courtes</span><span class="sxs-lookup"><span data-stu-id="3d8ec-143">Do Not Use Short File Name Extensions</span></span>

<span data-ttu-id="3d8ec-144">Les extensions de nom de fichier longues offrent les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="3d8ec-144">Long file name extensions offer the following advantages:</span></span>

-   <span data-ttu-id="3d8ec-145">La longueur limitée des extensions courtes les rend vulnérables aux *collisions d’extension.*</span><span class="sxs-lookup"><span data-stu-id="3d8ec-145">The limited length of short extensions make them prone to *extension collisions.*</span></span> <span data-ttu-id="3d8ec-146">Une collision d’extension se produit lorsque la même extension est utilisée pour classer plusieurs types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-146">An extension collision occurs when the same extension is used to classify multiple file types.</span></span> <span data-ttu-id="3d8ec-147">L’utilisation d’extensions longues réduit considérablement les risques de collision.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-147">Using long extensions significantly decreases the chances of a collision.</span></span>
-   <span data-ttu-id="3d8ec-148">Les noms de fichiers courts tendent à être énigmatiques.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-148">Short file names tend to be somewhat cryptic.</span></span> <span data-ttu-id="3d8ec-149">Les extensions longues ont tendance à être plus significatives, car des informations supplémentaires peuvent être incorporées dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-149">Long extensions tend to be more meaningful because additional information can be embedded in the extension.</span></span>

<span data-ttu-id="3d8ec-150">Pour plus d’informations, consultez [extensions de noms de fichiers](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="3d8ec-150">For more information, see [file name extensions](fa-file-extensions.md).</span></span>

## <a name="register-new-file-types-in-the-iana-mime-database"></a><span data-ttu-id="3d8ec-151">Inscrire de nouveaux types de fichiers dans la base de données MIME IANA</span><span class="sxs-lookup"><span data-stu-id="3d8ec-151">Register New File Types in the IANA MIME Database</span></span>

<span data-ttu-id="3d8ec-152">L’IANA (Internet Assigned Numbers Authority) conserve une base de données publique de types MIME inscrits.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-152">The Internet Assigned Numbers Authority (IANA) keeps a public database of registered MIME types.</span></span> <span data-ttu-id="3d8ec-153">Lors de la définition d’un nouveau type de fichier public, nous vous recommandons de définir également un type MIME pour le type de fichier et d’inscrire ce type auprès de l’IANA.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-153">When defining a new public file type, we recommended that you also define a MIME type for the file type and register this type with the IANA.</span></span> <span data-ttu-id="3d8ec-154">L’inscription n’est pas coûteuse.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-154">There is no cost for registration.</span></span>

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a><span data-ttu-id="3d8ec-155">S’inscrire auprès du service Web Windows pour les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-155">Sign Up with the Windows Web Service for File Associations</span></span>

<span data-ttu-id="3d8ec-156">Les développeurs d’applications peuvent s’inscrire auprès du service Web Windows que les utilisateurs utilisent pour trouver des applications qui peuvent fonctionner sur des types de fichiers spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3d8ec-156">Application developers can sign up with the Windows Web Service that users use to find applications that can operate on specific file types.</span></span> <span data-ttu-id="3d8ec-157">Le processus d’inscription au service Web est détaillé dans le [processus d’intégration du système d’association de fichiers Windows](https://support.microsoft.com/kb/929149).</span><span class="sxs-lookup"><span data-stu-id="3d8ec-157">The process for signing up with the web service is detailed in [Windows File Association System on-boarding process](https://support.microsoft.com/kb/929149).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d8ec-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d8ec-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d8ec-159">Exemple de scénario d’association de fichiers</span><span class="sxs-lookup"><span data-stu-id="3d8ec-159">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="3d8ec-160">Instructions pour la gestion des applications par défaut dans Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="3d8ec-160">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="3d8ec-161">Programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="3d8ec-161">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="3d8ec-162">Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)</span><span class="sxs-lookup"><span data-stu-id="3d8ec-162">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 




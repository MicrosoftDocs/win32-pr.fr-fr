---
title: Message Compiler (MC.exe)
description: Utilisé pour compiler des manifestes d’instrumentation et des fichiers texte de message.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- EventLog (MC.exe) du message
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524239"
---
# <a name="message-compiler-mcexe"></a><span data-ttu-id="e7ea2-104">Message Compiler (MC.exe)</span><span class="sxs-lookup"><span data-stu-id="e7ea2-104">Message Compiler (MC.exe)</span></span>

<span data-ttu-id="e7ea2-105">Utilisé pour compiler des manifestes d’instrumentation et des fichiers texte de message.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-105">Used to compile instrumentation manifests and message text files.</span></span> <span data-ttu-id="e7ea2-106">Le compilateur génère les fichiers de ressources de message auxquels votre application est liée.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-106">The compiler generates the message resource files to which your application links.</span></span>

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [<span data-ttu-id="e7ea2-107">Arguments communs aux fichiers de texte de message et aux fichiers manifeste</span><span class="sxs-lookup"><span data-stu-id="e7ea2-107">Arguments common to both message text files and manifest files</span></span>](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [<span data-ttu-id="e7ea2-108">Arguments spécifiques aux fichiers manifestes</span><span class="sxs-lookup"><span data-stu-id="e7ea2-108">Arguments specific to manifest files</span></span>](#arguments-specific-to-manifest-files)
-   [<span data-ttu-id="e7ea2-109">Arguments spécifiques à la génération de code que votre fournisseur utiliserait pour consigner des événements</span><span class="sxs-lookup"><span data-stu-id="e7ea2-109">Arguments specific to generating code that your provider would use to log events</span></span>](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [<span data-ttu-id="e7ea2-110">Arguments spécifiques aux fichiers texte du message</span><span class="sxs-lookup"><span data-stu-id="e7ea2-110">Arguments specific to message text files</span></span>](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a><span data-ttu-id="e7ea2-111">Arguments communs aux fichiers de texte de message et aux fichiers manifeste</span><span class="sxs-lookup"><span data-stu-id="e7ea2-111">Arguments common to both message text files and manifest files</span></span>

<dl> <dt>

<span data-ttu-id="e7ea2-112"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-112"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-113">Affiche les informations d’utilisation du compilateur de message.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-113">Displays the usage information for the Message Compiler.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-114"><span id="-c"></span><span id="-C"></span>**-c**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-114"><span id="-c"></span><span id="-C"></span>**-c**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-115">Utilisez cet argument pour que le compilateur définisse le bit client (bit 28) dans tous les ID de message.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-115">Use this argument to have the compiler set the customer bit (bit 28) in all message IDs.</span></span> <span data-ttu-id="e7ea2-116">Pour plus d’informations sur le bit du client, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-116">For information on the customer bit, see winerror.h.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-117"><span id="-cp"></span><span id="-CP"></span>**-** *encodage* CP</span><span class="sxs-lookup"><span data-stu-id="e7ea2-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-118">Utilisez cet argument pour spécifier l’encodage de caractères utilisé pour tous les fichiers texte générés.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-118">Use this argument to specify the character encoding used for all generated text files.</span></span> <span data-ttu-id="e7ea2-119">Les noms valides sont « ANSI » (par défaut), « UTF-8 » et « UTF-16 ».</span><span class="sxs-lookup"><span data-stu-id="e7ea2-119">Valid names include "ansi" (default), "utf-8", and "utf-16".</span></span> <span data-ttu-id="e7ea2-120">Les encodages Unicode ajoutent une marque d’ordre d’octet.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-120">The Unicode encodings will add a byte order mark.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>*extension* **-e**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extension*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-122">Utilisez cet argument pour spécifier l’extension à utiliser pour le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-122">Use this argument to specify the extension to use for the header file.</span></span> <span data-ttu-id="e7ea2-123">Vous pouvez spécifier jusqu’à trois caractères d’extension, à l’exclusion du point.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-123">You can specify up to a three characters extension, not including the period.</span></span> <span data-ttu-id="e7ea2-124">La valeur par défaut est. h.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-124">The default is .h.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *chemin*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *path*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-126">Utilisez cet argument pour spécifier le dossier dans lequel vous souhaitez que le compilateur place le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-126">Use this argument to specify the folder into which you want the compiler to place the generated header file.</span></span> <span data-ttu-id="e7ea2-127">L'emplacement par défaut est le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-127">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *longueur*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-129">Utilisez cet argument pour que le compilateur génère un avertissement si le message dépasse la *longueur* des caractères.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-129">Use this argument to have the compiler generate a warning if the any message exceeds *length* characters.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-131">Utilisez cet argument pour spécifier le dossier dans lequel vous souhaitez que le compilateur place le script généré du compilateur de ressources (fichier. RC) et les fichiers. bin générés (ressources binaires) inclus dans le script du compilateur de ressources.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-131">Use this argument to specify the folder into which you want the compiler to place the generated resource compiler script (.rc file) and the generated .bin files (binary resources) that the resource compiler script includes.</span></span> <span data-ttu-id="e7ea2-132">L'emplacement par défaut est le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-132">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-** *nom* z</span><span class="sxs-lookup"><span data-stu-id="e7ea2-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-134">Utilisez cet argument pour remplacer le nom de base par défaut que le compilateur utilise pour les fichiers qu’il génère.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-134">Use this argument to override the default base name that the compiler uses for the files that it generates.</span></span> <span data-ttu-id="e7ea2-135">La valeur par défaut consiste à utiliser le nom de base du fichier d’entrée de *nom* de fichier.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-135">The default is to use the base name of the *filename* input file.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-136"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-137">Fichier de manifeste d’instrumentation ou fichier texte de message.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-137">The instrumentation manifest file or message text file.</span></span> <span data-ttu-id="e7ea2-138">Le fichier doit exister dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-138">The file must exist in the current directory.</span></span> <span data-ttu-id="e7ea2-139">Vous pouvez spécifier un fichier manifeste, un fichier texte de message ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-139">You can specify a manifest file, message text file, or both.</span></span> <span data-ttu-id="e7ea2-140">Le nom de fichier doit inclure l’extension.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-140">The file name must include the extension.</span></span> <span data-ttu-id="e7ea2-141">La Convention consiste à utiliser une extension. Man pour les fichiers manifeste et une extension. MC pour les fichiers texte du message.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-141">The convention is to use a .man extension for manifest files and a .mc extension for message text files.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a><span data-ttu-id="e7ea2-142">Arguments spécifiques aux fichiers manifestes</span><span class="sxs-lookup"><span data-stu-id="e7ea2-142">Arguments specific to manifest files</span></span>

<dl> <dt>

<span data-ttu-id="e7ea2-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *path*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-144">Utilisez cet argument pour créer une ligne de base de votre instrumentation.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-144">Use this argument to create a baseline of your instrumentation.</span></span> <span data-ttu-id="e7ea2-145">Spécifiez le chemin d’accès au dossier qui contient vos fichiers manifeste de base de référence.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-145">Specify the path to the folder that contains your baseline manifest files.</span></span> <span data-ttu-id="e7ea2-146">Pour les versions ultérieures, vous utiliseriez ensuite l’argument **-t** pour vérifier le nouveau manifeste par rapport à la ligne de base pour les problèmes de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-146">For subsequent releases, you would then use the **-t** argument to check the new manifest against the baseline for compatibility issues.</span></span>

<span data-ttu-id="e7ea2-147">**Avant la version 1.12.7051 de MC :** Non disponible</span><span class="sxs-lookup"><span data-stu-id="e7ea2-147">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *path*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-149">Utilisez cet argument lorsque vous créez une nouvelle version de votre manifeste et que vous souhaitez vérifier la compatibilité des applications par rapport à la ligne de base que vous avez créée à l’aide de l’argument **-s** .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-149">Use this argument when you create a new version of your manifest and want to check it for application compatibility against the baseline that you created using the **-s** argument.</span></span> <span data-ttu-id="e7ea2-150">Le chemin d’accès doit pointer vers le dossier qui contient le. Fichiers BIN créés par l’opération de base (voir le commutateur **-s** ).</span><span class="sxs-lookup"><span data-stu-id="e7ea2-150">The path must point to the folder that contains the .BIN files that the baseline operation created (see the **-s** switch).</span></span>

<span data-ttu-id="e7ea2-151">**Avant la version 1.12.7051 de MC :** Non disponible</span><span class="sxs-lookup"><span data-stu-id="e7ea2-151">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *chemin*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *path*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-153">Le compilateur ignore cet argument et valide automatiquement le manifeste.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-153">The compiler ignores this argument and automatically validates the manifest.</span></span>

<span data-ttu-id="e7ea2-154">**Avant la version 1.12.7051 de MC :** Utilisez cet argument pour spécifier le dossier qui contient le fichier de schéma Eventic. xsd, que le compilateur utilise pour valider votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-154">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Eventman.xsd schema file, which the compiler uses to validate your manifest.</span></span> <span data-ttu-id="e7ea2-155">Le SDK Windows inclut le fichier de schéma Eventic. xsd dans le \\ dossier include.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-155">The Windows SDK includes the Eventman.xsd schema file in the \\Include folder.</span></span> <span data-ttu-id="e7ea2-156">Si vous ne spécifiez pas cet argument, le compilateur ne valide pas votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-156">If you do not specify this argument, the compiler does not validate your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *chemin*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *path*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-158">Le compilateur ignore cet argument.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-158">The compiler ignores this argument.</span></span>

<span data-ttu-id="e7ea2-159">**Avant la version 1.12.7051 de MC :** Utilisez cet argument pour spécifier le dossier qui contient le fichier Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-159">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Winmeta.xml file.</span></span> <span data-ttu-id="e7ea2-160">Le fichier Winmeta.xml contient les types d’entrée et de sortie reconnus, ainsi que les canaux, niveaux et OpCodes prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-160">The Winmeta.xml file contains the recognized input and output types as well as the predefined channels, levels, and opcodes.</span></span> <span data-ttu-id="e7ea2-161">Le SDK Windows inclut le fichier Winmeta.xml dans le \\ dossier include.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-161">The Windows SDK includes the Winmeta.xml file in the \\Include folder.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a><span data-ttu-id="e7ea2-162">Arguments spécifiques à la génération de code que votre fournisseur utiliserait pour consigner des événements</span><span class="sxs-lookup"><span data-stu-id="e7ea2-162">Arguments specific to generating code that your provider would use to log events</span></span>

<span data-ttu-id="e7ea2-163">Vous pouvez utiliser les arguments de compilateur suivants pour générer du code en mode noyau ou en mode utilisateur que vous pouvez utiliser pour consigner des événements.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-163">You can use the following compiler arguments to generate kernel-mode or user-mode code that you can use to log events.</span></span> <span data-ttu-id="e7ea2-164">Vous pouvez également demander que le compilateur génère du code pour prendre en charge l’écriture d’événements sur les ordinateurs antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-164">You can also request that the compiler generate code to support writing events on computers prior to Windows Vista.</span></span> <span data-ttu-id="e7ea2-165">Si votre application est écrite en C#, le compilateur peut générer une classe C# que vous pouvez utiliser pour consigner les événements.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-165">If your application is written C#, the compiler can generate a C# class that you can use to log events.</span></span> <span data-ttu-id="e7ea2-166">Ces arguments sont disponibles à partir de la version MC 1.12.7051 livrée avec la version Windows 7 du kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-166">These arguments are available beginning with MC version 1.12.7051 that ships with the Windows 7 version of the Window SDK.</span></span>

<dl> <dt>

<span data-ttu-id="e7ea2-167"><span id="-co"></span><span id="-CO"></span>**-Co**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-167"><span id="-co"></span><span id="-CO"></span>**-co**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-168">Utilisez cet argument pour que le service de journalisation appelle votre fonction définie par l’utilisateur pour chaque événement que vous journalisez (la fonction est appelée une fois que l’événement a été enregistré).</span><span class="sxs-lookup"><span data-stu-id="e7ea2-168">Use this argument to have the logging service call your user-defined function for each event that you log (the function is called after the event has been logged).</span></span> <span data-ttu-id="e7ea2-169">Votre fonction définie par l’utilisateur doit avoir la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-169">Your user-defined function must have the following signature.</span></span>


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



<span data-ttu-id="e7ea2-170">Vous devez également inclure la directive suivante dans votre code.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-170">You must also include the following directive in your code.</span></span>

`#define MCGEN_CALLOUT pFnUserFunction`

<span data-ttu-id="e7ea2-171">Vous devez conserver votre implémentation aussi rapidement que possible pour éviter les problèmes de journalisation ; le service ne consigne plus vos événements tant que la fonction n’est pas retournée.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-171">You should keep your implementation as short as possible to prevent logging issues; the service will not log anymore of your events until the function returns.</span></span>

<span data-ttu-id="e7ea2-172">Vous pouvez utiliser cet argument avec l’argument **-km** ou **-um** .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-172">You can use this argument with the **-km** or **-um** argument.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs (espace de** *noms* )</span><span class="sxs-lookup"><span data-stu-id="e7ea2-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-174">Utilisez cet argument pour que le compilateur génère une classe C# basée sur la classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-174">Use this argument to have the compiler generate a C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-espace de** *noms* CSS</span><span class="sxs-lookup"><span data-stu-id="e7ea2-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-176">Utilisez cet argument pour que le compilateur génère une classe C# statique basée sur la classe .NET 3,5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-176">Use this argument to have the compiler generate a static C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-177"><span id="-km"></span><span id="-KM"></span>**-km**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-177"><span id="-km"></span><span id="-KM"></span>**-km**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-178">Utilisez cet argument pour que le compilateur génère le code en mode noyau que vous utiliseriez pour enregistrer les événements définis dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-178">Use this argument to have the compiler generate the kernel-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-179"><span id="-mof"></span><span id="-MOF"></span>**-MOF**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-180">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-180">DEPRECATED.</span></span> <span data-ttu-id="e7ea2-181">Utilisez cet argument pour que le compilateur génère du code que vous pouvez utiliser pour consigner les événements sur les ordinateurs antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-181">Use this argument to have the compiler generate code that you can use to log events on computers prior to Windows Vista.</span></span> <span data-ttu-id="e7ea2-182">Cette option crée également un fichier MOF qui contient les classes MOF pour chaque événement défini dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-182">This option also creates a MOF file that contains the MOF classes for each event defined in the manifest.</span></span> <span data-ttu-id="e7ea2-183">Pour inscrire les classes dans le fichier MOF afin que les consommateurs puissent décoder les événements, utilisez le compilateur MOF (Mofcomp.exe).</span><span class="sxs-lookup"><span data-stu-id="e7ea2-183">To register the classes in the MOF file so that consumers can decode the events, use the MOF compiler (Mofcomp.exe).</span></span> <span data-ttu-id="e7ea2-184">Pour plus d’informations sur l’utilisation du compilateur MOF, consultez [format MOF](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e7ea2-184">For details on using the MOF compiler, see [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

<span data-ttu-id="e7ea2-185">Pour utiliser ce commutateur, vous devez respecter les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7ea2-185">To use this switch, you must adhere to the following restrictions:</span></span>

-   <span data-ttu-id="e7ea2-186">Chaque définition d’événement doit inclure les attributs Task et opcode</span><span class="sxs-lookup"><span data-stu-id="e7ea2-186">Every event definition must include the task and opcode attributes</span></span>
-   <span data-ttu-id="e7ea2-187">Chaque tâche doit inclure l’attribut eventGuid</span><span class="sxs-lookup"><span data-stu-id="e7ea2-187">Every task must include the eventGuid attribute</span></span>
-   <span data-ttu-id="e7ea2-188">Les données de modèle que les références d’événement ne peuvent pas contenir :</span><span class="sxs-lookup"><span data-stu-id="e7ea2-188">The template data that the event references cannot contain:</span></span>
    -   <span data-ttu-id="e7ea2-189">Éléments de données qui spécifient les types d’entrée Win : Binary ou Win : SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="e7ea2-189">Data items that specify the win:Binary or win:SYSTEMTIME input types</span></span>
    -   <span data-ttu-id="e7ea2-190">Structures</span><span class="sxs-lookup"><span data-stu-id="e7ea2-190">Structures</span></span>
    -   <span data-ttu-id="e7ea2-191">Tableaux de taille variable ; Toutefois, vous pouvez spécifier des tableaux de longueur fixe</span><span class="sxs-lookup"><span data-stu-id="e7ea2-191">Variable sized arrays; however, you can specify fixed length arrays</span></span>
    -   <span data-ttu-id="e7ea2-192">Les types de données String ne peuvent pas spécifier l’attribut length</span><span class="sxs-lookup"><span data-stu-id="e7ea2-192">String data types cannot specify the length attribute</span></span>

<span data-ttu-id="e7ea2-193">Vous devez utiliser cet argument avec l’argument **-um**, **-CS**, **-CSS** ou **-km**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-193">You must use this argument with the **-um**, **-cs**, **-css**, or **-km** argument</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *préfixe*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-195">Utilisez cet argument pour remplacer le préfixe par défaut que le compilateur utilise pour l’enregistrement des noms de macros et de méthodes.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-195">Use this argument to override the default prefix that the compiler uses for the logging macro names and method names.</span></span> <span data-ttu-id="e7ea2-196">Le préfixe par défaut est « EventWrite ».</span><span class="sxs-lookup"><span data-stu-id="e7ea2-196">The default prefix is "EventWrite".</span></span> <span data-ttu-id="e7ea2-197">La chaîne est sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-197">The string is case-sensitive.</span></span>

<span data-ttu-id="e7ea2-198">Vous pouvez utiliser cet argument avec l’argument **-um**, **-CS**, **-CSS** ou **-km** .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-198">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *préfixe*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-200">Utilisez cet argument pour supprimer des caractères au début du nom symbolique que vous avez spécifié pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-200">Use this argument to remove characters from the beginning of the symbolic name that you specified for the event.</span></span> <span data-ttu-id="e7ea2-201">La comparaison respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-201">The comparison is case-insensitive.</span></span> <span data-ttu-id="e7ea2-202">Le compilateur utilise le nom symbolique pour former les noms de macros et de méthodes de journalisation.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-202">The compiler uses the symbolic name to form the logging macro names and method names.</span></span>

<span data-ttu-id="e7ea2-203">Le nom par défaut d’une macro de journalisation est EventWrite *SymbolName*, où *SymbolName* est le nom symbolique que vous avez spécifié pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-203">The default name for a logging macro is EventWrite *SymbolName*, where *SymbolName* is the symbolic name that you specified for the event.</span></span> <span data-ttu-id="e7ea2-204">Par exemple, si vous affectez à l’attribut symbol de l’événement la valeur PrinterConnection, le nom de la macro est EventWritePrinterConnection.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-204">For example, if you set the symbol attribute of the event to PrinterConnection, the macro name would be EventWritePrinterConnection.</span></span> <span data-ttu-id="e7ea2-205">Pour supprimer l’imprimante du nom, utilisez l' **imprimante** **-P** , qui se traduit par EventWriteConnection.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-205">To remove Printer from the name, use **-P** **Printer**, which results in EventWriteConnection.</span></span>

<span data-ttu-id="e7ea2-206">Vous pouvez utiliser cet argument avec l’argument **-um**, **-CS**, **-CSS** ou **-km** .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-206">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-207"><span id="-um"></span><span id="-UM"></span>**-um**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-207"><span id="-um"></span><span id="-UM"></span>**-um**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-208">Utilisez cet argument pour que le compilateur génère le code en mode utilisateur que vous utiliseriez pour enregistrer les événements définis dans votre manifeste.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-208">Use this argument to have the compiler generate the user-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> </dl>

<span data-ttu-id="e7ea2-209">Pour que le compilateur génère du code de journalisation, vous devez spécifier l’argument **-um**, **-CS**, **-CSS** ou **-km** . ces arguments s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-209">To have the compiler generate logging code, you must specify the **-um**, **-cs**, **-css**, or **-km** argument; these arguments are mutually exclusive.</span></span>

<span data-ttu-id="e7ea2-210">Pour spécifier où placer les fichiers. h,. cs et. mof générés par le compilateur, utilisez l’argument **-h** .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-210">To specify where to place the .h, .cs, and .mof files that the compiler generates, use the **-h** argument.</span></span> <span data-ttu-id="e7ea2-211">Si vous ne spécifiez pas l’argument **-h** , les fichiers sont placés dans le dossier actif.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-211">If you do not specify the **-h** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="e7ea2-212">Pour spécifier où placer le fichier. RC et les fichiers binaires (qui contiennent les ressources de métadonnées) générés par le compilateur, utilisez l’argument **-r** .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-212">To specify where to place the .rc file and binary files (that contain the metadata resources) that the compiler generates, use the **-r** argument.</span></span> <span data-ttu-id="e7ea2-213">Si vous ne spécifiez pas l’argument **-r** , les fichiers sont placés dans le dossier actif.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-213">If you do not specify the **-r** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="e7ea2-214">Le compilateur utilise le nom de base du fichier d’entrée comme nom de base des fichiers qu’il génère.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-214">The compiler uses the base name of the input file as the base name of the files that it generates.</span></span> <span data-ttu-id="e7ea2-215">Pour spécifier un nom de base, utilisez l’argument **-z** .</span><span class="sxs-lookup"><span data-stu-id="e7ea2-215">To specify a base name, use the **-z** argument.</span></span>

### <a name="arguments-specific-to-message-text-files"></a><span data-ttu-id="e7ea2-216">Arguments spécifiques aux fichiers texte du message</span><span class="sxs-lookup"><span data-stu-id="e7ea2-216">Arguments specific to message text files</span></span>

<dl> <dt>

<span data-ttu-id="e7ea2-217"><span id="-a"></span><span id="-A"></span>**-a**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-217"><span id="-a"></span><span id="-A"></span>**-a**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-218">Utilisez cet argument pour spécifier que le fichier d’entrée de *nom* de fichier contient du contenu dans la page de codes Windows ANSI par défaut du système (CP_ACP).</span><span class="sxs-lookup"><span data-stu-id="e7ea2-218">Use this argument to specify that the *filename* input file contains content in the system-default Windows ANSI code page (CP_ACP).</span></span> <span data-ttu-id="e7ea2-219">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-219">This is the default.</span></span> <span data-ttu-id="e7ea2-220">Utilisez **-u** pour Unicode.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-220">Use **-u** for Unicode.</span></span> <span data-ttu-id="e7ea2-221">Si le fichier d’entrée contient une nomenclature, cet argument est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-221">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-222"><span id="-A"></span><span id="-a"></span>**-A**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-222"><span id="-A"></span><span id="-a"></span>**-A**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-223">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-223">DEPRECATED.</span></span> <span data-ttu-id="e7ea2-224">Utilisez cet argument pour spécifier que les messages dans le fichier output. bin doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-224">Use this argument to specify that the messages in the output .bin file should be ANSI.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-225"><span id="-b"></span><span id="-B"></span>**-b**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-225"><span id="-b"></span><span id="-B"></span>**-b**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-226">Utilisez cet argument pour que le compilateur utilise le nom de base du fichier d’entrée de *nom* de fichier pour les noms de fichiers. bin.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-226">Use this argument to have the compiler use the base name of the *filename* input file for the .bin file names.</span></span> <span data-ttu-id="e7ea2-227">La valeur par défaut consiste à utiliser « MSG ».</span><span class="sxs-lookup"><span data-stu-id="e7ea2-227">The default is to use "MSG".</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-228"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-228"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-229">Utilisez cet argument pour utiliser des valeurs décimales pour les constantes de gravité et de fonction dans le fichier d’en-tête au lieu de valeurs hexadécimales.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-229">Use this argument to use decimal values for the Severity and Facility constants in the header file instead of hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-230"><span id="-n"></span><span id="-N"></span>**-n**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-230"><span id="-n"></span><span id="-N"></span>**-n**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-231">Utilisez cet argument pour spécifier que les messages se terminent immédiatement après le corps du message.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-231">Use this argument to specify that messages terminate immediately after the message body.</span></span> <span data-ttu-id="e7ea2-232">La valeur par défaut consiste à terminer le corps du message par un CR/LF.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-232">The default is to terminate the message body with a CR/LF.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-233"><span id="-o"></span><span id="-O"></span>**-o**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-233"><span id="-o"></span><span id="-O"></span>**-o**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-234">Utilisez cet argument pour que le compilateur génère un fichier d’en-tête OLE2 à l’aide de définitions **HRESULT** au lieu de codes d’État.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-234">Use this argument to have the compiler generate an OLE2 header file using **HRESULT** definitions instead of status codes.</span></span> <span data-ttu-id="e7ea2-235">L’utilisation de codes d’État est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-235">Using status codes is the default.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-236"><span id="-u"></span><span id="-U"></span>**-u**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-236"><span id="-u"></span><span id="-U"></span>**-u**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-237">Utilisez cet argument pour spécifier que le fichier d’entrée de *nom* de fichier contient du contenu UTF-16LE.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-237">Use this argument to specify that the *filename* input file contains UTF-16LE content.</span></span> <span data-ttu-id="e7ea2-238">La valeur par défaut est le contenu ANSI.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-238">The default is ANSI content.</span></span> <span data-ttu-id="e7ea2-239">Si le fichier d’entrée contient une nomenclature, cet argument est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-239">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-240"><span id="-U"></span><span id="-u"></span>**-U**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-240"><span id="-U"></span><span id="-u"></span>**-U**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-241">Utilisez cet argument pour spécifier que les messages dans le fichier output. bin doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-241">Use this argument to specify that the messages in the output .bin file should be Unicode.</span></span> <span data-ttu-id="e7ea2-242">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-242">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-243"><span id="-v"></span><span id="-V"></span>**-v**</span><span class="sxs-lookup"><span data-stu-id="e7ea2-243"><span id="-v"></span><span id="-V"></span>**-v**</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-244">Utilisez cet argument pour générer une sortie détaillée.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-244">Use this argument to generate verbose output.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea2-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *chemin*</span><span class="sxs-lookup"><span data-stu-id="e7ea2-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span></span>
</dt> <dd>

<span data-ttu-id="e7ea2-246">Utilisez cet argument pour spécifier le dossier dans lequel vous souhaitez que le compilateur place le fichier include. dbg C.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-246">Use this argument to specify the folder into which you want the compiler to place the .dbg C include file.</span></span> <span data-ttu-id="e7ea2-247">Le fichier. dbg mappe les ID de message à leurs noms symboliques.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-247">The .dbg file maps message IDs to their symbolic names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7ea2-248">Notes</span><span class="sxs-lookup"><span data-stu-id="e7ea2-248">Remarks</span></span>

<span data-ttu-id="e7ea2-249">Les arguments **-A** et **-MOF** sont déconseillés et seront supprimés à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-249">The **-A** and **-mof** arguments are deprecated and will be removed in the future.</span></span>

<span data-ttu-id="e7ea2-250">Le compilateur accepte comme entrée un fichier manifeste (. Man) ou un fichier texte de message (. MC) et génère les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="e7ea2-250">The compiler accepts as input a manifest (.man) file or a message text (.mc) file and generates the following files:</span></span>

-   <span data-ttu-id="e7ea2-251">*nom de fichier*. h</span><span class="sxs-lookup"><span data-stu-id="e7ea2-251">*filename*.h</span></span>

    <span data-ttu-id="e7ea2-252">Fichier d’en-tête C/C++ qui contient les descripteurs d’événement, le GUID du fournisseur et les noms de symboles que vous référencez dans votre application.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-252">A C/C++ header file that contains the event descriptors, provider GUID, and symbol names that you reference in your application.</span></span>

-   <span data-ttu-id="e7ea2-253">*nom du fichier* TEMP. bin</span><span class="sxs-lookup"><span data-stu-id="e7ea2-253">*filename* TEMP.bin</span></span>

    <span data-ttu-id="e7ea2-254">Fichier de ressources binaire qui contient le fournisseur et les métadonnées d’événement.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-254">A binary resource file that contains the provider and event metadata.</span></span> <span data-ttu-id="e7ea2-255">Il s’agit de la ressource de modèle, qui est indiquée par le suffixe temporaire du nom de base du fichier.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-255">This is the template resource, which is signified by the TEMP suffix of the base name of the file.</span></span>

-   <span data-ttu-id="e7ea2-256">Msg00001. bin</span><span class="sxs-lookup"><span data-stu-id="e7ea2-256">Msg00001.bin</span></span>

    <span data-ttu-id="e7ea2-257">Un fichier de ressources binaire pour chaque langue que vous spécifiez (par exemple, si votre manifeste contient des chaînes de message en-US et fr-FR, le compilateur génère Msg00001. bin et Msg00002. bin).</span><span class="sxs-lookup"><span data-stu-id="e7ea2-257">A binary resource file for each language that you specify (for example, if your manifest contains message strings in en-US and fr-FR, the compiler would generate Msg00001.bin and Msg00002.bin).</span></span>

-   <span data-ttu-id="e7ea2-258">*nom de fichier*. RC</span><span class="sxs-lookup"><span data-stu-id="e7ea2-258">*filename*.rc</span></span>

    <span data-ttu-id="e7ea2-259">Script du compilateur de ressources qui contient les instructions pour inclure chaque fichier. bin en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-259">A resource compiler script that contains the statements to include each .bin file as a resource.</span></span>

<span data-ttu-id="e7ea2-260">Pour les arguments qui acceptent un chemin d’accès, le chemin d’accès peut être un chemin d’accès absolu, relatif ou UNC et il peut contenir des variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-260">For arguments that take a path, the path can be an absolute, relative, or UNC path and it can contain environment variables.</span></span>

<span data-ttu-id="e7ea2-261">**Avant la version 1.12.7051 de MC :** Le compilateur n’autorise pas les chemins d’accès relatifs ou les variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-261">**Prior to MC version 1.12.7051:** The compiler does not allow relative paths or environment variables.</span></span>

<span data-ttu-id="e7ea2-262">Le SDK Windows comprend le compilateur (mc.exe) dans le \\ dossier bin.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-262">The Windows SDK includes the compiler (mc.exe) in the \\Bin folder.</span></span>

## <a name="examples"></a><span data-ttu-id="e7ea2-263">Exemples</span><span class="sxs-lookup"><span data-stu-id="e7ea2-263">Examples</span></span>

<span data-ttu-id="e7ea2-264">L’exemple suivant compile un manifeste à l’aide des valeurs par défaut du compilateur.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-264">The following example compiles a manifest using the compiler defaults.</span></span>

``` syntax
mc spooler.man
```

<span data-ttu-id="e7ea2-265">L’exemple suivant compile le manifeste et place l’en-tête et les fichiers de ressources dans les dossiers spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e7ea2-265">The following example compiles the manifest and places the header and resource files in the specified folders.</span></span>

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a><span data-ttu-id="e7ea2-266">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7ea2-266">Requirements</span></span>

| <span data-ttu-id="e7ea2-267">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7ea2-267">Requirement</span></span> | <span data-ttu-id="e7ea2-268">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7ea2-268">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="e7ea2-269">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7ea2-269">Minimum supported client</span></span> | <span data-ttu-id="e7ea2-270">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7ea2-270">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="e7ea2-271">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7ea2-271">Minimum supported server</span></span> | <span data-ttu-id="e7ea2-272">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7ea2-272">Windows 2000 Server \[desktop apps only\]</span></span>       |

---
description: Le compilateur format MOF (MOF) analyse un fichier contenant des instructions MOF et ajoute les classes et les instances de classe définies dans le fichier à l’espace de stockage WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863325"
---
# <a name="mofcomp"></a><span data-ttu-id="78d9e-103">mofcomp</span><span class="sxs-lookup"><span data-stu-id="78d9e-103">mofcomp</span></span>

<span data-ttu-id="78d9e-104">Le compilateur [*format MOF (MOF)*](gloss-m.md) analyse un fichier contenant des instructions MOF et ajoute les classes et les instances de classe définies dans le fichier à l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-104">The [*Managed Object Format (MOF)*](gloss-m.md) compiler parses a file containing MOF statements and adds the classes and class instances defined in the file to the WMI repository.</span></span> <span data-ttu-id="78d9e-105">Les fichiers MOF sont généralement compilés automatiquement lors de l’installation des systèmes avec lesquels ils sont fournis, mais vous pouvez également compiler les fichiers MOF à l’aide de cet outil.</span><span class="sxs-lookup"><span data-stu-id="78d9e-105">MOF files are usually automatically compiled during the installation of the systems with which they are provided, but you can also compile MOF files by using this tool.</span></span>

<span data-ttu-id="78d9e-106">Pour plus d’informations sur la localisation et l’utilisation de mofcomp.exe, consultez [utilisation des outils de gestion WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="78d9e-106">For more information about locating and using mofcomp.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span> <span data-ttu-id="78d9e-107">Pour plus d’informations sur la suppression de classes et d’instances de l’espace de stockage WMI, consultez la commande de préprocesseur [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="78d9e-107">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="78d9e-108">L’exemple de code suivant montre comment exécuter le compilateur MOF sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="78d9e-108">The following code example shows how to run the MOF compiler on a file.</span></span>

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a><span data-ttu-id="78d9e-109">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="78d9e-109">Switches</span></span>

<dl> <dt>

<span data-ttu-id="78d9e-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-récupération automatique**</span><span class="sxs-lookup"><span data-stu-id="78d9e-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-111">Ajoute le fichier MOF nommé à la liste des fichiers compilés au cours de la récupération du référentiel.</span><span class="sxs-lookup"><span data-stu-id="78d9e-111">Adds the named MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="78d9e-112">La liste des fichiers MOF de récupération automatique est stockée dans la clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="78d9e-112">The list of autorecover MOF files is stored in the registry key:</span></span>

<span data-ttu-id="78d9e-113">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**</span><span class="sxs-lookup"><span data-stu-id="78d9e-113">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM\\**</span></span>

<span data-ttu-id="78d9e-114">Les fichiers MOF listés dans cette entrée de Registre doivent résider sur l’ordinateur local, car les fichiers MOF qui utilisent la commande **AutoRecover** ne peuvent pas récupérer les fichiers MOF situés sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="78d9e-114">The MOF files listed in this registry entry must reside on the local computer because MOF files that use the **autorecover** command cannot recover MOF files located on a remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="78d9e-115">Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction [**\# pragma AutoRecover**](pragma-autorecover.md) de préprocesseur dans votre fichier [*format MOF*](gloss-m.md) (MOF).</span><span class="sxs-lookup"><span data-stu-id="78d9e-115">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format*](gloss-m.md) (MOF) file.</span></span>

 

</dd> <dt>

<span data-ttu-id="78d9e-116"><span id="-check"></span><span id="-CHECK"></span>**-vérifier**</span><span class="sxs-lookup"><span data-stu-id="78d9e-116"><span id="-check"></span><span id="-CHECK"></span>**-check**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-117">Demande que le compilateur effectue une vérification de la syntaxe uniquement et imprime les messages d’erreur appropriés.</span><span class="sxs-lookup"><span data-stu-id="78d9e-117">Requests that the compiler perform a syntax check only and print appropriate error messages.</span></span> <span data-ttu-id="78d9e-118">Aucun autre commutateur ne peut être utilisé avec ce commutateur.</span><span class="sxs-lookup"><span data-stu-id="78d9e-118">No other switch can be used with this switch.</span></span> <span data-ttu-id="78d9e-119">Lorsque ce commutateur est utilisé, aucune connexion à Windows Management Instrumentation (WMI) n’est établie et aucune modification n’est apportée au référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-119">When this switch is used, no connection to Windows Management Instrumentation (WMI) is established and no modifications to the WMI repository are made.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N : <** _NamespacePath_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<**_namespacepath_*_>_*</span></span>
</dt> <dd><span data-ttu-id="78d9e-121">Demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que *NamespacePath*.</span><span class="sxs-lookup"><span data-stu-id="78d9e-121">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="78d9e-122">Le MOF compilé est chargé dans l’espace de noms mofcomp par défaut, racine \\ par défaut, sauf si ce commutateur est utilisé.</span><span class="sxs-lookup"><span data-stu-id="78d9e-122">The compiled MOF is loaded into the default Mofcomp namespace, root\\default, unless this switch is used.</span></span> <span data-ttu-id="78d9e-123">Vous pouvez également insérer l’espace de noms du pragma de commande du préprocesseur **\# («**_chemin d’accès de l’espace de noms_*_»)_* dans le fichier MOF pour obtenir le même effet.</span><span class="sxs-lookup"><span data-stu-id="78d9e-123">You can also insert the preprocessor command **\#pragma namespace ("**_namespace path_*_")_* in the MOF file to achieve the same effect.</span></span> <span data-ttu-id="78d9e-124">Si le commutateur **-N :** et la commande de l' \# <a href="pragma-namespace.md">espace de noms pragma</a> sont utilisés, la \# **récupération automatique** de l' **espace de noms pragma** est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="78d9e-124">If both the **-N:** switch and the \#<a href="pragma-namespace.md">pragma namespace</a> command are used, \#**pragma namespace** **autorecover** takes priority.</span></span> <span data-ttu-id="78d9e-125">Dans ce cas, la seule façon de compiler le MOF dans un autre espace de noms consiste à modifier le fichier MOF et à modifier la \# commande **pragma namespace** .</span><span class="sxs-lookup"><span data-stu-id="78d9e-125">In this case, the only way to compile the MOF into another namespace is to edit the MOF file and change the \#**pragma namespace** command.</span></span> <span data-ttu-id="78d9e-126">Un ordinateur distant peut être spécifié à l’aide de la \\ \\ \\ racine MachineName \\ default.</span><span class="sxs-lookup"><span data-stu-id="78d9e-126">A remote computer can be specified using \\\\machinename\\root\\default.</span></span></dd> <dt>

<span data-ttu-id="78d9e-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Class : CreateOnly**</span><span class="sxs-lookup"><span data-stu-id="78d9e-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-128">Demande que le compilateur n’apporte aucune modification aux classes existantes.</span><span class="sxs-lookup"><span data-stu-id="78d9e-128">Requests that the compiler not make any changes to existing classes.</span></span> <span data-ttu-id="78d9e-129">Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une classe spécifiée dans le fichier MOF existe déjà.</span><span class="sxs-lookup"><span data-stu-id="78d9e-129">When this switch is used, the compile operation terminates if a class specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Class : ForceUpdate**</span><span class="sxs-lookup"><span data-stu-id="78d9e-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-131">Force les mises à jour des classes lorsque des classes enfants sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="78d9e-131">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="78d9e-132">Par exemple, supposons qu’un qualificateur de classe est défini dans une classe enfant et que la classe de base tente d’ajouter le même qualificateur.</span><span class="sxs-lookup"><span data-stu-id="78d9e-132">For example, suppose a class qualifier is defined in a child class and the base class tries to add the same qualifier.</span></span> <span data-ttu-id="78d9e-133">Dans la **classe :** le mode ForceUpdate, le compilateur MOF résout ce conflit en supprimant le qualificateur en conflit dans la classe enfant.</span><span class="sxs-lookup"><span data-stu-id="78d9e-133">In **-class:forceupdate** mode, the MOF compiler resolves this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="78d9e-134">Si la classe enfant a des instances, la mise à jour forcée échoue.</span><span class="sxs-lookup"><span data-stu-id="78d9e-134">If the child class has instances, the forced update fails.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-Class : safeupdate**</span><span class="sxs-lookup"><span data-stu-id="78d9e-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-136">Autorise les mises à jour des classes, même s’il existe des classes enfants, à condition que la modification n’entraîne pas de conflits avec les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="78d9e-136">Allows updates of classes even if there are child classes, as long as the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="78d9e-137">Par exemple, cet indicateur permet d’ajouter une nouvelle propriété à la classe de base qui n’a pas été mentionnée précédemment dans les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="78d9e-137">For example, this flag allows adding a new property to the base class that was not previously mentioned in child classes.</span></span> <span data-ttu-id="78d9e-138">Si les classes enfants ont des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="78d9e-138">If the child classes have instances, the update fails.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-Class : updateonly**</span><span class="sxs-lookup"><span data-stu-id="78d9e-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-140">Demande que le compilateur ne crée pas de nouvelles classes.</span><span class="sxs-lookup"><span data-stu-id="78d9e-140">Requests that the compiler not create any new classes.</span></span> <span data-ttu-id="78d9e-141">Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une classe spécifiée dans le fichier MOF n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="78d9e-141">When this switch is used, the compile operation terminates if a class specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance : updateonly**</span><span class="sxs-lookup"><span data-stu-id="78d9e-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-143">Demande que le compilateur ne crée pas de nouvelles instances.</span><span class="sxs-lookup"><span data-stu-id="78d9e-143">Requests that the compiler not create any new instances.</span></span> <span data-ttu-id="78d9e-144">Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une instance spécifiée dans le fichier MOF n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="78d9e-144">When this switch is used, the compile operation terminates if an instance specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance : CreateOnly**</span><span class="sxs-lookup"><span data-stu-id="78d9e-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-146">Demande que le compilateur n’apporte aucune modification aux instances existantes.</span><span class="sxs-lookup"><span data-stu-id="78d9e-146">Requests that the compiler not make any changes to existing instances.</span></span> <span data-ttu-id="78d9e-147">Lorsque ce commutateur est utilisé, l’opération de compilation se termine si une instance spécifiée dans le fichier MOF existe déjà.</span><span class="sxs-lookup"><span data-stu-id="78d9e-147">When this switch is used, the compile operation terminates if an instance specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B : <** _nom de fichier_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<**_filename_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-149">Demande que le compilateur crée une version binaire du fichier MOF portant le nom *filename* sans apporter de modification au référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-149">Requests that the compiler create a binary version of the MOF file with the name *filename* without making any modifications to the WMI repository.</span></span>

<span data-ttu-id="78d9e-150">Si vous utilisez l’option **-B : <** _nom_ *_>_* de fichier pour créer un fichier MOF binaire, seules les versions de qualificateur par défaut sont stockées dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-150">If you use the **-B:<**_filename_*_>_* option to create a binary MOF file, only default qualifier flavors are stored in the WMI repository.</span></span>

<span data-ttu-id="78d9e-151">Le format MOF binaire est le format intermédiaire pour combiner un pilote WDM avec le MOF en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="78d9e-151">Binary MOF format is the intermediate format for combining a WDM-driver with the MOF as a resource.</span></span> <span data-ttu-id="78d9e-152">Le MOF binaire représente des classes et des instances comme un fichier MOF de texte et est compressé avant d’être stocké sur le disque.</span><span class="sxs-lookup"><span data-stu-id="78d9e-152">The binary MOF represents classes and instances just as a text MOF file does and is compressed before it is stored on disk.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span><span class="sxs-lookup"><span data-stu-id="78d9e-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-154">Demande que le compilateur effectue une vérification de la syntaxe WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-154">Requests that the compiler perform a WMI syntax check.</span></span> <span data-ttu-id="78d9e-155">Le commutateur **-B :** doit être utilisé avec ce commutateur.</span><span class="sxs-lookup"><span data-stu-id="78d9e-155">The **-B:** switch must be used with this switch.</span></span> <span data-ttu-id="78d9e-156">Le commutateur **-WMI** est utilisé uniquement pour générer des fichiers MOF binaires utilisables par les pilotes de périphériques WDM.</span><span class="sxs-lookup"><span data-stu-id="78d9e-156">The **-WMI** switch is only used for building binary MOF files for use by WDM device drivers.</span></span> <span data-ttu-id="78d9e-157">Ce commutateur appelle un vérificateur de fichiers MOF binaire distinct qui s’exécute après la création du fichier MOF binaire.</span><span class="sxs-lookup"><span data-stu-id="78d9e-157">This switch invokes a separate binary MOF file checker, which runs after the binary MOF file is created.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P : <** _mot de passe_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<**_Password_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-159">*Spécifie le mot de* passe pour l’utilisateur de l’ordinateur à entrer lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="78d9e-159">Specifies *Password* as the password for the computer user to enter when logging on.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U : <** _nom d’utilisateur_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<**_UserName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-161">Spécifie le nom d’utilisateur comme nom de l' *utilisateur qui ouvre* une session.</span><span class="sxs-lookup"><span data-stu-id="78d9e-161">Specifies *UserName* as the name of the user logging on.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A :** _autorité_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<**_Authority_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-163">Spécifie l' *autorité* en tant qu’autorité (nom de domaine) à utiliser lors de la connexion à WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-163">Specifies *Authority* as the authority (domain name) to use when logging on to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF :** _chemin d’accès_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-165">Nom de la sortie neutre de la langue.</span><span class="sxs-lookup"><span data-stu-id="78d9e-165">Name of the language neutral output.</span></span> <span data-ttu-id="78d9e-166">Utilisé avec le commutateur **-Amendement** pour spécifier le nom du fichier MOF indépendant de la langue qui sera généré.</span><span class="sxs-lookup"><span data-stu-id="78d9e-166">Used with the **-AMENDMENT** switch to specify the name of the language-neutral MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL :** _chemin d’accès_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-168">Nom de la sortie spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="78d9e-168">Name of the language specific output.</span></span> <span data-ttu-id="78d9e-169">Utilisé avec le commutateur **-Amendement** pour spécifier le nom du fichier MOF propre à la langue qui sera généré.</span><span class="sxs-lookup"><span data-stu-id="78d9e-169">Used with the **-AMENDMENT** switch to specify the name of the language-specific MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Amendement : <** _paramètres régionaux_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<**_Locale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-171">Divise le fichier MOF en versions indépendantes du langage et spécifiques.</span><span class="sxs-lookup"><span data-stu-id="78d9e-171">Splits the MOF file into language-neutral and -specific versions.</span></span> <span data-ttu-id="78d9e-172">Le compilateur MOF crée une forme indépendante du langage du fichier MOF dont tous les qualificateurs modifiés ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="78d9e-172">The MOF compiler creates a language-neutral form of the MOF file that has all amended qualifiers removed.</span></span> <span data-ttu-id="78d9e-173">Une version localisée du fichier MOF est également créée avec une extension de nom de fichier MFL.</span><span class="sxs-lookup"><span data-stu-id="78d9e-173">A localized version of the MOF file is also created with an MFL file name extension.</span></span> <span data-ttu-id="78d9e-174">Les paramètres *régionaux* spécifient le nom de l’espace de noms enfant qui contient les définitions de classe localisées.</span><span class="sxs-lookup"><span data-stu-id="78d9e-174">The *Locale* parameter specifies the name of the child namespace that contains the localized class definitions.</span></span> <span data-ttu-id="78d9e-175">Le format des paramètres *régionaux* est MS \_ xxx, où xxx est la valeur hexadécimale du LCID Windows.</span><span class="sxs-lookup"><span data-stu-id="78d9e-175">The format of the *Locale* parameter is MS\_xxx where xxx is the hexadecimal value of the Windows LCID.</span></span> <span data-ttu-id="78d9e-176">Par exemple, les paramètres régionaux pour l’anglais américain sont MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="78d9e-176">For example, the locale for American English is MS\_409.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _resourceName_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <**_ResourceName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-178">Extrait le fichier MOF binaire à partir d’une ressource nommée.</span><span class="sxs-lookup"><span data-stu-id="78d9e-178">Extracts binary MOF from a named resource.</span></span> <span data-ttu-id="78d9e-179">Ce commutateur obtient le fichier MOF binaire de la classe dans l’espace de stockage WMI, tandis que le commutateur-B crée le format MOF binaire à partir d’un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="78d9e-179">This switch gets the binary MOF from the class in the WMI repository while the -B switch creates the binary MOF format from a MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L : <** _ResourceLocale_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<**_ResourceLocale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-181">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="78d9e-181">Optional.</span></span> <span data-ttu-id="78d9e-182">Extrait les descriptions localisées de MOF à partir du fichier MOF binaire en cas d’utilisation avec le commutateur-ER.</span><span class="sxs-lookup"><span data-stu-id="78d9e-182">Extracts the localized MOF descriptions from the binary MOF when used with -ER switch.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span><span class="sxs-lookup"><span data-stu-id="78d9e-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-184">Nom du fichier à analyser.</span><span class="sxs-lookup"><span data-stu-id="78d9e-184">Name of the file to parse.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="78d9e-185">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="78d9e-185">Return Values</span></span>

<span data-ttu-id="78d9e-186">Comme première opération, le compilateur MOF effectue une vérification de la syntaxe du fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="78d9e-186">As its first operation, the MOF compiler performs a syntax check on the MOF file.</span></span> <span data-ttu-id="78d9e-187">Si le compilateur détecte des erreurs, il affiche un message d’erreur et le processus se termine.</span><span class="sxs-lookup"><span data-stu-id="78d9e-187">If the compiler finds any errors, it prints an error message and the process terminates.</span></span>

<span data-ttu-id="78d9e-188">Le compilateur MOF peut retourner les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="78d9e-188">The MOF compiler can return the following values:</span></span>

<dl> <dt>

<span data-ttu-id="78d9e-189"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="78d9e-189"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-190">L’opération de compilation MOF a réussi.</span><span class="sxs-lookup"><span data-stu-id="78d9e-190">MOF compile operation was successful.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-191"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="78d9e-191"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-192">Le compilateur MOF n’a pas pu se connecter au serveur WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-192">The MOF compiler could not connect with the WMI server.</span></span> <span data-ttu-id="78d9e-193">Cela est dû à une erreur sémantique, telle qu’une incompatibilité avec le référentiel WMI existant ou à une erreur réelle, telle que l’échec du démarrage du serveur WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-193">This is either because of a semantic error such as an incompatibility with the existing WMI repository or an actual error such as the failure of the WMI server to start.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-194"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="78d9e-194"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-195">Un ou plusieurs commutateurs de ligne de commande ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="78d9e-195">One or more command-line switches were not valid.</span></span>

</dd> <dt>

<span data-ttu-id="78d9e-196"><span id="3"></span>1,3</span><span class="sxs-lookup"><span data-stu-id="78d9e-196"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="78d9e-197">Une erreur de syntaxe MOF s’est produite.</span><span class="sxs-lookup"><span data-stu-id="78d9e-197">A MOF syntax error occurred.</span></span>

</dd> </dl>

<span data-ttu-id="78d9e-198">Si le fichier MOF est correctement analysé, mais qu’une tentative est effectuée pour effectuer une opération qui est interdite par un commutateur de ligne de commande, le compilateur retourne un code d’erreur généré par WMI au lieu de l’un des codes de retour répertoriés dans la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="78d9e-198">If the MOF file is parsed correctly, but an attempt is made to perform an operation that is forbidden by a command-line switch, the compiler returns an error code generated by WMI instead of any of the return codes listed in the list preceding.</span></span> <span data-ttu-id="78d9e-199">Par exemple, un code d’erreur WMI est retourné lorsque le commutateur **-instance : updateonly** est spécifié et que le fichier MOF tente de créer une instance.</span><span class="sxs-lookup"><span data-stu-id="78d9e-199">For example, a WMI error code is returned when the **-instance:updateonly** switch is specified and the MOF file attempts to create an instance.</span></span>

<span data-ttu-id="78d9e-200">Si l’instruction de préprocesseur [**\# pragma autoautorecover**](pragma-autorecover.md) ne figure pas dans le fichier, l’avertissement suivant est retourné :</span><span class="sxs-lookup"><span data-stu-id="78d9e-200">If the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement is not in the file, then the following warning is returned:</span></span>

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a><span data-ttu-id="78d9e-201">Notes</span><span class="sxs-lookup"><span data-stu-id="78d9e-201">Remarks</span></span>

<span data-ttu-id="78d9e-202">Le compilateur MOF est disponible dans le répertoire% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="78d9e-202">The MOF Compiler is available in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="78d9e-203">Vous devez spécifier le fichier MOF comme paramètre du compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="78d9e-203">You must specify the MOF file as the parameter of the MOF Compiler.</span></span> <span data-ttu-id="78d9e-204">Vous pouvez également spécifier un commutateur de récupération automatique si vous souhaitez que le fichier MOF soit recompilé automatiquement si le référentiel CIM doit être automatiquement récupéré.</span><span class="sxs-lookup"><span data-stu-id="78d9e-204">You can also specify an Autorecover switch if you want the MOF file to be automatically recompiled if the CIM Repository ever has to be automatically recovered.</span></span> <span data-ttu-id="78d9e-205">Pour plus d’informations, tapez **mofcomp/ ?**</span><span class="sxs-lookup"><span data-stu-id="78d9e-205">For more information, type **Mofcomp /?**</span></span> <span data-ttu-id="78d9e-206">à l'invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="78d9e-206">at the command prompt.</span></span>

<span data-ttu-id="78d9e-207">Un fichier MOF qui utilise le jeu de caractères Unicode contient une signature en tant que deux premiers octets du fichier.</span><span class="sxs-lookup"><span data-stu-id="78d9e-207">A MOF file that uses the Unicode character set contains a signature as the first two bytes of the file.</span></span> <span data-ttu-id="78d9e-208">Cette signature est U + FFFE ou U + FEFF, en fonction de l’ordre des octets du fichier.</span><span class="sxs-lookup"><span data-stu-id="78d9e-208">This signature is either U+FFFE or U+FEFF, depending on the byte ordering of the file.</span></span>

<span data-ttu-id="78d9e-209">Si aucune erreur ne se produit dans le processus d’analyse, le compilateur MOF se connecte au serveur WMI qui s’exécute sur l’ordinateur local, sauf si le commutateur **-Check** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="78d9e-209">When no errors occur in the parsing process, the MOF compiler connects to the WMI server running on the local computer unless the **-check** switch is specified.</span></span> <span data-ttu-id="78d9e-210">Les classes et les instances définies dans le fichier MOF sont ajoutées à l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="78d9e-210">Classes and instances defined in the MOF file are added to the WMI repository.</span></span>

<span data-ttu-id="78d9e-211">Lorsqu’une erreur se produit lors de la mise à jour de l’espace de stockage WMI, le compilateur n’effectue aucune tentative pour retourner le référentiel à son état avant le début du traitement du compilateur.</span><span class="sxs-lookup"><span data-stu-id="78d9e-211">When an error occurs in updating the WMI repository, the compiler makes no attempt to return the repository to its state before the compiler began processing.</span></span>

<span data-ttu-id="78d9e-212">**Windows 8 :** Lors de l’installation d’un fournisseur, mofcomp traite les \[ \] qualificateurs de clé et \[ statique \] comme true s’ils sont présents, indépendamment de leurs valeurs réelles.</span><span class="sxs-lookup"><span data-stu-id="78d9e-212">**Windows 8:** When installing a provider, mofcomp treats the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="78d9e-213">D’autres qualificateurs sont considérés comme false s’ils sont présents, mais ne sont pas explicitement définis sur true.</span><span class="sxs-lookup"><span data-stu-id="78d9e-213">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d9e-214">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78d9e-214">Requirements</span></span>



| <span data-ttu-id="78d9e-215">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78d9e-215">Requirement</span></span> | <span data-ttu-id="78d9e-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="78d9e-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="78d9e-217">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d9e-217">Minimum supported client</span></span><br/> | <span data-ttu-id="78d9e-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78d9e-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="78d9e-219">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d9e-219">Minimum supported server</span></span><br/> | <span data-ttu-id="78d9e-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78d9e-220">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78d9e-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78d9e-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d9e-222">**espace de noms pragma**</span><span class="sxs-lookup"><span data-stu-id="78d9e-222">**pragma namespace**</span></span>](pragma-namespace.md)
</dt> <dt>

[<span data-ttu-id="78d9e-223">Compilation des fichiers MOF</span><span class="sxs-lookup"><span data-stu-id="78d9e-223">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="78d9e-224">Compilation des fichiers MOF localisés</span><span class="sxs-lookup"><span data-stu-id="78d9e-224">Compiling Localized MOF Files</span></span>](compiling-localized-mof-files.md)
</dt> <dt>

[<span data-ttu-id="78d9e-225">Inscription d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="78d9e-225">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="78d9e-226">**IMOFCompiler::CompileFile**</span><span class="sxs-lookup"><span data-stu-id="78d9e-226">**IMOFCompiler::CompileFile**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 


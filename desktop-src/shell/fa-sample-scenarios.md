---
description: Dans l’exemple suivant, une société de développement de logiciels hypothétique appelée Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Exemple d’association de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b92922bb907c4dd90b3e2bdc3d16c8e8b52e6a
ms.sourcegitcommit: b0d03febac36ff77cba034615b94ea103311398d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/19/2021
ms.locfileid: "107715787"
---
# <a name="file-association-example"></a><span data-ttu-id="7550a-103">Exemple d’association de fichiers</span><span class="sxs-lookup"><span data-stu-id="7550a-103">File Association Example</span></span>

<span data-ttu-id="7550a-104">Dans l’exemple suivant, une société de développement de logiciels hypothétique, appelée Litware, Inc., crée un nouveau lecteur audio appelé LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="7550a-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="7550a-105">Litware souhaite concevoir une association de fichiers entre LitwarePlayer et son type de fichier primaire, qui utilise un format audio nouvellement développé qui permet à un CD audio entier d’être stocké en moins de 10 kilo-octets de mémoire sans perte de qualité.</span><span class="sxs-lookup"><span data-stu-id="7550a-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7550a-106">Cette rubrique ne s’applique pas à Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7550a-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="7550a-107">Le mode de fonctionnement des associations de fichiers par défaut dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7550a-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="7550a-108">Pour plus d’informations, consultez la section sur les **modifications apportées à la façon dont Windows 10 gère les applications par défaut** dans [cette publication](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="7550a-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="7550a-109">Conception d’une nouvelle association de fichiers</span><span class="sxs-lookup"><span data-stu-id="7550a-109">Designing a New File Association</span></span>

<span data-ttu-id="7550a-110">La société doit effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7550a-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="7550a-111">**Déterminez si le nouveau type de fichier doit être considéré comme public ou privé.**</span><span class="sxs-lookup"><span data-stu-id="7550a-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="7550a-112">Ce nouveau type de fichier est un type de média.</span><span class="sxs-lookup"><span data-stu-id="7550a-112">This new file type is a media type.</span></span> <span data-ttu-id="7550a-113">Étant donné que les utilisateurs échangent des fichiers multimédias sur différentes plateformes et qu’il peut y avoir d’autres applications qui doivent lire le format LitwarePlayer, un type de fichier [public](fa-file-types.md) est le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="7550a-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="7550a-114">**Déterminez si ce type de fichier est déjà défini.**</span><span class="sxs-lookup"><span data-stu-id="7550a-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="7550a-115">Vérifiez la base de données MIME IANA (Internet Assigned Numbers Authority) et d’autres bases de données de type de fichier public sur Internet pour déterminer qu’aucun type de fichier comparable n’a été défini.</span><span class="sxs-lookup"><span data-stu-id="7550a-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="7550a-116">Étant donné qu’il s’agit d’un nouveau format de fichier, vous devez définir un nouveau type de fichier.</span><span class="sxs-lookup"><span data-stu-id="7550a-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="7550a-117">**Définissez une extension de nom de fichier pour le nouveau type de fichier.**</span><span class="sxs-lookup"><span data-stu-id="7550a-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="7550a-118">Les développeurs choisissent le `.opa-ltw-audio` , qui intègre leur abréviation de fournisseur et une indication sur le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="7550a-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="7550a-119">La recherche détermine que l’extension n’est pas utilisée par un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7550a-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="7550a-120">Conformément aux recommandations actuelles, aucune extension brève n’est définie.</span><span class="sxs-lookup"><span data-stu-id="7550a-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="7550a-121">**Définissez un type MIME pour le type de fichier et inscrivez-le auprès de l’IANA.**</span><span class="sxs-lookup"><span data-stu-id="7550a-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="7550a-122">Litware définit le nouveau type MIME comme *audio/LitwarePlayer. 1* et prépare une application de type MIME, conformément aux directives énoncées dans les numéros RFC 2045, 2046, 2047 et 2048.</span><span class="sxs-lookup"><span data-stu-id="7550a-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="7550a-123">Ils envoient ensuite l’application à l’IANA, qui ajoute le nouveau type de fichier à la base de données des types MIME inscrits.</span><span class="sxs-lookup"><span data-stu-id="7550a-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="7550a-124">**Déterminez si un ProgID existe pour le type de fichier.**</span><span class="sxs-lookup"><span data-stu-id="7550a-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="7550a-125">Étant donné qu’il s’agit d’un nouveau type de fichier, aucun [ProgID](fa-progids.md) n’existe pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7550a-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="7550a-126">Litware définit la conception d’un nouveau ProgID pour LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="7550a-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="7550a-127">Ils décident du nom convivial « LitwarePlayer Audio Player » (qui est stocké en tant que ressource dans le fichier LitwarePlayer.exe), et ils conçoivent une icône par défaut à utiliser pour les fichiers associés à LitwarePlayer (également stockés dans LitwarePlayer.exe).</span><span class="sxs-lookup"><span data-stu-id="7550a-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="7550a-128">Étant donné que LitwarePlayer est une nouvelle application, il s’agit d’un ProgID version 1.</span><span class="sxs-lookup"><span data-stu-id="7550a-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="7550a-129">**Enregistrez le ProgID.**</span><span class="sxs-lookup"><span data-stu-id="7550a-129">**Register the ProgID.**</span></span> <span data-ttu-id="7550a-130">Lorsque LitwarePlayer est installé, le programme d’installation crée l’entrée [ProgID](fa-progids.md) suivante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7550a-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    <span data-ttu-id="7550a-131">Dans la clé de commande, %1 est passé en tant que chemin d’accès au fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="7550a-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="7550a-132">**Enregistrez l’extension de nom de fichier pour le type de fichier.**</span><span class="sxs-lookup"><span data-stu-id="7550a-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="7550a-133">Lorsque LitwarePlayer est installé, le programme d’installation crée les entrées suivantes dans le registre pour son extension de type de fichier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7550a-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="7550a-134">Chaque fois qu’une association de fichier est créée ou modifiée, avertissez le système qu’une modification a été apportée en appelant [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), en spécifiant l' \_ événement ASSOCCHANGED SHCNE.</span><span class="sxs-lookup"><span data-stu-id="7550a-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="7550a-135">Si ce n’est pas le cas, l’interpréteur de commandes peut ne pas reconnaître les modifications apportées tant que le système n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="7550a-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="7550a-136">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7550a-136">Additional Resources</span></span>

-   [<span data-ttu-id="7550a-137">Présentation des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="7550a-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="7550a-138">Inscription d’un navigateur Internet ou d’un client de messagerie à l’aide du menu Démarrer de Windows</span><span class="sxs-lookup"><span data-stu-id="7550a-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="7550a-139">[Inscription d’une application dans un schéma d’URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7550a-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="7550a-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7550a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7550a-141">Meilleures pratiques pour les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="7550a-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="7550a-142">Instructions pour la gestion des applications par défaut dans Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="7550a-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="7550a-143">Programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="7550a-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="7550a-144">Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)</span><span class="sxs-lookup"><span data-stu-id="7550a-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 

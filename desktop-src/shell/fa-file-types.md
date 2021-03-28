---
description: Cette rubrique explique comment créer de nouveaux types de fichiers et comment associer votre application à votre type de fichier et à d’autres types de fichiers bien définis.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Types de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973243"
---
# <a name="file-types"></a><span data-ttu-id="b5bb6-103">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="b5bb6-103">File Types</span></span>

<span data-ttu-id="b5bb6-104">Cette rubrique explique comment créer de nouveaux types de fichiers et comment associer votre application à votre type de fichier et à d’autres types de fichiers bien définis.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-104">This topic explains how to create new file types and how to associate your app with your file type and other well-defined file types.</span></span> <span data-ttu-id="b5bb6-105">Les fichiers avec une extension de nom de fichier commun partagée (. doc,. html, etc.) sont du même *type*.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-105">Files with a shared common file name extension (.doc, .html, and so on) are of the same *type*.</span></span> <span data-ttu-id="b5bb6-106">Par exemple, si vous créez un éditeur de texte, vous pouvez utiliser le type de fichier. txt existant.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-106">For example, if you create a new text editor, then you can use the existing .txt file type.</span></span> <span data-ttu-id="b5bb6-107">Dans d’autres cas, vous devrez peut-être créer un nouveau type de fichier.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-107">In other cases, you might need to create a new file type.</span></span>

<span data-ttu-id="b5bb6-108">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="b5bb6-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b5bb6-109">Types de fichiers publics et privés</span><span class="sxs-lookup"><span data-stu-id="b5bb6-109">Public and Private File Types</span></span>](#public-and-private-file-types)
-   [<span data-ttu-id="b5bb6-110">Enregistrement d’un type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-110">Registering a File Type</span></span>](#registering-a-file-type)
    -   [<span data-ttu-id="b5bb6-111">Définition des sous-clés facultatives et des attributs d’extension de type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-111">Setting Optional Subkeys and File Type Extension Attributes</span></span>](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [<span data-ttu-id="b5bb6-112">Suppression des informations du registre lors de la désinstallation</span><span class="sxs-lookup"><span data-stu-id="b5bb6-112">Deleting Registry Information During Uninstallation</span></span>](#deleting-registry-information-during-uninstallation)
-   [<span data-ttu-id="b5bb6-113">Types de fichiers prenant en charge les métadonnées ouvertes</span><span class="sxs-lookup"><span data-stu-id="b5bb6-113">File Types That Support Open Metadata</span></span>](#file-types-that-support-open-metadata)
-   [<span data-ttu-id="b5bb6-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5bb6-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="b5bb6-115">Vous trouverez des informations supplémentaires dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5bb6-115">Additional information can be found on the following topics:</span></span>

-   [<span data-ttu-id="b5bb6-116">Comment choisir une extension de type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-116">How To Choose a File Type Extension</span></span>](how-to-choose-a-file-type-extension.md)
-   [<span data-ttu-id="b5bb6-117">Comment définir des attributs de type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-117">How To Define File Type Attributes</span></span>](./how-to-define-file-type-attributes.md)
-   [<span data-ttu-id="b5bb6-118">Comment inclure une application dans la boîte de dialogue Ouvrir avec</span><span class="sxs-lookup"><span data-stu-id="b5bb6-118">How To Include an Application on the Open with Dialog Box</span></span>](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [<span data-ttu-id="b5bb6-119">Comment exclure une application de la boîte de dialogue Ouvrir avec pour les types de fichiers non associés</span><span class="sxs-lookup"><span data-stu-id="b5bb6-119">How To Exclude an Application from the Open with Dialog Box for Unassociated File Types</span></span>](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a><span data-ttu-id="b5bb6-120">Types de fichiers publics et privés</span><span class="sxs-lookup"><span data-stu-id="b5bb6-120">Public and Private File Types</span></span>

<span data-ttu-id="b5bb6-121">Les types de fichiers publics sont également appelés types populaires ou contentieuses, car les applications concurrentes peuvent souhaiter être associées à ces types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-121">Public file types are also known as popular or contentious types because competing applications might want to be associated with these file types.</span></span> <span data-ttu-id="b5bb6-122">Les caractéristiques des types de fichiers publics sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5bb6-122">Characteristics of public file types include:</span></span>

-   <span data-ttu-id="b5bb6-123">Elles sont généralement définies par des corps de normes et/ou sont promues par leurs organisations de définition en tant que formats d’échange.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-123">They are typically defined by standards bodies, and/or are promoted by their defining organizations as interchange formats.</span></span>
-   <span data-ttu-id="b5bb6-124">Ils sont souvent échangés entre les ordinateurs et les utilisateurs à des fins diverses.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-124">They are often exchanged between computers and users for diverse purposes.</span></span>
-   <span data-ttu-id="b5bb6-125">Ils doivent être pris en charge sur de nombreuses plateformes différentes.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-125">They need to be supported on many different platforms.</span></span>
-   <span data-ttu-id="b5bb6-126">Les applications de plusieurs fournisseurs sont susceptibles de les gérer.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-126">Applications from multiple vendors are likely to handle them.</span></span>

<span data-ttu-id="b5bb6-127">Voici quelques exemples de types de fichiers considérés comme étant publics : types de fichiers image. png,. gif,. jpg et. bmp, et types audio. wav,. mp3 et. au.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-127">Some examples of file types that are considered public are the image file types .png, .gif, .jpg, and .bmp, and the audio types .wav, .mp3, and .au.</span></span>

<span data-ttu-id="b5bb6-128">Contrairement aux types de fichiers publics, les types de fichiers privés ou propriétaires ont généralement un format qui est implémenté et interprété par une seule application ou un seul fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-128">Unlike public file types, private or proprietary file types typically have a format that is implemented and understood by only one application or vendor.</span></span> <span data-ttu-id="b5bb6-129">Par conséquent, les types de fichiers privés ne sont généralement pas sujets aux conflits entre les applications.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-129">As a result, private file types are typically not prone to conflicts between applications.</span></span> <span data-ttu-id="b5bb6-130">Certains types de fichiers peuvent démarrer en tant que types de fichiers privés, mais deviennent par la suite des types de fichiers publics.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-130">Some file types can start as private file types but later become public file types.</span></span>

> [!Note]  
> <span data-ttu-id="b5bb6-131">Windows ne fait pas la distinction entre les types de fichiers publics et privés.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-131">Windows does not differentiate between public and private file types.</span></span> <span data-ttu-id="b5bb6-132">La distinction est pertinente uniquement pour prendre des décisions sur votre choix d’inscription de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-132">The distinction is relevant only in making decisions about your choice of file type registration.</span></span>

 

## <a name="registering-a-file-type"></a><span data-ttu-id="b5bb6-133">Enregistrement d’un type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-133">Registering a File Type</span></span>

<span data-ttu-id="b5bb6-134">Pour associer le type de fichier à une application existante, localisez le ProgID de l’application dans le registre.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-134">To associate the file type with an existing application, locate the application ProgID in the registry.</span></span> <span data-ttu-id="b5bb6-135">Pour associer le type de fichier à une nouvelle application, définissez un ProgID pour votre application.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-135">To associate the file type with a new application, define a ProgID for your application.</span></span> <span data-ttu-id="b5bb6-136">Pour plus d’informations sur la définition d’un nouveau ProgID, consultez [identificateurs par programmation](fa-progids.md).</span><span class="sxs-lookup"><span data-stu-id="b5bb6-136">For information about defining a new ProgID, see [Programmatic Identifiers](fa-progids.md).</span></span>

<span data-ttu-id="b5bb6-137">Les sous-clés d’extension de nom de fichier se présentent sous la forme générale suivante : ProgID d' *extension* = .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-137">File name extension subkeys have the following general form: *extension*=*ProgID*.</span></span> <span data-ttu-id="b5bb6-138">Les sous-clés d’extension de nom de fichier sont stockées dans la sous-arborescence **\_ \_ racine de classes HKEY** .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-138">File name extension subkeys are stored in the **HKEY\_CLASSES\_ROOT** subtree.</span></span>

<span data-ttu-id="b5bb6-139">Il est important d’inclure le point de début (.) lors de la création de sous-clés de type de fichier dans le registre.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-139">It is important to include the leading period (.) when creating file type subkeys in the registry.</span></span> <span data-ttu-id="b5bb6-140">Par exemple, si vous souhaitez qu’un type de fichier avec l’extension Short. MYP et l’extension long. MYP-file soit ouvert avec une application appelée MyProgram, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b5bb6-140">For example, if you want a file type with the short extension .myp and the long extension .myp-file to be opened with an application called MyProgram, use the following syntax:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

<span data-ttu-id="b5bb6-141">Comme illustré dans l’exemple précédent, si vous inscrivez également une extension de nom de fichier Short (. MYP), vous devez créer une sous-clé pour l’extension longue (fichier. MYP).</span><span class="sxs-lookup"><span data-stu-id="b5bb6-141">As demonstrated in the preceding example, if you also register a short file name extension (.myp), you should create a subkey for the long extension (.myp-file) as well.</span></span> <span data-ttu-id="b5bb6-142">Pour plus d’informations, consultez [gestionnaires de types de fichiers](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b5bb6-142">For more information, see [File Type Handlers](fa-file-extensions.md).</span></span>

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a><span data-ttu-id="b5bb6-143">Définition des sous-clés facultatives et des attributs d’extension de type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-143">Setting Optional Subkeys and File Type Extension Attributes</span></span>

<span data-ttu-id="b5bb6-144">Les entrées d’extension de type de fichier dans le registre ont plusieurs sous-clés et attributs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-144">File type extension entries in the registry have several optional subkeys and attributes.</span></span>

<span data-ttu-id="b5bb6-145">Les entrées d’extension de type de fichier utilisées par les associations de fichiers sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-145">The file type extension entries that are used by file associations are described in the following table.</span></span> <span data-ttu-id="b5bb6-146">Toutes les valeurs sont du type de **Registre \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-146">All values are of the **REG\_SZ** type.</span></span>



| <span data-ttu-id="b5bb6-147">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="b5bb6-147">Registry entry</span></span>  | <span data-ttu-id="b5bb6-148">Action</span><span class="sxs-lookup"><span data-stu-id="b5bb6-148">Action</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5bb6-149">Default</span><span class="sxs-lookup"><span data-stu-id="b5bb6-149">Default</span></span>         | <span data-ttu-id="b5bb6-150">Définissez la valeur par défaut de la sous-clé d’extension sur le ProgID auquel elle est liée.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-150">Set the default value of the extension subkey to the ProgID to which it is linked.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b5bb6-151">Type de contenu</span><span class="sxs-lookup"><span data-stu-id="b5bb6-151">Content Type</span></span>    | <span data-ttu-id="b5bb6-152">Définissez la valeur type de contenu sur le type de contenu MIME du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-152">Set the Content Type value to the file type's MIME content type.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b5bb6-153">OpenWithList</span><span class="sxs-lookup"><span data-stu-id="b5bb6-153">OpenWithList</span></span>    | <span data-ttu-id="b5bb6-154">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-154">Do not use.</span></span> <span data-ttu-id="b5bb6-155">Cette sous-clé contient une ou plusieurs sous-clés d’application pour les applications qui s’affichent dans l’entrée de la boîte de dialogue **Ouvrir avec** pour le type de fichier et est destinée uniquement aux applications. exe sur les systèmes d’exploitation antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-155">This subkey contains one or more application subkeys for applications that appear in the **Open with** dialog box entry for the file type and is intended only for .exe applications on operating systems prior to Windows XP.</span></span> <span data-ttu-id="b5bb6-156">Utilisez OpenWithProgIds à la place.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-156">Use OpenWithProgIds instead.</span></span>                                                            |
| <span data-ttu-id="b5bb6-157">OpenWithProgIds</span><span class="sxs-lookup"><span data-stu-id="b5bb6-157">OpenWithProgIds</span></span> | <span data-ttu-id="b5bb6-158">Cette sous-clé contient une liste d’autres ProgID pour ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-158">This subkey contains a list of alternate ProgIDs for this file type.</span></span> <span data-ttu-id="b5bb6-159">Les programmes pour ces ProgID s’affichent dans le menu **Ouvrir avec** et sont disponibles en tant qu’applications du Windows Store par défaut pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-159">The programs for these ProgIDs appear in the **Open with** menu and are available as default Windows Store apps for the file type.</span></span> <span data-ttu-id="b5bb6-160">Chaque fois qu’une application prend le contrôle de ce type de fichier en modifiant la valeur par défaut, elle doit également ajouter une entrée à cette liste.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-160">Whenever an application takes over this file type by changing the default value, it should also add an entry to this list.</span></span> |
| <span data-ttu-id="b5bb6-161">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="b5bb6-161">PerceivedType</span></span>   | <span data-ttu-id="b5bb6-162">Définissez la valeur PerceivedType sur le PerceivedType auquel le fichier appartient, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-162">Set the PerceivedType value to the PerceivedType to which the file belongs, if any.</span></span> <span data-ttu-id="b5bb6-163">Cette chaîne n’est pas utilisée par les versions de Windows antérieures à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-163">This string is not used by Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="b5bb6-164">Pour plus d’informations, consultez [types perçus et inscription des applications](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="b5bb6-164">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>                                                                           |



 

<span data-ttu-id="b5bb6-165">La forme générale d’une sous-clé d’extension de nom de fichier est la suivante.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-165">The general form of a file name extension subkey is as follows.</span></span> <span data-ttu-id="b5bb6-166">Tous les types d’entrée sont du type de **Registre \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-166">All entry types are of the **REG\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

<span data-ttu-id="b5bb6-167">Considérations importantes à propos des types de fichiers :</span><span class="sxs-lookup"><span data-stu-id="b5bb6-167">Important considerations about file types include:</span></span>

-   <span data-ttu-id="b5bb6-168">La sous-arborescence **\_ \_ racine de classes HKEY** est une vue formée en fusionnant les classes de logiciels de l' **\_ \_ utilisateur actuel HKEY** \\  \\  et les classes de logiciel **HKEY \_ local \_ machine** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="b5bb6-168">The **HKEY\_CLASSES\_ROOT** subtree is a view formed by merging **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** and **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes**</span></span>
-   <span data-ttu-id="b5bb6-169">En général, **la \_ \_ racine de classes HKEY** est destinée à être lue à partir de, mais n’est pas écrite dans.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-169">In general, **HKEY\_CLASSES\_ROOT** is intended to be read from but not written to.</span></span> <span data-ttu-id="b5bb6-170">Pour plus d’informations, consultez l’article [ \_ \_ racine des classes HKEY](../sysinfo/hkey-classes-root-key.md) .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-170">For more information, see the [HKEY\_CLASSES\_ROOT](../sysinfo/hkey-classes-root-key.md) article.</span></span>
-   <span data-ttu-id="b5bb6-171">Pour inscrire globalement un type de fichier sur un ordinateur particulier, créez une entrée pour le type de fichier dans la sous-clé de classes de logiciels de l' **\_ \_ ordinateur local HKEY** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-171">To register a file type globally on a particular computer, create an entry for the file type in the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="b5bb6-172">Pour que l’inscription d’un type de fichier soit visible pour l’utilisateur actuel uniquement, créez une entrée pour le type de fichier dans la sous-clé de classes de logiciels de la clé **HKEY \_ Current \_ User** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-172">To make a file type registration visible to the current user only, create an entry for the file type in the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="b5bb6-173">Une application peut fournir sa propre implémentation d’un verbe, tel que Open ou Play, comme indiqué dans l’exemple de Registre suivant.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-173">An application can provide its own implementation of a verb, such as open or play, as shown in the following registry example.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    <span data-ttu-id="b5bb6-174">Les sous-clés de la sous-clé de verbe incluent la ligne de commande et la méthode cible de déplacement : **Command** et **dropTarget**.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-174">Subkeys of the verb subkey include the command line and the drop target method: **command** and **DropTarget**.</span></span>

-   <span data-ttu-id="b5bb6-175">Lorsque vous créez ou modifiez une association de fichiers, il est important d’informer le système que vous avez apporté une modification.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-175">When you create or change a file association, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="b5bb6-176">Pour ce faire, appelez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) et spécifiez l’événement **\_ ASSOCCHANGED SHCNE** .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-176">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) and specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="b5bb6-177">Si vous n’appelez pas **SHChangeNotify**, la modification peut ne pas être reconnue tant que le système n’a pas été redémarré.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-177">If you do not call **SHChangeNotify**, the change may not be recognized until after the system is rebooted.</span></span>
-   <span data-ttu-id="b5bb6-178">Pour récupérer les informations de Registre relatives à une association de fichiers, utilisez l’interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="b5bb6-178">To retrieve registry information regarding a file association, use the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface.</span></span> <span data-ttu-id="b5bb6-179">Pour un scénario qui illustre cette procédure, consultez [exemple de scénario d’association de fichiers](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="b5bb6-179">For a scenario that illustrates this procedure, see [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

> [!Note]  
> <span data-ttu-id="b5bb6-180">Les sous-clés de registre des **applications** et des **chemins d’application** sont utilisées pour enregistrer et contrôler le comportement du système pour le compte des applications.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-180">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="b5bb6-181">Pour plus d’informations sur cette fonctionnalité, consultez [inscription de l’application](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="b5bb6-181">For more detailed information about this functionality, see [Application Registration](app-registration.md).</span></span>

 

### <a name="deleting-registry-information-during-uninstallation"></a><span data-ttu-id="b5bb6-182">Suppression des informations du registre lors de la désinstallation</span><span class="sxs-lookup"><span data-stu-id="b5bb6-182">Deleting Registry Information During Uninstallation</span></span>

<span data-ttu-id="b5bb6-183">Lors de la désinstallation d’une application, les ProgID et la plupart des autres informations de Registre associées à cette application doivent être supprimés dans le cadre de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-183">When uninstalling an application, the ProgIDs and most other registry information associated with that application should be deleted as part of the uninstallation.</span></span> <span data-ttu-id="b5bb6-184">Toutefois, les applications qui ont pris possession d’un type de fichier (en définissant la valeur par défaut de la sous-clé HKEY. extension **\_ \_ racine** du type de fichier \\  sur le ProgID de l’application) ne doivent pas tenter de supprimer cette valeur lors de la désinstallation de.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-184">However, applications that have taken ownership of a file type (by setting the Default value of the file type's **HKEY\_CLASSES\_ROOT**\\ *.extension* subkey to the ProgID of the application) should not attempt to remove that value when uninstalling.</span></span> <span data-ttu-id="b5bb6-185">Le fait de laisser les données en place pour la valeur par défaut évite de déterminer si une autre application a pris possession du type de fichier et a remplacé la valeur par défaut après l’installation de l’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-185">Leaving the data in place for the Default value avoids the difficulty of determining whether another application has taken ownership of the file type and overwritten the Default value after the original application was installed.</span></span> <span data-ttu-id="b5bb6-186">Windows respecte la valeur par défaut uniquement si le ProgID a trouvé un ProgID enregistré.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-186">Windows respects the Default value only if the ProgID found there is a registered ProgID.</span></span> <span data-ttu-id="b5bb6-187">Si le ProgID n’est pas inscrit, il est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-187">If the ProgID is unregistered, it is ignored.</span></span>

<span data-ttu-id="b5bb6-188">Notez que d’autres informations sur la propriété du type de fichier sont stockées dans la sous-arborescence de l' **\_ \_ utilisateur actuel HKEY** et sont également utilisées uniquement lorsque l’application à laquelle elle fait référence est inscrite.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-188">Note that other file-type ownership information is stored in the **HKEY\_CURRENT\_USER** subtree and also is used only when the application that it references is registered.</span></span> <span data-ttu-id="b5bb6-189">Par conséquent, il n’est pas nécessaire de supprimer ces données lors de la désinstallation d’une application.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-189">Therefore, this data does not need to be removed when uninstalling an application.</span></span>

<span data-ttu-id="b5bb6-190">À titre d’exemple, le code suivant montre l’état du Registre avant la désinstallation d’une application :</span><span class="sxs-lookup"><span data-stu-id="b5bb6-190">As an example, the following shows the state of the registry before an application is uninstalled:</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

<span data-ttu-id="b5bb6-191">L’exemple suivant montre l’état de ces mêmes entrées de registre après la désinstallation de l’application.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-191">The following shows the state of those same registry entries after the application has been uninstalled.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a><span data-ttu-id="b5bb6-192">Types de fichiers prenant en charge les métadonnées ouvertes</span><span class="sxs-lookup"><span data-stu-id="b5bb6-192">File Types That Support Open Metadata</span></span>

<span data-ttu-id="b5bb6-193">Dans Windows 7 et versions ultérieures, les types de fichiers suivants prennent en charge les métadonnées ouvertes.</span><span class="sxs-lookup"><span data-stu-id="b5bb6-193">In Windows 7 and later, the following file types support open metadata.</span></span>



| <span data-ttu-id="b5bb6-194">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-194">File type</span></span>                                                               | <span data-ttu-id="b5bb6-195">Extensions de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-195">File name extensions</span></span>                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b5bb6-196">Documents Office 2007</span><span class="sxs-lookup"><span data-stu-id="b5bb6-196">Office 2007 Documents</span></span>                                                   | <span data-ttu-id="b5bb6-197">. docx,. xlsx,. pptx</span><span class="sxs-lookup"><span data-stu-id="b5bb6-197">.docx, .xlsx, .pptx</span></span>                                           |
| <span data-ttu-id="b5bb6-198">Documents Office 97-2003</span><span class="sxs-lookup"><span data-stu-id="b5bb6-198">Office 97-2003 Documents</span></span>                                                | <span data-ttu-id="b5bb6-199">. doc,. xls,. ppt</span><span class="sxs-lookup"><span data-stu-id="b5bb6-199">.doc, .xls, .ppt</span></span>                                              |
| <span data-ttu-id="b5bb6-200">Recherche enregistrée</span><span class="sxs-lookup"><span data-stu-id="b5bb6-200">Saved Search</span></span>                                                            | <span data-ttu-id="b5bb6-201">. search-ms</span><span class="sxs-lookup"><span data-stu-id="b5bb6-201">.search-ms</span></span>                                                    |
| <span data-ttu-id="b5bb6-202">Formats basés sur Windows Media (conteneur ASF)</span><span class="sxs-lookup"><span data-stu-id="b5bb6-202">Windows Media-based formats (Advanced Streaming Format (ASF) container)</span></span> | <span data-ttu-id="b5bb6-203">. wmv,. WMA</span><span class="sxs-lookup"><span data-stu-id="b5bb6-203">.wmv, .wma</span></span>                                                    |
| <span data-ttu-id="b5bb6-204">MP4 (gestionnaire de propriétés)</span><span class="sxs-lookup"><span data-stu-id="b5bb6-204">MP4 (property handler)</span></span>                                                  | <span data-ttu-id="b5bb6-205">. MP4,. M4A,. m4v,. mp4v,. M4P,. M4B,. 3gp,. 3GPP,. 3GP2,. mov</span><span class="sxs-lookup"><span data-stu-id="b5bb6-205">.mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b5bb6-206">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5bb6-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5bb6-207">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="b5bb6-207">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="b5bb6-208">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="b5bb6-208">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="b5bb6-209">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="b5bb6-209">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="b5bb6-210">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="b5bb6-210">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="b5bb6-211">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="b5bb6-211">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="b5bb6-212">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="b5bb6-212">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="b5bb6-213">Types perçus</span><span class="sxs-lookup"><span data-stu-id="b5bb6-213">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="b5bb6-214">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="b5bb6-214">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 

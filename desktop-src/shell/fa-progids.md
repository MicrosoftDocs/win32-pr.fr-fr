---
description: L’interpréteur de commandes utilise une sous-clé de Registre ProgID (identificateur programmatique) pour associer un type de fichier à une application et contrôler le comportement de l’Association.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificateurs programmatiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991077"
---
# <a name="programmatic-identifiers"></a><span data-ttu-id="08612-103">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="08612-103">Programmatic Identifiers</span></span>

<span data-ttu-id="08612-104">L’interpréteur de commandes utilise une sous-clé de Registre ProgID (identificateur programmatique) pour associer un type de fichier à une application et contrôler le comportement de l’Association.</span><span class="sxs-lookup"><span data-stu-id="08612-104">The Shell uses a programmatic identifier (ProgID) registry subkey to associate a file type with an application, and to control the behavior of the association.</span></span> <span data-ttu-id="08612-105">Les entrées ProgID utilisées pour les associations de fichiers se trouvent sous la **\_ \_ racine de classes HKEY** dans le registre.</span><span class="sxs-lookup"><span data-stu-id="08612-105">The ProgID entries used for file associations are located under **HKEY\_CLASSES\_ROOT** in the registry.</span></span>

<span data-ttu-id="08612-106">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="08612-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="08612-107">Éléments d’identificateur programmatique utilisés par les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="08612-107">Programmatic Identifier Elements Used by File Associations</span></span>](#programmatic-identifier-elements-used-by-file-associations)
-   [<span data-ttu-id="08612-108">Utilisation d’identificateurs programmatiques avec version</span><span class="sxs-lookup"><span data-stu-id="08612-108">Using Versioned Programmatic Identifiers</span></span>](#using-versioned-programmatic-identifiers)
-   [<span data-ttu-id="08612-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08612-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="08612-110">Pour plus d’informations, consultez [comment inscrire un type de fichier pour une nouvelle application](how-to-register-a-file-type-for-a-new-application.md)</span><span class="sxs-lookup"><span data-stu-id="08612-110">For additional information, read [How To Register a File Type for a New Application](how-to-register-a-file-type-for-a-new-application.md)</span></span>

## <a name="programmatic-identifier-elements-used-by-file-associations"></a><span data-ttu-id="08612-111">Éléments d’identificateur programmatique utilisés par les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="08612-111">Programmatic Identifier Elements Used by File Associations</span></span>

<span data-ttu-id="08612-112">Le format approprié d’un nom de clé ProgID est \[ *Vendor ou application* \] . \[ *Composant* \] . \[  \] , Séparées par des points et sans espaces, comme dans Word.Document. 6.</span><span class="sxs-lookup"><span data-stu-id="08612-112">The proper format of a ProgID key name is \[*Vendor or Application*\].\[*Component*\].\[*Version*\], separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="08612-113">La partie *version* est facultative, mais vivement recommandée.</span><span class="sxs-lookup"><span data-stu-id="08612-113">The *Version* portion is optional but strongly recommended.</span></span> <span data-ttu-id="08612-114">Pour plus d’informations, consultez [utilisation d’identificateurs programmatiques avec version](#using-versioned-programmatic-identifiers).</span><span class="sxs-lookup"><span data-stu-id="08612-114">For more information, see [Using Versioned Programmatic Identifiers](#using-versioned-programmatic-identifiers).</span></span>

<span data-ttu-id="08612-115">Une sous-clé ProgID doit inclure les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="08612-115">A ProgID subkey should include the following elements.</span></span> <span data-ttu-id="08612-116">Notez que certaines données de chaîne de cette clé requièrent une mise en forme spécifique.</span><span class="sxs-lookup"><span data-stu-id="08612-116">Note that some string data in this key requires specific formatting.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08612-117">Élément</span><span class="sxs-lookup"><span data-stu-id="08612-117">Element</span></span></th>
<th><span data-ttu-id="08612-118">Description</span><span class="sxs-lookup"><span data-stu-id="08612-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08612-119"><strong>Valeurs</strong></span><span class="sxs-lookup"><span data-stu-id="08612-119"><strong>(Default)</strong></span></span></td>
<td><span data-ttu-id="08612-120">Définissez l’entrée par défaut de la sous-clé ProgID sur un nom convivial pour ce ProgID, pouvant être affiché à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="08612-120">Set the default entry of the ProgID subkey to a friendly name for that ProgID, suitable to display to the user.</span></span> <span data-ttu-id="08612-121">L’utilisation de cette entrée pour contenir le nom convivial est déconseillée par l’entrée FriendlyTypeName sur les systèmes exécutant Windows 2000 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="08612-121">The use of this entry to hold the friendly name is deprecated by the FriendlyTypeName entry on systems running Windows 2000 or later.</span></span> <span data-ttu-id="08612-122">Toutefois, vous devez définir cette valeur pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="08612-122">However, you should set this value for backward compatibility.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08612-123"><strong>AllowSilentDefaultTakeOver</strong> (introduit dans Windows 8)</span><span class="sxs-lookup"><span data-stu-id="08612-123"><strong>AllowSilentDefaultTakeOver</strong> (introduced in Windows 8)</span></span></td>
<td><span data-ttu-id="08612-124">Définissez cette entrée facultative pour signaler que Windows doit ignorer ce ProgID lors de la détermination d’un gestionnaire par défaut pour un type de fichier public.</span><span class="sxs-lookup"><span data-stu-id="08612-124">Set this optional entry to signal that Windows should ignore this ProgID when determining a default handler for a public file type.</span></span> <span data-ttu-id="08612-125">Que cette valeur soit définie ou non, l’identificateur de programme (ProgID) continue à s’afficher dans le menu contextuel et la boîte de dialogue OpenWith.</span><span class="sxs-lookup"><span data-stu-id="08612-125">Regardless of whether this value is set, the ProgID continues to appear in the OpenWith shortcut menu and dialog.</span></span> <span data-ttu-id="08612-126">Il s’agit d’une valeur REG_NONE.</span><span class="sxs-lookup"><span data-stu-id="08612-126">This is a REG_NONE value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08612-127"><strong>AppUserModelID</strong> (introduite dans Windows 7)</span><span class="sxs-lookup"><span data-stu-id="08612-127"><strong>AppUserModelID</strong> (introduced in Windows 7)</span></span></td>
<td><span data-ttu-id="08612-128">Définissez cette entrée facultative sur l’ID de modèle utilisateur d’application explicite de l’application (AppUserModelID) si l’application utilise une valeur AppUserModelID explicite et utilise les listes de raccourcis <strong>récentes</strong> ou <strong>fréquentes</strong> générées par le système, ou fournit une liste de raccourcis personnalisée.</span><span class="sxs-lookup"><span data-stu-id="08612-128">Set this optional entry to the application's explicit Application User Model ID (AppUserModelID) if the application uses an explicit AppUserModelID and uses either the system's automatically generated <strong>Recent</strong> or <strong>Frequent</strong> Jump Lists or provides a custom Jump List.</span></span> <span data-ttu-id="08612-129">Si une application utilise un AppUserModelID explicite et ne définit pas cette valeur, les éléments ne s’affichent pas dans les listes de raccourcis de cette application.</span><span class="sxs-lookup"><span data-stu-id="08612-129">If an application uses an explicit AppUserModelID and does not set this value, items will not appear in that application's Jump Lists.</span></span> <span data-ttu-id="08612-130">Il s’agit d’une chaîne de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="08612-130">This is a REG_SZ string.</span></span> <span data-ttu-id="08612-131">Pour plus d’informations, consultez <a href="appids.md">ID de modèle d’utilisateur d’application (AppUserModelIDs)</a>.</span><span class="sxs-lookup"><span data-stu-id="08612-131">For more information, see <a href="appids.md">Application User Model IDs (AppUserModelIDs)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08612-132"><strong>EditFlags</strong></span><span class="sxs-lookup"><span data-stu-id="08612-132"><strong>EditFlags</strong></span></span></td>
<td><span data-ttu-id="08612-133">Définissez cette entrée facultative à l’aide d’indicateurs à partir de l’énumération <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08612-133">Set this optional entry using flags from the <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> enumeration.</span></span> <span data-ttu-id="08612-134">L’entrée indicateurs contrôle certains aspects de la gestion de l’interpréteur de commandes des types de fichiers liés à ce ProgID.</span><span class="sxs-lookup"><span data-stu-id="08612-134">The EditFlags entry controls some aspects of the Shell's handling of the file types linked to this ProgID.</span></span> <span data-ttu-id="08612-135">Vous pouvez également utiliser l’entrée indicateurs pour limiter la capacité de l’utilisateur à modifier certains aspects de ces types de fichiers à l’aide de la feuille de propriétés d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="08612-135">You can also use the EditFlags entry to limit how much the user can modify certain aspects of these file types using a file's property sheet.</span></span> <span data-ttu-id="08612-136">Les valeurs <strong>FILETYPEATTRIBUTEFLAGS</strong> utilisées pour indicateurs sont des valeurs binaires conçues pour vous permettre de combiner plusieurs attributs en une seule valeur dans une opération or au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="08612-136">The <strong>FILETYPEATTRIBUTEFLAGS</strong> values used for EditFlags are binary values designed so that you can combine multiple attributes into a single value in a bitwise OR operation.</span></span> <span data-ttu-id="08612-137">Il s’agit d’une valeur REG_DWORD ou REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="08612-137">This is a REG_DWORD or REG_BINARY value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08612-138"><strong>FriendlyTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="08612-138"><strong>FriendlyTypeName</strong></span></span></td>
<td><span data-ttu-id="08612-139">Définissez cette entrée sur un nom convivial pour le ProgID, pouvant être affiché à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="08612-139">Set this entry to a friendly name for the ProgID, suitable to display to the user.</span></span> <span data-ttu-id="08612-140">Pour des fins de cohérence, cette chaîne doit contenir les mêmes données que l’entrée par défaut pour cette clé ProgID.</span><span class="sxs-lookup"><span data-stu-id="08612-140">For consistency, this string should contain the same data as the Default entry for this ProgID key.</span></span> <span data-ttu-id="08612-141">Cette entrée peut être une REG_SZ ou REG_EXPAND_SZ chaîne, mais elle doit être formatée comme une chaîne indirecte (nom de fichier complet et valeur de ressource précédée du symbole @), par exemple <em>@% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="08612-141">This entry can be either a REG_SZ or REG_EXPAND_SZ string, but it must be formatted as an indirect string (a fully qualified file name and resource value preceded by the @ symbol), for instance <em>@%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08612-142"><strong>InfoTip</strong></span><span class="sxs-lookup"><span data-stu-id="08612-142"><strong>InfoTip</strong></span></span></td>
<td><span data-ttu-id="08612-143">Définissez cette entrée sur un bref message d’aide que l’interpréteur de commandes affiche pour ce ProgID.</span><span class="sxs-lookup"><span data-stu-id="08612-143">Set this entry to a brief help message that the Shell displays for this ProgID.</span></span> <span data-ttu-id="08612-144">L’entrée info-bulle s’affiche dans une boîte de dialogue de pointage avec la souris.</span><span class="sxs-lookup"><span data-stu-id="08612-144">The InfoTip entry displays in a mouse-over dialog box.</span></span> <span data-ttu-id="08612-145">Cette valeur peut être une REG_SZ ou REG_EXPAND_SZ chaîne, mais comme FriendlyTypeName, elle doit être mise en forme en tant que chaîne indirecte.</span><span class="sxs-lookup"><span data-stu-id="08612-145">This value can be either a REG_SZ or REG_EXPAND_SZ string but, like FriendlyTypeName, it must be formatted as an indirect string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08612-146"><strong>CurVer</strong></span><span class="sxs-lookup"><span data-stu-id="08612-146"><strong>CurVer</strong></span></span></td>
<td><span data-ttu-id="08612-147">Définissez l’entrée (par défaut) de cette sous-clé sur la version la plus récente de ce ProgID.</span><span class="sxs-lookup"><span data-stu-id="08612-147">Set the (Default) entry of this subkey to the most current version of this ProgID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08612-148">À moins que vous n’ayez des versions d’application côte à côte, autrement dit, si plusieurs versions sont installées sur le même système, vous devez éviter d’utiliser <strong>Curver</strong>.</span><span class="sxs-lookup"><span data-stu-id="08612-148">Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08612-149"><strong>DefaultIcon</strong>.</span><span class="sxs-lookup"><span data-stu-id="08612-149"><strong>DefaultIcon</strong>.</span></span></td>
<td><span data-ttu-id="08612-150">Définissez l’entrée (par défaut) de cette sous-clé sur l’icône par défaut que vous souhaitez afficher pour les types de fichiers associés à ce ProgID.</span><span class="sxs-lookup"><span data-stu-id="08612-150">Set the (Default) entry of this subkey to the default icon that you want to display for file types associated with this ProgID.</span></span> <span data-ttu-id="08612-151">Cette valeur peut être une REG_SZ ou REG_EXPAND_SZ chaîne, mais elle doit être fournie sous la forme d’un nom de fichier complet avec sa valeur de ressource de surveillance, par exemple <em>% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="08612-151">This value can be either a REG_SZ or REG_EXPAND_SZ string, but it must be provided as a fully qualified file name with its attendant resource value, for instance <em>%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="08612-152">L’exemple de clé de Registre suivant illustre un nœud de clé ProgID d’association de fichiers :</span><span class="sxs-lookup"><span data-stu-id="08612-152">The following registry key example illustrates a file association ProgID key node:</span></span>

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a><span data-ttu-id="08612-153">Utilisation d’identificateurs programmatiques avec version</span><span class="sxs-lookup"><span data-stu-id="08612-153">Using Versioned Programmatic Identifiers</span></span>

<span data-ttu-id="08612-154">Un ProgID avec version est un ProgID dont la version est indiquée dans son nom.</span><span class="sxs-lookup"><span data-stu-id="08612-154">A versioned ProgID is one whose version is indicated in its name.</span></span> <span data-ttu-id="08612-155">Pour ce faire, vous devez ajouter un point et le numéro de version au nom.</span><span class="sxs-lookup"><span data-stu-id="08612-155">You typically do this by adding a period and the version number to the name.</span></span> <span data-ttu-id="08612-156">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="08612-156">For example:</span></span>

-   <span data-ttu-id="08612-157">Word.Document. 6</span><span class="sxs-lookup"><span data-stu-id="08612-157">Word.Document.6</span></span>
-   <span data-ttu-id="08612-158">Word.Document. 8</span><span class="sxs-lookup"><span data-stu-id="08612-158">Word.Document.8</span></span>

<span data-ttu-id="08612-159">Il s’agit de ProgID avec version, respectivement les versions 6 et 8.</span><span class="sxs-lookup"><span data-stu-id="08612-159">These are versioned ProgIDs, with versions 6 and 8 respectively.</span></span> <span data-ttu-id="08612-160">Si vous disposez d’une application côte à côte, autrement dit, une application qui prend en charge plusieurs versions de votre application installées en même temps, utilisez des ProgID indépendants de la version et de CurVer.</span><span class="sxs-lookup"><span data-stu-id="08612-160">If you have a side-by-side application, that is, one that supports multiple versions of your application installed at the same time, then use CurVer and Version Independent ProgIDs.</span></span> <span data-ttu-id="08612-161">Dans le cas contraire, vous devez éviter les ProgID indépendants de la version et de CurVer, car ils risquent d’être inefficaces.</span><span class="sxs-lookup"><span data-stu-id="08612-161">Otherwise, CurVer and Version Independent ProgIDs should be avoided because they will lead to inefficiency.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08612-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08612-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08612-163">Comment inscrire un type de fichier pour une nouvelle application</span><span class="sxs-lookup"><span data-stu-id="08612-163">How To Register a File Type for a New Application</span></span>](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[<span data-ttu-id="08612-164">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="08612-164">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="08612-165">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="08612-165">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="08612-166">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="08612-166">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="08612-167">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="08612-167">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="08612-168">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="08612-168">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="08612-169">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="08612-169">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="08612-170">Types perçus</span><span class="sxs-lookup"><span data-stu-id="08612-170">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="08612-171">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="08612-171">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 





---
description: La table de classe contient des informations relatives au serveur COM qui doivent être générées dans le cadre de la publication du produit. Chaque ligne peut générer un ensemble de clés et de valeurs de registre. Les informations ProgId associées sont incluses dans ce tableau.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Table de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520525"
---
# <a name="class-table"></a><span data-ttu-id="bea14-105">Table de classe</span><span class="sxs-lookup"><span data-stu-id="bea14-105">Class Table</span></span>

<span data-ttu-id="bea14-106">La table de classe contient des informations relatives au serveur COM qui doivent être générées dans le cadre de la publication du produit.</span><span class="sxs-lookup"><span data-stu-id="bea14-106">The Class table contains COM server-related information that must be generated as a part of the product advertisement.</span></span> <span data-ttu-id="bea14-107">Chaque ligne peut générer un ensemble de clés et de valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="bea14-107">Each row may generate a set of registry keys and values.</span></span> <span data-ttu-id="bea14-108">Les informations ProgId associées sont incluses dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="bea14-108">The associated ProgId information is included in this table.</span></span>

<span data-ttu-id="bea14-109">La table de classe contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bea14-109">The Class table has the following columns.</span></span>



| <span data-ttu-id="bea14-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="bea14-110">Column</span></span>           | <span data-ttu-id="bea14-111">Type</span><span class="sxs-lookup"><span data-stu-id="bea14-111">Type</span></span>                         | <span data-ttu-id="bea14-112">Clé</span><span class="sxs-lookup"><span data-stu-id="bea14-112">Key</span></span> | <span data-ttu-id="bea14-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="bea14-113">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="bea14-114">CLSID</span><span class="sxs-lookup"><span data-stu-id="bea14-114">CLSID</span></span>            | [<span data-ttu-id="bea14-115">GUID</span><span class="sxs-lookup"><span data-stu-id="bea14-115">GUID</span></span>](guid.md)             | <span data-ttu-id="bea14-116">O</span><span class="sxs-lookup"><span data-stu-id="bea14-116">Y</span></span>   | <span data-ttu-id="bea14-117">N</span><span class="sxs-lookup"><span data-stu-id="bea14-117">N</span></span>        |
| <span data-ttu-id="bea14-118">Context</span><span class="sxs-lookup"><span data-stu-id="bea14-118">Context</span></span>          | [<span data-ttu-id="bea14-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="bea14-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="bea14-120">O</span><span class="sxs-lookup"><span data-stu-id="bea14-120">Y</span></span>   | <span data-ttu-id="bea14-121">N</span><span class="sxs-lookup"><span data-stu-id="bea14-121">N</span></span>        |
| <span data-ttu-id="bea14-122">-\_</span><span class="sxs-lookup"><span data-stu-id="bea14-122">Component\_</span></span>      | [<span data-ttu-id="bea14-123">Identificateur</span><span class="sxs-lookup"><span data-stu-id="bea14-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="bea14-124">O</span><span class="sxs-lookup"><span data-stu-id="bea14-124">Y</span></span>   | <span data-ttu-id="bea14-125">N</span><span class="sxs-lookup"><span data-stu-id="bea14-125">N</span></span>        |
| <span data-ttu-id="bea14-126">ProgId \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="bea14-126">ProgId\_Default</span></span>  | [<span data-ttu-id="bea14-127">Text</span><span class="sxs-lookup"><span data-stu-id="bea14-127">Text</span></span>](text.md)             | <span data-ttu-id="bea14-128">N</span><span class="sxs-lookup"><span data-stu-id="bea14-128">N</span></span>   | <span data-ttu-id="bea14-129">O</span><span class="sxs-lookup"><span data-stu-id="bea14-129">Y</span></span>        |
| <span data-ttu-id="bea14-130">Description</span><span class="sxs-lookup"><span data-stu-id="bea14-130">Description</span></span>      | [<span data-ttu-id="bea14-131">Text</span><span class="sxs-lookup"><span data-stu-id="bea14-131">Text</span></span>](text.md)             | <span data-ttu-id="bea14-132">N</span><span class="sxs-lookup"><span data-stu-id="bea14-132">N</span></span>   | <span data-ttu-id="bea14-133">O</span><span class="sxs-lookup"><span data-stu-id="bea14-133">Y</span></span>        |
| <span data-ttu-id="bea14-134">AppId\_</span><span class="sxs-lookup"><span data-stu-id="bea14-134">AppId\_</span></span>          | [<span data-ttu-id="bea14-135">GUID</span><span class="sxs-lookup"><span data-stu-id="bea14-135">GUID</span></span>](guid.md)             | <span data-ttu-id="bea14-136">N</span><span class="sxs-lookup"><span data-stu-id="bea14-136">N</span></span>   | <span data-ttu-id="bea14-137">O</span><span class="sxs-lookup"><span data-stu-id="bea14-137">Y</span></span>        |
| <span data-ttu-id="bea14-138">FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="bea14-138">FileTypeMask</span></span>     | [<span data-ttu-id="bea14-139">Text</span><span class="sxs-lookup"><span data-stu-id="bea14-139">Text</span></span>](text.md)             | <span data-ttu-id="bea14-140">N</span><span class="sxs-lookup"><span data-stu-id="bea14-140">N</span></span>   | <span data-ttu-id="bea14-141">O</span><span class="sxs-lookup"><span data-stu-id="bea14-141">Y</span></span>        |
| <span data-ttu-id="bea14-142">Icône\_</span><span class="sxs-lookup"><span data-stu-id="bea14-142">Icon\_</span></span>           | [<span data-ttu-id="bea14-143">Identificateur</span><span class="sxs-lookup"><span data-stu-id="bea14-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="bea14-144">N</span><span class="sxs-lookup"><span data-stu-id="bea14-144">N</span></span>   | <span data-ttu-id="bea14-145">O</span><span class="sxs-lookup"><span data-stu-id="bea14-145">Y</span></span>        |
| <span data-ttu-id="bea14-146">IndexIcône</span><span class="sxs-lookup"><span data-stu-id="bea14-146">IconIndex</span></span>        | [<span data-ttu-id="bea14-147">Integer</span><span class="sxs-lookup"><span data-stu-id="bea14-147">Integer</span></span>](integer.md)       | <span data-ttu-id="bea14-148">N</span><span class="sxs-lookup"><span data-stu-id="bea14-148">N</span></span>   | <span data-ttu-id="bea14-149">O</span><span class="sxs-lookup"><span data-stu-id="bea14-149">Y</span></span>        |
| <span data-ttu-id="bea14-150">DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="bea14-150">DefInprocHandler</span></span> | [<span data-ttu-id="bea14-151">Nom du fichier</span><span class="sxs-lookup"><span data-stu-id="bea14-151">Filename</span></span>](filename.md)     | <span data-ttu-id="bea14-152">N</span><span class="sxs-lookup"><span data-stu-id="bea14-152">N</span></span>   | <span data-ttu-id="bea14-153">O</span><span class="sxs-lookup"><span data-stu-id="bea14-153">Y</span></span>        |
| <span data-ttu-id="bea14-154">Argument</span><span class="sxs-lookup"><span data-stu-id="bea14-154">Argument</span></span>         | [<span data-ttu-id="bea14-155">Correct</span><span class="sxs-lookup"><span data-stu-id="bea14-155">Formatted</span></span>](formatted.md)   | <span data-ttu-id="bea14-156">N</span><span class="sxs-lookup"><span data-stu-id="bea14-156">N</span></span>   | <span data-ttu-id="bea14-157">O</span><span class="sxs-lookup"><span data-stu-id="bea14-157">Y</span></span>        |
| <span data-ttu-id="bea14-158">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="bea14-158">Feature\_</span></span>        | [<span data-ttu-id="bea14-159">Identificateur</span><span class="sxs-lookup"><span data-stu-id="bea14-159">Identifier</span></span>](identifier.md) | <span data-ttu-id="bea14-160">N</span><span class="sxs-lookup"><span data-stu-id="bea14-160">N</span></span>   | <span data-ttu-id="bea14-161">N</span><span class="sxs-lookup"><span data-stu-id="bea14-161">N</span></span>        |
| <span data-ttu-id="bea14-162">Attributs</span><span class="sxs-lookup"><span data-stu-id="bea14-162">Attributes</span></span>       | [<span data-ttu-id="bea14-163">Integer</span><span class="sxs-lookup"><span data-stu-id="bea14-163">Integer</span></span>](integer.md)       | <span data-ttu-id="bea14-164">N</span><span class="sxs-lookup"><span data-stu-id="bea14-164">N</span></span>   | <span data-ttu-id="bea14-165">O</span><span class="sxs-lookup"><span data-stu-id="bea14-165">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="bea14-166">Informations sur les colonnes</span><span class="sxs-lookup"><span data-stu-id="bea14-166">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="bea14-167"><span id="CLSID"></span><span id="clsid"></span>IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="bea14-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="bea14-168">Identificateur de classe (ID) d’un serveur COM.</span><span class="sxs-lookup"><span data-stu-id="bea14-168">The Class identifier (ID) of a COM server.</span></span>

</dd> <dt>

<span data-ttu-id="bea14-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contexte</span><span class="sxs-lookup"><span data-stu-id="bea14-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Context</span></span>
</dt> <dd>

<span data-ttu-id="bea14-170">Contexte de serveur pour ce serveur.</span><span class="sxs-lookup"><span data-stu-id="bea14-170">The server context for this server.</span></span> <span data-ttu-id="bea14-171">Entrez l’une des valeurs suivantes pour la clé CLSID.</span><span class="sxs-lookup"><span data-stu-id="bea14-171">Enter one of the following values for the CLSID Key.</span></span>



| <span data-ttu-id="bea14-172">CLÉ CLSID</span><span class="sxs-lookup"><span data-stu-id="bea14-172">CLSID KEY</span></span>                             | <span data-ttu-id="bea14-173">Description</span><span class="sxs-lookup"><span data-stu-id="bea14-173">Description</span></span>                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="bea14-174">LocalServer</span><span class="sxs-lookup"><span data-stu-id="bea14-174">LocalServer</span></span>](../com/localserver.md)       | <span data-ttu-id="bea14-175">Spécifie le chemin d’accès complet à une application serveur locale 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bea14-175">Specifies the full path to a 16-bit local server application.</span></span>             |
| [<span data-ttu-id="bea14-176">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="bea14-176">LocalServer32</span></span>](../com/localserver32.md)   | <span data-ttu-id="bea14-177">Spécifie le chemin d’accès complet à une application serveur locale 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bea14-177">Specifies the full path to a 32-bit local server application.</span></span>             |
| [<span data-ttu-id="bea14-178">InprocServer</span><span class="sxs-lookup"><span data-stu-id="bea14-178">InprocServer</span></span>](../com/inprocserver.md)     | <span data-ttu-id="bea14-179">Spécifie le chemin d’accès à une DLL de serveur in-process.</span><span class="sxs-lookup"><span data-stu-id="bea14-179">Specifies the path to an in-process server DLL.</span></span>                           |
| [<span data-ttu-id="bea14-180">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="bea14-180">InprocServer32</span></span>](../com/inprocserver32.md) | <span data-ttu-id="bea14-181">Spécifie le chemin d’accès à un serveur in-process 32 bits et le modèle de thread.</span><span class="sxs-lookup"><span data-stu-id="bea14-181">Specifies the path to a 32-bit in-process server and the threading model.</span></span> |



 

</dd> <dt>

<span data-ttu-id="bea14-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="bea14-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="bea14-183">Clé externe dans la [table de composants](component-table.md) spécifiant le composant dont le fichier de clé fournit le serveur com.</span><span class="sxs-lookup"><span data-stu-id="bea14-183">External key into the [Component table](component-table.md) specifying the component whose key file provides the COM server.</span></span>

</dd> <dt>

<span data-ttu-id="bea14-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="bea14-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId\_Default</span></span>
</dt> <dd>

<span data-ttu-id="bea14-185">ID de programme par défaut associé à cet ID de classe.</span><span class="sxs-lookup"><span data-stu-id="bea14-185">The default Program ID associated with this Class ID.</span></span> <span data-ttu-id="bea14-186">Cette colonne est une clé étrangère dans la [table ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="bea14-186">This column is a foreign key into the [ProgID table](progid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="bea14-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="bea14-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="bea14-188">Description localisée associée à l’ID de classe et à l’ID de programme.</span><span class="sxs-lookup"><span data-stu-id="bea14-188">Localized description associated with the Class ID and Program ID.</span></span>

</dd> <dt>

<span data-ttu-id="bea14-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span><span class="sxs-lookup"><span data-stu-id="bea14-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span></span>
</dt> <dd>

<span data-ttu-id="bea14-190">ID d’application contenant les informations DCOM pour l’application associée ( [GUID](guid.md)de chaîne).</span><span class="sxs-lookup"><span data-stu-id="bea14-190">Application ID containing DCOM information for the associated application (string [GUID](guid.md)).</span></span> <span data-ttu-id="bea14-191">Cette colonne est une clé étrangère dans la [table AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="bea14-191">This column is a foreign key into the [AppId table](appid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="bea14-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="bea14-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span></span>
</dt> <dd>

<span data-ttu-id="bea14-193">Contient des informations pour la clé HKCR (ce CLSID).</span><span class="sxs-lookup"><span data-stu-id="bea14-193">Contains information for the HKCR (this CLSID) key.</span></span>

<span data-ttu-id="bea14-194">Si plusieurs modèles existent, ils doivent être délimités par un point-virgule et les sous-clés numériques sont générées : 0, 1, 2... Pour plus d’informations sur cette fonctionnalité, consultez [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span><span class="sxs-lookup"><span data-stu-id="bea14-194">If multiple patterns exist, they must be delimited by a semicolon, and numeric subkeys are generated: 0, 1, 2... For more information about this functionality, see [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span></span>

</dd> <dt>

<span data-ttu-id="bea14-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Située\_</span><span class="sxs-lookup"><span data-stu-id="bea14-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="bea14-196">Fichier fournissant l’icône associée à ce CLSID.</span><span class="sxs-lookup"><span data-stu-id="bea14-196">The file providing the icon associated with this CLSID.</span></span> <span data-ttu-id="bea14-197">Le programme d’installation écrit l’entrée dans cette colonne sous la clé DefaultIcon associée au ProgId.</span><span class="sxs-lookup"><span data-stu-id="bea14-197">The installer writes the entry in this column under the DefaultIcon key associated with the ProgId.</span></span> <span data-ttu-id="bea14-198">Si la valeur n’est pas null, la colonne est une clé étrangère dans la [table d’icônes](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="bea14-198">If it is not null, the column is a foreign key into the [Icon table](icon-table.md).</span></span> <span data-ttu-id="bea14-199">Si la valeur est null, le serveur COM fournit la ressource icône.</span><span class="sxs-lookup"><span data-stu-id="bea14-199">If it is null, the COM server provides the icon resource.</span></span> <span data-ttu-id="bea14-200">Les associations et les raccourcis de fichiers publiés requièrent une valeur non null dans cette colonne pour s’afficher correctement.</span><span class="sxs-lookup"><span data-stu-id="bea14-200">Advertised file associations and shortcuts require a non-null value in this column to display properly.</span></span>

</dd> <dt>

<span data-ttu-id="bea14-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IndexIcône</span><span class="sxs-lookup"><span data-stu-id="bea14-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="bea14-202">Index d’icône dans le fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="bea14-202">Icon index into the icon file.</span></span> <span data-ttu-id="bea14-203">Peut être Null.</span><span class="sxs-lookup"><span data-stu-id="bea14-203">This can be null.</span></span>

<span data-ttu-id="bea14-204">Nombres non négatifs uniquement.</span><span class="sxs-lookup"><span data-stu-id="bea14-204">Non-negative numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="bea14-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="bea14-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span></span>
</dt> <dd>

<span data-ttu-id="bea14-206">Ce champ spécifie le gestionnaire in-process par défaut pour le contexte de serveur spécifié dans le champ de contexte.</span><span class="sxs-lookup"><span data-stu-id="bea14-206">This field specifies the default in-process handler for the server context specified in the Context field.</span></span>

<span data-ttu-id="bea14-207">Ce champ doit avoir la valeur null si une clé de CLSID InprocServer ou InprocServer apparaît dans le champ de contexte.</span><span class="sxs-lookup"><span data-stu-id="bea14-207">This field must be Null if an InprocServer or InprocServer CLSID key appears in the Context field.</span></span>

<span data-ttu-id="bea14-208">Si une clé de CLSID LocalServer ou LocalServer32 apparaît dans le champ de contexte, la valeur du champ DefInprocHandler identifie le gestionnaire in-process par défaut.</span><span class="sxs-lookup"><span data-stu-id="bea14-208">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the value in the DefInprocHandler field identifies the default in-process handler.</span></span>



| <span data-ttu-id="bea14-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="bea14-209">Value</span></span>                | <span data-ttu-id="bea14-210">Description</span><span class="sxs-lookup"><span data-stu-id="bea14-210">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bea14-211">valeur non numérique</span><span class="sxs-lookup"><span data-stu-id="bea14-211">non-numeric value</span></span>    | <span data-ttu-id="bea14-212">Le programme d’installation traite une valeur non numérique dans le champ DefInprocHandler comme un fichier système servant de gestionnaire in-process 32 bits spécifié par la clé InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="bea14-212">The installer treats a non-numeric value in the DefInprocHandler field as a system file serving as the 32-bit in-process handler specified by the InprocHandler32 key.</span></span>                                                                                                            |
| <span data-ttu-id="bea14-213">Null</span><span class="sxs-lookup"><span data-stu-id="bea14-213">Null</span></span>                 | <span data-ttu-id="bea14-214">Les champs DefInprocHandler et argument peuvent tous deux avoir la valeur null pour une clé de CLSID LocalServer ou LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="bea14-214">The DefInprocHandler and Argument fields can both be Null for a LocalServer or LocalServer32 CLSID key.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="bea14-215">1 = par défaut (système)</span><span class="sxs-lookup"><span data-stu-id="bea14-215">1 = default (system)</span></span> | <span data-ttu-id="bea14-216">La valeur par défaut est le gestionnaire in-process 16 bits spécifié par InprocHandler.</span><span class="sxs-lookup"><span data-stu-id="bea14-216">The default is the 16-bit in-process handler specified by InprocHandler.</span></span> <span data-ttu-id="bea14-217">Dans ce cas, la valeur de InprocHandler est le nom dans le Registre sous lequel la valeur du gestionnaire in-process par défaut est stockée.</span><span class="sxs-lookup"><span data-stu-id="bea14-217">In this case, the value of InprocHandler is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="bea14-218">Par exemple, HKEY \_ local \_ machine machine \\ Software \\ classes \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="bea14-218">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span>     |
| <span data-ttu-id="bea14-219">2 = par défaut (système)</span><span class="sxs-lookup"><span data-stu-id="bea14-219">2 = default (system)</span></span> | <span data-ttu-id="bea14-220">La valeur par défaut est le gestionnaire in-process 32 bits spécifié par InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="bea14-220">The default is the 32-bit in-process handler specified by InprocHandler32.</span></span> <span data-ttu-id="bea14-221">Dans ce cas, la valeur de InprocHandler32 est le nom dans le Registre sous lequel la valeur du gestionnaire in-process par défaut est stockée.</span><span class="sxs-lookup"><span data-stu-id="bea14-221">In this case, the value of InprocHandler32 is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="bea14-222">Par exemple, HKEY \_ local \_ machine machine \\ Software \\ classes \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="bea14-222">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span> |
| <span data-ttu-id="bea14-223">3 = valeur par défaut (système)</span><span class="sxs-lookup"><span data-stu-id="bea14-223">3 = default (system)</span></span> | <span data-ttu-id="bea14-224">La valeur par défaut est un gestionnaire in-process 16 bits ou 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bea14-224">The default is a 16-bit or 32-bit in-process handler.</span></span>                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="bea14-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="bea14-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="bea14-226">Si une clé de CLSID LocalServer ou LocalServer32 apparaît dans le champ de contexte, le texte de ce champ est enregistré en tant qu’argument sur le serveur et est utilisé par COM pour appeler le serveur.</span><span class="sxs-lookup"><span data-stu-id="bea14-226">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the text in this field is registered as the argument against the server and is used by COM to invoke the server.</span></span> <span data-ttu-id="bea14-227">Les champs DefInprocHandler et argument peuvent tous les deux avoir la valeur null si LocalServer ou LocalServer32 apparaît dans le champ de contexte.</span><span class="sxs-lookup"><span data-stu-id="bea14-227">The DefInprocHandler and Argument fields can both be Null if LocalServer or LocalServer32 appears in the Context field.</span></span>

<span data-ttu-id="bea14-228">Notez que la résolution des propriétés dans le champ argument est limitée.</span><span class="sxs-lookup"><span data-stu-id="bea14-228">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="bea14-229">Une propriété mise en forme en tant que \[ propriété \] dans ce champ ne peut être résolue que si la propriété a déjà la valeur prévue lorsque le composant propriétaire de la classe est installé.</span><span class="sxs-lookup"><span data-stu-id="bea14-229">A property formatted as \[Property\] in this field can only be resolved if the property already has the intended value when the component owning the class is installed.</span></span> <span data-ttu-id="bea14-230">Par exemple, pour que l’argument « \[ \#MyDoc.doc\] » soit résolu à la valeur correcte, le même processus doit installer le fichier MyDoc.doc et le composant qui possède la classe.</span><span class="sxs-lookup"><span data-stu-id="bea14-230">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the class.</span></span>

</dd> <dt>

<span data-ttu-id="bea14-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="bea14-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="bea14-232">Clé externe dans la [table de fonctionnalités](feature-table.md) spécifiant la fonctionnalité qui fournit le serveur com.</span><span class="sxs-lookup"><span data-stu-id="bea14-232">External key into the [Feature table](feature-table.md) specifying the feature that provides the COM server.</span></span>

<span data-ttu-id="bea14-233">Clé externe vers la colonne de l’une des tables de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bea14-233">External key to column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="bea14-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="bea14-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="bea14-235">Si **msidbClassAttributesRelativePath** est défini dans cette colonne, le nom de fichier complet peut être utilisé pour les serveurs com.</span><span class="sxs-lookup"><span data-stu-id="bea14-235">If **msidbClassAttributesRelativePath** is set in this column, the bare file name can be used for COM servers.</span></span> <span data-ttu-id="bea14-236">Le programme d’installation enregistre le nom de fichier uniquement au lieu du chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="bea14-236">The installer registers the file name only instead of the complete path.</span></span> <span data-ttu-id="bea14-237">Cela permet au serveur dans le répertoire actif de prendre la priorité et autorise plusieurs copies du même composant.</span><span class="sxs-lookup"><span data-stu-id="bea14-237">This enables the server in the current directory to take precedence and allows multiple copies of the same component.</span></span>



| <span data-ttu-id="bea14-238">Attribut</span><span class="sxs-lookup"><span data-stu-id="bea14-238">Attribute</span></span>                            | <span data-ttu-id="bea14-239">Decimal</span><span class="sxs-lookup"><span data-stu-id="bea14-239">Decimal</span></span> | <span data-ttu-id="bea14-240">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="bea14-240">Hexadecimal</span></span> |
|--------------------------------------|---------|-------------|
| <span data-ttu-id="bea14-241">**msidbClassAttributesRelativePath**</span><span class="sxs-lookup"><span data-stu-id="bea14-241">**msidbClassAttributesRelativePath**</span></span> | <span data-ttu-id="bea14-242">1</span><span class="sxs-lookup"><span data-stu-id="bea14-242">1</span></span>       | <span data-ttu-id="bea14-243">0x001</span><span class="sxs-lookup"><span data-stu-id="bea14-243">0x001</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bea14-244">Notes</span><span class="sxs-lookup"><span data-stu-id="bea14-244">Remarks</span></span>

<span data-ttu-id="bea14-245">Cette table est référencée lorsque l’action [RegisterClassInfo](registerclassinfo-action.md) ou l' [action UnregisterClassInfo](unregisterclassinfo-action.md) sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="bea14-245">This table is referred to when the [RegisterClassInfo action](registerclassinfo-action.md) or the [UnregisterClassInfo action](unregisterclassinfo-action.md) are executed.</span></span>

## <a name="validation"></a><span data-ttu-id="bea14-246">Validation</span><span class="sxs-lookup"><span data-stu-id="bea14-246">Validation</span></span>

<dl>

[<span data-ttu-id="bea14-247">ICE03</span><span class="sxs-lookup"><span data-stu-id="bea14-247">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="bea14-248">ICE06</span><span class="sxs-lookup"><span data-stu-id="bea14-248">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="bea14-249">ICE19</span><span class="sxs-lookup"><span data-stu-id="bea14-249">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="bea14-250">ICE32</span><span class="sxs-lookup"><span data-stu-id="bea14-250">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="bea14-251">ICE36</span><span class="sxs-lookup"><span data-stu-id="bea14-251">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="bea14-252">ICE41</span><span class="sxs-lookup"><span data-stu-id="bea14-252">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="bea14-253">ICE42</span><span class="sxs-lookup"><span data-stu-id="bea14-253">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="bea14-254">ICE46</span><span class="sxs-lookup"><span data-stu-id="bea14-254">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="bea14-255">ICE66</span><span class="sxs-lookup"><span data-stu-id="bea14-255">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="bea14-256">ICE69</span><span class="sxs-lookup"><span data-stu-id="bea14-256">ICE69</span></span>](ice69.md)  
</dl>

 

 

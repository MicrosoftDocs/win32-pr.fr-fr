---
description: La table ActionText contient le texte à afficher dans une boîte de dialogue de progression et écrit dans le journal pour les actions dont l’exécution prend beaucoup de temps. Le texte affiché comprend la description de l’action et, éventuellement, les données mises en forme à partir de l’action.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Table ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517801"
---
# <a name="actiontext-table"></a><span data-ttu-id="7aa21-104">Table ActionText</span><span class="sxs-lookup"><span data-stu-id="7aa21-104">ActionText Table</span></span>

<span data-ttu-id="7aa21-105">La table ActionText contient le texte à afficher dans une boîte de dialogue de progression et écrit dans le journal pour les actions dont l’exécution prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="7aa21-105">The ActionText Table contains text to be displayed in a progress dialog box, and written to the log for actions that take a long time to execute.</span></span> <span data-ttu-id="7aa21-106">Le texte affiché comprend la description de l’action et, éventuellement, les données mises en forme à partir de l’action.</span><span class="sxs-lookup"><span data-stu-id="7aa21-106">The displayed text consists of the action description and optionally formatted data from the action.</span></span>

<span data-ttu-id="7aa21-107">La table ActionText contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7aa21-107">The ActionText Table has the following columns.</span></span>



| <span data-ttu-id="7aa21-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="7aa21-108">Column</span></span>      | <span data-ttu-id="7aa21-109">Type</span><span class="sxs-lookup"><span data-stu-id="7aa21-109">Type</span></span>                         | <span data-ttu-id="7aa21-110">Clé</span><span class="sxs-lookup"><span data-stu-id="7aa21-110">Key</span></span> | <span data-ttu-id="7aa21-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7aa21-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="7aa21-112">Action</span><span class="sxs-lookup"><span data-stu-id="7aa21-112">Action</span></span>      | [<span data-ttu-id="7aa21-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="7aa21-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7aa21-114">O</span><span class="sxs-lookup"><span data-stu-id="7aa21-114">Y</span></span>   | <span data-ttu-id="7aa21-115">N</span><span class="sxs-lookup"><span data-stu-id="7aa21-115">N</span></span>        |
| <span data-ttu-id="7aa21-116">Description</span><span class="sxs-lookup"><span data-stu-id="7aa21-116">Description</span></span> | [<span data-ttu-id="7aa21-117">Text</span><span class="sxs-lookup"><span data-stu-id="7aa21-117">Text</span></span>](text.md)             | <span data-ttu-id="7aa21-118">N</span><span class="sxs-lookup"><span data-stu-id="7aa21-118">N</span></span>   | <span data-ttu-id="7aa21-119">O</span><span class="sxs-lookup"><span data-stu-id="7aa21-119">Y</span></span>        |
| <span data-ttu-id="7aa21-120">Modèle</span><span class="sxs-lookup"><span data-stu-id="7aa21-120">Template</span></span>    | [<span data-ttu-id="7aa21-121">Modèle</span><span class="sxs-lookup"><span data-stu-id="7aa21-121">Template</span></span>](template.md)     | <span data-ttu-id="7aa21-122">N</span><span class="sxs-lookup"><span data-stu-id="7aa21-122">N</span></span>   | <span data-ttu-id="7aa21-123">O</span><span class="sxs-lookup"><span data-stu-id="7aa21-123">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7aa21-124">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7aa21-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7aa21-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="7aa21-125"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="7aa21-126">Nom de l'action.</span><span class="sxs-lookup"><span data-stu-id="7aa21-126">Name of the action.</span></span>

<span data-ttu-id="7aa21-127">Clé de table primaire.</span><span class="sxs-lookup"><span data-stu-id="7aa21-127">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="7aa21-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="7aa21-128"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="7aa21-129">Description localisée affichée dans la boîte de dialogue de progression, ou écrite dans le journal lorsque l’action est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7aa21-129">Localized description that is displayed in the progress dialog box, or written to the log when the action is executing.</span></span>

</dd> <dt>

<span data-ttu-id="7aa21-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Modèle</span><span class="sxs-lookup"><span data-stu-id="7aa21-130"><span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Template</span></span>
</dt> <dd>

<span data-ttu-id="7aa21-131">Modèle de format localisé utilisé pour mettre en forme les enregistrements de données d’action à afficher pendant l’exécution de l’action.</span><span class="sxs-lookup"><span data-stu-id="7aa21-131">A localized format template that is used to format action data records to display during action execution.</span></span> <span data-ttu-id="7aa21-132">Si aucun modèle n’est fourni, les données d’action ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="7aa21-132">If a template is not supplied, then the action data is not displayed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7aa21-133">Notes</span><span class="sxs-lookup"><span data-stu-id="7aa21-133">Remarks</span></span>

<span data-ttu-id="7aa21-134">En règle générale, les entrées de la table ActionText font référence aux actions des tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="7aa21-134">Typically, the entries in the ActionText table refer to actions in sequence tables.</span></span> <span data-ttu-id="7aa21-135">Le programme d’installation effectue d’autres actions qui ne sont pas répertoriées dans la table de séquence, mais qui doivent toujours être spécifiées dans la table.</span><span class="sxs-lookup"><span data-stu-id="7aa21-135">There are other actions the installer performs that are not listed in the sequence table, but still need to be specified in the table.</span></span> <span data-ttu-id="7aa21-136">Le tableau suivant identifie les entrées de table requises pour lesquelles le nom d’action et le modèle doivent être créés exactement comme indiqué, mais la description peut être personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7aa21-136">The following table identifies the required table entries where the action name and template must be authored exactly as shown, but the description can be customized.</span></span>



| <span data-ttu-id="7aa21-137">Action</span><span class="sxs-lookup"><span data-stu-id="7aa21-137">Action</span></span>          | <span data-ttu-id="7aa21-138">Description</span><span class="sxs-lookup"><span data-stu-id="7aa21-138">Description</span></span>                             | <span data-ttu-id="7aa21-139">Modèle</span><span class="sxs-lookup"><span data-stu-id="7aa21-139">Template</span></span> |
|-----------------|-----------------------------------------|----------|
| <span data-ttu-id="7aa21-140">Restauration</span><span class="sxs-lookup"><span data-stu-id="7aa21-140">Rollback</span></span>        | <span data-ttu-id="7aa21-141">Annule des actions.</span><span class="sxs-lookup"><span data-stu-id="7aa21-141">Undoes actions.</span></span>                         | <span data-ttu-id="7aa21-142">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7aa21-142">\[1\]</span></span>    |
| <span data-ttu-id="7aa21-143">RollbackCleanup</span><span class="sxs-lookup"><span data-stu-id="7aa21-143">RollbackCleanup</span></span> | <span data-ttu-id="7aa21-144">Supprime les anciens fichiers.</span><span class="sxs-lookup"><span data-stu-id="7aa21-144">Removes old files.</span></span>                      | <span data-ttu-id="7aa21-145">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7aa21-145">\[1\]</span></span>    |
| <span data-ttu-id="7aa21-146">GenerateScript</span><span class="sxs-lookup"><span data-stu-id="7aa21-146">GenerateScript</span></span>  | <span data-ttu-id="7aa21-147">Génère des opérations système pour l’action.</span><span class="sxs-lookup"><span data-stu-id="7aa21-147">Generates system operations for action.</span></span> | <span data-ttu-id="7aa21-148">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7aa21-148">\[1\]</span></span>    |



 

> [!Note]  
> <span data-ttu-id="7aa21-149">Le texte d’action s’affiche uniquement pour les actions qui s’exécutent dans le script d’installation.</span><span class="sxs-lookup"><span data-stu-id="7aa21-149">Action text is only displayed for actions that run within the installation script.</span></span> <span data-ttu-id="7aa21-150">Par conséquent, le texte d’action s’affiche uniquement pour les actions qui sont séquencées entre les actions [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa21-150">Therefore, action text is only displayed for actions that are sequenced between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

 

<span data-ttu-id="7aa21-151">Vous pouvez importer une table ActionText localisée dans votre base de données à l’aide de Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span><span class="sxs-lookup"><span data-stu-id="7aa21-151">You can import a localized ActionText table into your database by using Msidb.exe or [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).</span></span> <span data-ttu-id="7aa21-152">Le kit de développement logiciel (SDK) contient une table ActionText localisée pour chacune des langues listées dans la section [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa21-152">The SDK includes a localized ActionText Table for each of the languages listed in the [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) section.</span></span> <span data-ttu-id="7aa21-153">Si la table ActionText n’est pas remplie, le programme d’installation charge les chaînes localisées pour la langue spécifiée par la propriété [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa21-153">If the ActionText table is not populated, the installer loads localized strings for the language specified by the [**ProductLanguage**](productlanguage.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="7aa21-154">Validation</span><span class="sxs-lookup"><span data-stu-id="7aa21-154">Validation</span></span>

<dl>

[<span data-ttu-id="7aa21-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="7aa21-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7aa21-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="7aa21-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7aa21-157">ICE46</span><span class="sxs-lookup"><span data-stu-id="7aa21-157">ICE46</span></span>](ice46.md)  
</dl>

 

 




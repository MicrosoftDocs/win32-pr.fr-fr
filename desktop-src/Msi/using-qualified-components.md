---
description: Les composants qualifiés sont une méthode d’indirection et peuvent être utilisés pour regrouper des composants avec des fonctionnalités parallèles dans des catégories.
ms.assetid: 45a05ab2-d951-415d-bdb8-cb0a73eb9967
title: Utilisation des composants qualifiés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11233a91e8883d1a4151957d3e73d18ebdcff25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113242"
---
# <a name="using-qualified-components"></a><span data-ttu-id="ac809-103">Utilisation des composants qualifiés</span><span class="sxs-lookup"><span data-stu-id="ac809-103">Using Qualified Components</span></span>

<span data-ttu-id="ac809-104">Les composants qualifiés sont une méthode d’indirection et peuvent être utilisés pour regrouper des composants avec des fonctionnalités parallèles dans des catégories.</span><span class="sxs-lookup"><span data-stu-id="ac809-104">Qualified components are a method of indirection and can be used to group components with parallel functionality into categories.</span></span>

<span data-ttu-id="ac809-105">Pour retourner le chemin d’accès complet et installer un [composant qualifié](qualified-components.md), appelez [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span><span class="sxs-lookup"><span data-stu-id="ac809-105">To return the full path and install a [qualified component](qualified-components.md), call [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa).</span></span>

<span data-ttu-id="ac809-106">Pour énumérer tous les qualificateurs de composants qualifiés et les chaînes descriptives, appelez [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="ac809-106">To enumerate all of the qualified component qualifiers and descriptive strings, call [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

<span data-ttu-id="ac809-107">**Pour regrouper des composants dans une catégorie de composants qualifiés**</span><span class="sxs-lookup"><span data-stu-id="ac809-107">**To group components together into a qualified-component category**</span></span>

1.  <span data-ttu-id="ac809-108">Il doit y avoir un enregistrement dans la [table](component-table.md) des composants pour chaque composant inclus dans la nouvelle catégorie de composants qualifiés.</span><span class="sxs-lookup"><span data-stu-id="ac809-108">There must be a record in the [Component table](component-table.md) for each component that is included in the new category of qualified components.</span></span> <span data-ttu-id="ac809-109">Créez les champs de la table Component de la même façon que pour les composants ordinaires.</span><span class="sxs-lookup"><span data-stu-id="ac809-109">Author the fields in the Component table the same as for ordinary components.</span></span> <span data-ttu-id="ac809-110">Notez que chaque composant qualifié doit avoir un GUID d’ID de composant unique entré dans la colonne ComponentId de la table des composants.</span><span class="sxs-lookup"><span data-stu-id="ac809-110">Note that each qualified component must have a unique component ID GUID entered in the ComponentId column of the Component table.</span></span>
2.  <span data-ttu-id="ac809-111">Générez une chaîne de texte de qualificateur pour chaque composant qualifié.</span><span class="sxs-lookup"><span data-stu-id="ac809-111">Generate a qualifier text string for each qualified component.</span></span> <span data-ttu-id="ac809-112">Le qualificateur doit être une chaîne de texte unique qui peut être générée facilement lors de la recherche d’un composant qualifié.</span><span class="sxs-lookup"><span data-stu-id="ac809-112">The qualifier must be unique text string that can be easily generated when searching for a qualified component.</span></span> <span data-ttu-id="ac809-113">Par exemple, si les composants de la catégorie sont qualifiés par langue, l’identificateur de paramètres régionaux (LCID) numérique est une chaîne de qualificateur raisonnable.</span><span class="sxs-lookup"><span data-stu-id="ac809-113">For example, if the components in the category are being qualified by language, the numeric locale identifier (LCID) is a reasonable qualifier string.</span></span>
3.  <span data-ttu-id="ac809-114">Ajoutez un enregistrement dans la [table PublishComponent](publishcomponent-table.md) pour chaque composant qualifié.</span><span class="sxs-lookup"><span data-stu-id="ac809-114">Add a record in the [PublishComponent table](publishcomponent-table.md) for each qualified component.</span></span> <span data-ttu-id="ac809-115">Entrez les identificateurs de composant qualifiés de la colonne composant de la table de composants dans la \_ colonne composant de la table PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="ac809-115">Enter the qualified-component identifiers from the Component column of the Component table into the Component\_ column of the PublishComponent table.</span></span> <span data-ttu-id="ac809-116">Entrez les chaînes de qualificateur pour chaque composant qualifié dans la colonne qualificateur.</span><span class="sxs-lookup"><span data-stu-id="ac809-116">Enter the qualifier strings for each qualified component into the Qualifier column.</span></span> <span data-ttu-id="ac809-117">Entrez une chaîne localisée à afficher à l’utilisateur et décrivant le composant qualifié dans la colonne facultative AppData.</span><span class="sxs-lookup"><span data-stu-id="ac809-117">Enter a localized string to be displayed to the user and describing the qualified component into the optional AppData column.</span></span> <span data-ttu-id="ac809-118">Une chaîne explicative doit être placée dans le champ AppData, par exemple « dictionnaire français », au lieu du LCID numérique uniquement.</span><span class="sxs-lookup"><span data-stu-id="ac809-118">An explanatory string should be put in the AppData field, such as "French Dictionary," rather than just the numeric LCID.</span></span> <span data-ttu-id="ac809-119">Entrez le nom de la fonctionnalité qui utilise ce composant dans la \_ colonne fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ac809-119">Enter the name of the feature that uses this component into the Feature\_ column.</span></span> <span data-ttu-id="ac809-120">L’identificateur de fonctionnalité dans ce champ doit également être listé dans la colonne fonctionnalité du [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ac809-120">The feature identifier in this field must also be listed in the Feature column of the [Feature table](feature-table.md).</span></span>
4.  <span data-ttu-id="ac809-121">Générez un GUID de catégorie pour cette catégorie de composants qualifiés.</span><span class="sxs-lookup"><span data-stu-id="ac809-121">Generate a category GUID for this category of qualified components.</span></span> <span data-ttu-id="ac809-122">Il doit s’agir d’un [GUID](guid.md)valide.</span><span class="sxs-lookup"><span data-stu-id="ac809-122">This must be a valid [GUID](guid.md).</span></span> <span data-ttu-id="ac809-123">Si vous utilisez un utilitaire tel que GUIDGEN pour générer le GUID, assurez-vous qu’il contient uniquement des lettres majuscules.</span><span class="sxs-lookup"><span data-stu-id="ac809-123">If you use a utility such as GUIDGEN to generate the GUID be sure that it contains only uppercase letters.</span></span> <span data-ttu-id="ac809-124">Pour chaque composant qualifié de cette catégorie, entrez le GUID de la catégorie dans le champ ComponentId de la [table PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="ac809-124">For every qualified component in this category, enter the category GUID into the ComponentId field of the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="ac809-125">L’exemple suivant montre comment la catégorie « modèles de télécopie » des composants qualifiés est créée dans les tables composant, fonctionnalité et PublishComponent.</span><span class="sxs-lookup"><span data-stu-id="ac809-125">The following example illustrates how the "FAX Templates" category of qualified components are authored into the Component, Feature, and PublishComponent tables.</span></span>

[<span data-ttu-id="ac809-126">Table PublishComponent</span><span class="sxs-lookup"><span data-stu-id="ac809-126">PublishComponent table</span></span>](publishcomponent-table.md)



| <span data-ttu-id="ac809-127">ComponentId</span><span class="sxs-lookup"><span data-stu-id="ac809-127">ComponentId</span></span>                  | <span data-ttu-id="ac809-128">Qualificateur</span><span class="sxs-lookup"><span data-stu-id="ac809-128">Qualifier</span></span> | <span data-ttu-id="ac809-129">AppData</span><span class="sxs-lookup"><span data-stu-id="ac809-129">AppData</span></span>             | <span data-ttu-id="ac809-130">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="ac809-130">Feature\_</span></span>   | <span data-ttu-id="ac809-131">-\_</span><span class="sxs-lookup"><span data-stu-id="ac809-131">Component\_</span></span>    |
|------------------------------|-----------|---------------------|-------------|----------------|
| <span data-ttu-id="ac809-132">{GUID de catégorie de modèle de télécopie}</span><span class="sxs-lookup"><span data-stu-id="ac809-132">{FAX Template Category GUID}</span></span> | <span data-ttu-id="ac809-133">1033</span><span class="sxs-lookup"><span data-stu-id="ac809-133">1033</span></span>      | <span data-ttu-id="ac809-134">Modèle anglais américain</span><span class="sxs-lookup"><span data-stu-id="ac809-134">US English template</span></span> | <span data-ttu-id="ac809-135">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-135">FAXTemplate</span></span> | <span data-ttu-id="ac809-136">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="ac809-136">FAXTemplateENU</span></span> |
|                              | <span data-ttu-id="ac809-137">1041</span><span class="sxs-lookup"><span data-stu-id="ac809-137">1041</span></span>      | <span data-ttu-id="ac809-138">Modèle japonais</span><span class="sxs-lookup"><span data-stu-id="ac809-138">Japanese template</span></span>   | <span data-ttu-id="ac809-139">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-139">FAXTemplate</span></span> | <span data-ttu-id="ac809-140">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="ac809-140">FAXTemplateJPN</span></span> |
|                              | <span data-ttu-id="ac809-141">1054</span><span class="sxs-lookup"><span data-stu-id="ac809-141">1054</span></span>      | <span data-ttu-id="ac809-142">Modèle thaï</span><span class="sxs-lookup"><span data-stu-id="ac809-142">Thai template</span></span>       | <span data-ttu-id="ac809-143">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-143">FAXTemplate</span></span> | <span data-ttu-id="ac809-144">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="ac809-144">FAXTemplateTHA</span></span> |
|                              | <span data-ttu-id="ac809-145">1031</span><span class="sxs-lookup"><span data-stu-id="ac809-145">1031</span></span>      | <span data-ttu-id="ac809-146">Modèle allemand</span><span class="sxs-lookup"><span data-stu-id="ac809-146">German template</span></span>     | <span data-ttu-id="ac809-147">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-147">FAXTemplate</span></span> | <span data-ttu-id="ac809-148">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="ac809-148">FAXTemplateDEU</span></span> |



 

<span data-ttu-id="ac809-149">[Table des composants](component-table.md) (table partielle)</span><span class="sxs-lookup"><span data-stu-id="ac809-149">[Component table](component-table.md) (partial table)</span></span>



| <span data-ttu-id="ac809-150">Composant</span><span class="sxs-lookup"><span data-stu-id="ac809-150">Component</span></span>      | <span data-ttu-id="ac809-151">ComponentId</span><span class="sxs-lookup"><span data-stu-id="ac809-151">ComponentId</span></span>                                  |
|----------------|----------------------------------------------|
| <span data-ttu-id="ac809-152">FAXTemplateENU</span><span class="sxs-lookup"><span data-stu-id="ac809-152">FAXTemplateENU</span></span> | <span data-ttu-id="ac809-153">{*GUID du composant de modèle de télécopie (anglais des États-Unis)*}</span><span class="sxs-lookup"><span data-stu-id="ac809-153">{*FAX Template (US English) component GUID*}</span></span> |
| <span data-ttu-id="ac809-154">FAXTemplateJPN</span><span class="sxs-lookup"><span data-stu-id="ac809-154">FAXTemplateJPN</span></span> | <span data-ttu-id="ac809-155">{*GUID du composant de modèle de télécopie (japonais)*}</span><span class="sxs-lookup"><span data-stu-id="ac809-155">{*FAX Template (Japanese) component GUID*}</span></span>   |
| <span data-ttu-id="ac809-156">FAXTemplateTHA</span><span class="sxs-lookup"><span data-stu-id="ac809-156">FAXTemplateTHA</span></span> | <span data-ttu-id="ac809-157">{*GUID du composant de modèle de télécopie (thaï)*}</span><span class="sxs-lookup"><span data-stu-id="ac809-157">{*FAX Template (Thai) component GUID*}</span></span>       |
| <span data-ttu-id="ac809-158">FAXTemplateDEU</span><span class="sxs-lookup"><span data-stu-id="ac809-158">FAXTemplateDEU</span></span> | <span data-ttu-id="ac809-159">{*GUID du composant de modèle de télécopie (allemand)*}</span><span class="sxs-lookup"><span data-stu-id="ac809-159">{*FAX Template (German) component GUID*}</span></span>     |



 

<span data-ttu-id="ac809-160">[Table des fonctionnalités](feature-table.md) (table partielle)</span><span class="sxs-lookup"><span data-stu-id="ac809-160">[Feature table](feature-table.md) (partial table)</span></span>



| <span data-ttu-id="ac809-161">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="ac809-161">Feature</span></span>     |
|-------------|
| <span data-ttu-id="ac809-162">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-162">FAXTemplate</span></span> |
| <span data-ttu-id="ac809-163">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-163">FAXTemplate</span></span> |
| <span data-ttu-id="ac809-164">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-164">FAXTemplate</span></span> |
| <span data-ttu-id="ac809-165">FAXTemplate</span><span class="sxs-lookup"><span data-stu-id="ac809-165">FAXTemplate</span></span> |



 

 

 




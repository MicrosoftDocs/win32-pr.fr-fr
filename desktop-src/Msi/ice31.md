---
description: ICE31 valide tous les styles de polices prédéfinis utilisés dans les contrôles qui affichent du texte. Il vérifie également que la propriété DefaultUIFont fait référence à un style de police valide.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203580"
---
# <a name="ice31"></a><span data-ttu-id="6c70d-104">ICE31</span><span class="sxs-lookup"><span data-stu-id="6c70d-104">ICE31</span></span>

<span data-ttu-id="6c70d-105">ICE31 valide tous les styles de polices prédéfinis utilisés dans les [contrôles](controls.md) qui affichent du texte.</span><span class="sxs-lookup"><span data-stu-id="6c70d-105">ICE31 validates any predefined font styles used in [controls](controls.md) that display text.</span></span> <span data-ttu-id="6c70d-106">Il vérifie également que la propriété [**DefaultUIFont**](defaultuifont.md) fait référence à un style de police valide.</span><span class="sxs-lookup"><span data-stu-id="6c70d-106">It also validates that the [**DefaultUIFont**](defaultuifont.md) property refers to a valid font style.</span></span>

<span data-ttu-id="6c70d-107">Les contrôles peuvent avoir un style de police prédéfini comme décrit dans [Ajout de contrôles et de texte](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="6c70d-107">Controls can have a predefined font style as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="6c70d-108">Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&*style*} à la chaîne de caractères affichés.</span><span class="sxs-lookup"><span data-stu-id="6c70d-108">To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&*style*}.</span></span> <span data-ttu-id="6c70d-109">Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c70d-109">Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="6c70d-110">Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie comme un style de texte valide, cette police sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="6c70d-110">If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.</span></span>

<span data-ttu-id="6c70d-111">ICE31 vérifie la colonne de texte pour chaque contrôle dans la [table de contrôle](control-table.md) afin de vérifier qu’il existe une entrée valide dans la [table TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c70d-111">ICE31 checks the Text column for each control in the [Control Table](control-table.md) to verifies that a valid entry exist in the [TextStyle table](textstyle-table.md).</span></span>

<span data-ttu-id="6c70d-112">ICE31 ignore le [contrôle ScrollableText](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="6c70d-112">ICE31 ignores the [ScrollableText Control](scrollabletext-control.md).</span></span>

## <a name="results"></a><span data-ttu-id="6c70d-113">Résultats</span><span class="sxs-lookup"><span data-stu-id="6c70d-113">Results</span></span>

<span data-ttu-id="6c70d-114">ICE31 publie un message d’erreur pour les styles non définis, les noms de style trop longs, une table de style de filtre (TextStyle) manquante et des balises de style sans accolade fermante.</span><span class="sxs-lookup"><span data-stu-id="6c70d-114">ICE31 posts an error message for undefined styles, style names that are too long, a missing TextStyle table, and style tags with no closing brace.</span></span>

<span data-ttu-id="6c70d-115">ICE31 publie un avertissement si la balise de style n’est pas au début de la ligne, ou si un contrôle a plusieurs balises de style.</span><span class="sxs-lookup"><span data-stu-id="6c70d-115">ICE31 posts a warning if the style tag is not at the beginning of the line, or if a control has multiple style tags.</span></span>

## <a name="example"></a><span data-ttu-id="6c70d-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="6c70d-116">Example</span></span>

<span data-ttu-id="6c70d-117">ICE31 publie les erreurs suivantes pour l’exemple illustré :</span><span class="sxs-lookup"><span data-stu-id="6c70d-117">ICE31 posts the following errors for the example shown:</span></span>

-   <span data-ttu-id="6c70d-118">Le contrôle DialogB. Control1 utilise le style TextStyle BadStyle non défini.</span><span class="sxs-lookup"><span data-stu-id="6c70d-118">Control DialogB.Control1 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="6c70d-119">Le contrôle DialogB. Control2 utilise le style TextStyle BadStyle non défini.</span><span class="sxs-lookup"><span data-stu-id="6c70d-119">Control DialogB.Control2 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="6c70d-120">L’accolade fermante du style de texte est manquante dans le contrôle DialogB. Control6.</span><span class="sxs-lookup"><span data-stu-id="6c70d-120">Control DialogB.Control6 is missing closing brace in text style.</span></span>
-   <span data-ttu-id="6c70d-121">Le contrôle DialogB. Control3 spécifie un style de texte qui est trop long pour être valide.</span><span class="sxs-lookup"><span data-stu-id="6c70d-121">Control DialogB.Control3 specifies a text style that is too long to be valid.</span></span>

<span data-ttu-id="6c70d-122">ICE31 publie l’avertissement suivant pour l’exemple illustré :</span><span class="sxs-lookup"><span data-stu-id="6c70d-122">ICE31 posts the following warning for the example shown:</span></span>

-   <span data-ttu-id="6c70d-123">La balise de style texte dans DialogB. Control4 n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="6c70d-123">Text Style tag in DialogB.Control4 has no effect.</span></span> <span data-ttu-id="6c70d-124">Voulez-vous vraiment qu’elle apparaisse sous forme de texte ?</span><span class="sxs-lookup"><span data-stu-id="6c70d-124">Do you really want it to appear as text?</span></span>

<span data-ttu-id="6c70d-125">[Table de contrôle](control-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="6c70d-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="6c70d-126">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="6c70d-126">Dialog</span></span>  | <span data-ttu-id="6c70d-127">Contrôler</span><span class="sxs-lookup"><span data-stu-id="6c70d-127">Control</span></span>  | <span data-ttu-id="6c70d-128">Texte</span><span class="sxs-lookup"><span data-stu-id="6c70d-128">Text</span></span>                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c70d-129">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="6c70d-129">DialogA</span></span> | <span data-ttu-id="6c70d-130">Control0</span><span class="sxs-lookup"><span data-stu-id="6c70d-130">Control0</span></span> | <span data-ttu-id="6c70d-131">{ \\ OKStyle} il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-131">{\\OKStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="6c70d-132">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="6c70d-132">DialogA</span></span> | <span data-ttu-id="6c70d-133">Control1</span><span class="sxs-lookup"><span data-stu-id="6c70d-133">Control1</span></span> | <span data-ttu-id="6c70d-134">{&OKStyle} Il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-134">{&OKStyle}This is the text to display.</span></span>                                                                                                                              |
| <span data-ttu-id="6c70d-135">DialogB</span><span class="sxs-lookup"><span data-stu-id="6c70d-135">DialogB</span></span> | <span data-ttu-id="6c70d-136">Control1</span><span class="sxs-lookup"><span data-stu-id="6c70d-136">Control1</span></span> | <span data-ttu-id="6c70d-137">{&BadStyle} Il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-137">{&BadStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="6c70d-138">DialogB</span><span class="sxs-lookup"><span data-stu-id="6c70d-138">DialogB</span></span> | <span data-ttu-id="6c70d-139">Control2</span><span class="sxs-lookup"><span data-stu-id="6c70d-139">Control2</span></span> | <span data-ttu-id="6c70d-140">{ \\ BadStyle} il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-140">{\\BadStyle}This is the text to display.</span></span>                                                                                                                            |
| <span data-ttu-id="6c70d-141">DialogB</span><span class="sxs-lookup"><span data-stu-id="6c70d-141">DialogB</span></span> | <span data-ttu-id="6c70d-142">Control3</span><span class="sxs-lookup"><span data-stu-id="6c70d-142">Control3</span></span> | <span data-ttu-id="6c70d-143">{&style qui est supérieur à 72 caractères et, par conséquent, ne peut pas être un style même si vous l’avez géré pour l’obtenir dans la table TextStyle} Il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-143">{&Style that is over 72 chars and therefore cannot possibly be a style even if somehow you did manage to get it in the TextStyle table}This is the text to display.</span></span> |
| <span data-ttu-id="6c70d-144">DialogB</span><span class="sxs-lookup"><span data-stu-id="6c70d-144">DialogB</span></span> | <span data-ttu-id="6c70d-145">Control4</span><span class="sxs-lookup"><span data-stu-id="6c70d-145">Control4</span></span> | <span data-ttu-id="6c70d-146">Avertissement { \\ OKStyle} il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-146">Warning {\\OKStyle}This is the text to display.</span></span>                                                                                                                     |
| <span data-ttu-id="6c70d-147">DialogB</span><span class="sxs-lookup"><span data-stu-id="6c70d-147">DialogB</span></span> | <span data-ttu-id="6c70d-148">Control5</span><span class="sxs-lookup"><span data-stu-id="6c70d-148">Control5</span></span> | <span data-ttu-id="6c70d-149">{ \\ OKStyle} {&OKStyle} il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-149">{\\OKStyle}{&OKStyle}This is the text to display.</span></span>                                                                                                                   |
| <span data-ttu-id="6c70d-150">DialogB</span><span class="sxs-lookup"><span data-stu-id="6c70d-150">DialogB</span></span> | <span data-ttu-id="6c70d-151">Control6</span><span class="sxs-lookup"><span data-stu-id="6c70d-151">Control6</span></span> | <span data-ttu-id="6c70d-152">{ \\ OKStyle il s’agit du texte à afficher.</span><span class="sxs-lookup"><span data-stu-id="6c70d-152">{\\OKStyle This is the text to display.</span></span>                                                                                                                             |



 

<span data-ttu-id="6c70d-153">[Table TextStyle](textstyle-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="6c70d-153">[TextStyle table](textstyle-table.md) (partial)</span></span>



| <span data-ttu-id="6c70d-154">TextStyle</span><span class="sxs-lookup"><span data-stu-id="6c70d-154">TextStyle</span></span> |
|-----------|
| <span data-ttu-id="6c70d-155">OkStyle</span><span class="sxs-lookup"><span data-stu-id="6c70d-155">OkStyle</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="6c70d-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c70d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c70d-157">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="6c70d-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




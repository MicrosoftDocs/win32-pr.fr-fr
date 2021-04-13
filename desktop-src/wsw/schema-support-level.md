---
title: Niveau de prise en charge du schéma
description: Cette section décrit en détail le niveau de prise en charge du schéma.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Services Web du niveau de prise en charge des schémas pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104559460"
---
# <a name="schema-support-level"></a><span data-ttu-id="9d267-106">Niveau de prise en charge du schéma</span><span class="sxs-lookup"><span data-stu-id="9d267-106">Schema support level</span></span>

<span data-ttu-id="9d267-107">Cette section décrit en détail le niveau de prise en charge du schéma.</span><span class="sxs-lookup"><span data-stu-id="9d267-107">This section covers the details around the level of schema support.</span></span>


<span data-ttu-id="9d267-108">Le schéma prend directement en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9d267-108">The schema directly supports the following:</span></span>

-   <span data-ttu-id="9d267-109">Séquences d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9d267-109">Sequences of elements.</span></span>
-   <span data-ttu-id="9d267-110">Dérivation des types d’éléments.</span><span class="sxs-lookup"><span data-stu-id="9d267-110">Derivation of element types.</span></span>
-   <span data-ttu-id="9d267-111">Choix simples d’éléments (ceux qui sont mappés à une Union avec balises).</span><span class="sxs-lookup"><span data-stu-id="9d267-111">Simple choices of elements (those that map to a tagged union).</span></span>
-   <span data-ttu-id="9d267-112">Types de base définis par le format binaire XSD/.NET, y compris les plages (min/max).</span><span class="sxs-lookup"><span data-stu-id="9d267-112">Basic types defined by XSD / .NET binary format including ranges (min/max).</span></span>
-   <span data-ttu-id="9d267-113">Prise en charge simple de tout élément (aucune restriction sur le type d’élément).</span><span class="sxs-lookup"><span data-stu-id="9d267-113">Simple support for any element (no restrictions on type of element).</span></span>
-   <span data-ttu-id="9d267-114">Éléments et attributs facultatifs avec des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d267-114">Optional elements and attributes with default values.</span></span>
-   <span data-ttu-id="9d267-115">Répétition d’éléments avec des plages (min/max).</span><span class="sxs-lookup"><span data-stu-id="9d267-115">Repeating elements with ranges (min/max).</span></span>
-   <span data-ttu-id="9d267-116">Éléments nillable.</span><span class="sxs-lookup"><span data-stu-id="9d267-116">Nillable elements.</span></span>

<span data-ttu-id="9d267-117">Le schéma ne prend pas en charge directement les éléments suivants (ce qui implique le comportement « de secours ») :</span><span class="sxs-lookup"><span data-stu-id="9d267-117">The schema does not support the following directly (which imply the "fallback" behavior):</span></span>

-   <span data-ttu-id="9d267-118">Types de base définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d267-118">User defined basic types.</span></span>
-   <span data-ttu-id="9d267-119">Choix plus compliqués.</span><span class="sxs-lookup"><span data-stu-id="9d267-119">More complicated choices.</span></span>
-   <span data-ttu-id="9d267-120">Rejet des attributs inconnus.</span><span class="sxs-lookup"><span data-stu-id="9d267-120">Rejecting unknown attributes.</span></span>
-   <span data-ttu-id="9d267-121">Attributs inconnus d’un aller-retour.</span><span class="sxs-lookup"><span data-stu-id="9d267-121">Round tripping unknown attributes.</span></span>
-   <span data-ttu-id="9d267-122">Prise en charge plus complexe de tout élément.</span><span class="sxs-lookup"><span data-stu-id="9d267-122">More complicated support for any element.</span></span>
-   <span data-ttu-id="9d267-123">Construction All.</span><span class="sxs-lookup"><span data-stu-id="9d267-123">The all construct.</span></span>
-   <span data-ttu-id="9d267-124">Clé/keyref.</span><span class="sxs-lookup"><span data-stu-id="9d267-124">Key/keyref.</span></span>

<span data-ttu-id="9d267-125">Voici une répartition détaillée de la prise en charge des différents composants de schéma.</span><span class="sxs-lookup"><span data-stu-id="9d267-125">Following is a detailed breakdown of different schema component support.</span></span> <span data-ttu-id="9d267-126">Il est comparé au contrat de données dans WCF, car la similarité des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9d267-126">It is compared with data contract in WCF because the similarity in functionality.</span></span> <span data-ttu-id="9d267-127">La différence est décrite.</span><span class="sxs-lookup"><span data-stu-id="9d267-127">The difference will be described.</span></span>

<span data-ttu-id="9d267-128">En général, pour les comportements de secours :</span><span class="sxs-lookup"><span data-stu-id="9d267-128">Generally, for fallback behaviors:</span></span>

-   <span data-ttu-id="9d267-129">les attributs sont retransmis à WS \_ String ;</span><span class="sxs-lookup"><span data-stu-id="9d267-129">attributes are fall backed to WS\_STRING;</span></span>
-   <span data-ttu-id="9d267-130">le contenu de l’élément est stocké dans la \_ \_ mémoire tampon WS XML.</span><span class="sxs-lookup"><span data-stu-id="9d267-130">element content are fall backed to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="9d267-131">complexType sont représentées dans une structure contenant un champ de \_ tampon WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="9d267-131">complexType are fall backed to structure containing a field of WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="9d267-132">Les types simples sont retransmis à WS \_ String.</span><span class="sxs-lookup"><span data-stu-id="9d267-132">Simple types are fall backed to WS\_STRING.</span></span>

<span data-ttu-id="9d267-133">Wsutil génère des avertissements pour les composants de schéma qui ne sont pas entièrement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d267-133">wsutil generates warnings for schema components that are not currently fully supported.</span></span> <span data-ttu-id="9d267-134">L’application devra peut-être effectuer une vérification supplémentaire pour que ces composants soient nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9d267-134">Application might need to do additional verification for those components are needed.</span></span> <span data-ttu-id="9d267-135">Les Wsutil d’heures supplémentaires peuvent être améliorées pour gérer certaines des fonctionnalités actuellement prises en charge dans l’exécution, comme la prise en charge de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d267-135">Overtime wsutil can be improved to handle some of the features that are currently supported in runtime, like default value support.</span></span> <span data-ttu-id="9d267-136">Wsutil peut également être amélioré avec la sérialisation pour prendre en charge d’autres fonctionnalités telles que abstract.</span><span class="sxs-lookup"><span data-stu-id="9d267-136">wsutil can also be improved together with serialization to support other features like abstract.</span></span> <span data-ttu-id="9d267-137">Le nombre de composants de schéma non pris en charge peut être réduit dans le temps.</span><span class="sxs-lookup"><span data-stu-id="9d267-137">The number of unsupported schema components can be reduced over time.</span></span>

## <a name="the-overall-schema-document"></a><span data-ttu-id="9d267-138">Document de schéma global</span><span class="sxs-lookup"><span data-stu-id="9d267-138">The Overall Schema Document</span></span>

<span data-ttu-id="9d267-139">Définition globale qui peut affecter les définitions incorporées dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="9d267-139">Global definition that might affect embedded definitions in the schema.</span></span> <span data-ttu-id="9d267-140">Il s’agit d’attributs globaux qui s’appliquent à toutes les définitions du schéma.</span><span class="sxs-lookup"><span data-stu-id="9d267-140">These are global attributes that are applicable to all definitions in the schema.</span></span>

<span data-ttu-id="9d267-141"><XS : Schema> attributs</span><span class="sxs-lookup"><span data-stu-id="9d267-141"><xs:schema> attributes</span></span>

-   <span data-ttu-id="9d267-142">attributeFromDefault ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-142">attributeFromDefault Ignored.</span></span>
-   <span data-ttu-id="9d267-143">blockDefault ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-143">blockDefault Ignored.</span></span>
-   <span data-ttu-id="9d267-144">elementFormDefault ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-144">elementFormDefault Ignored.</span></span> <span data-ttu-id="9d267-145">Cela est différent de dataContract, car les éléments non qualifiés sont pris en charge dans le Runtime.</span><span class="sxs-lookup"><span data-stu-id="9d267-145">This is different from dataContract as unqualified elements are supported in runtime.</span></span>
-   <span data-ttu-id="9d267-146">finalDefault ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-146">finalDefault Ignored.</span></span> <span data-ttu-id="9d267-147">Il n’existe pas de prise en charge du langage C pour le concept final.</span><span class="sxs-lookup"><span data-stu-id="9d267-147">There is no C language support for the concept of final.</span></span>
-   <span data-ttu-id="9d267-148">ID ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-148">id Ignored.</span></span>
-   <span data-ttu-id="9d267-149">targetNamespace pris en charge et mappé à l’espace de noms du service.</span><span class="sxs-lookup"><span data-stu-id="9d267-149">targetNamespace Supported and mapped to the service namespace.</span></span>
-   <span data-ttu-id="9d267-150">version ignorée.</span><span class="sxs-lookup"><span data-stu-id="9d267-150">version Ignored.</span></span>

<span data-ttu-id="9d267-151"><XS : Schema> contents</span><span class="sxs-lookup"><span data-stu-id="9d267-151"><xs:schema> contents</span></span>

-   <span data-ttu-id="9d267-152">include pris en charge ; Wsutil requiert que toutes les définitions nécessaires soient disponibles en tant que fichiers d’entrée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="9d267-152">include Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="9d267-153">redéfinition ignorée.</span><span class="sxs-lookup"><span data-stu-id="9d267-153">redefine Ignored.</span></span> <span data-ttu-id="9d267-154">Wsutil ne prend pas en charge cette.</span><span class="sxs-lookup"><span data-stu-id="9d267-154">wsutil does not support this.</span></span>
-   <span data-ttu-id="9d267-155">importation prise en charge ; Wsutil requiert que toutes les définitions nécessaires soient disponibles en tant que fichiers d’entrée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="9d267-155">import Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="9d267-156">simpleType pris en charge-voir la section type simple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9d267-156">simpleType Supported- see simple type section below.</span></span>
-   <span data-ttu-id="9d267-157">complexType pris en charge-voir la section’complexType'</span><span class="sxs-lookup"><span data-stu-id="9d267-157">complexType Supported- see 'complexType' section</span></span>
-   <span data-ttu-id="9d267-158">Groupe ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-158">group Ignored.</span></span>
-   <span data-ttu-id="9d267-159">attributeGroup ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-159">attributeGroup Ignored.</span></span>
-   <span data-ttu-id="9d267-160">élément pris en charge ; correspond aux définitions d’éléments globaux.</span><span class="sxs-lookup"><span data-stu-id="9d267-160">element Supported; maps to global element definitions.</span></span>
-   <span data-ttu-id="9d267-161">attribut pris en charge ; correspond aux définitions d’attributs globaux.</span><span class="sxs-lookup"><span data-stu-id="9d267-161">attribute Supported; maps to global attribute definitions.</span></span>
-   <span data-ttu-id="9d267-162">Notation ignorée</span><span class="sxs-lookup"><span data-stu-id="9d267-162">notation Ignored</span></span>

## <a name="complex-type"></a><span data-ttu-id="9d267-163">Type complexe</span><span class="sxs-lookup"><span data-stu-id="9d267-163">Complex Type</span></span>

<span data-ttu-id="9d267-164">Le type complexe, représenté par <XS : complexType>, peut être la restriction d’un type simple ou d’un type complexe, d’une extension de type simple, de tableaux ou de structures.</span><span class="sxs-lookup"><span data-stu-id="9d267-164">Complex type, represented by <xs:complexType>, could be restriction of simple type or complex type, extension of simple type, arrays or structure.</span></span> <span data-ttu-id="9d267-165">Nous avons remarqué que dans l’extension de types simples, il n’y a pas d’héritage et aucune prise en charge de xsi : type.</span><span class="sxs-lookup"><span data-stu-id="9d267-165">Noticed that in extension of simple types, there is no inheritance and no xsi:type support.</span></span>

<span data-ttu-id="9d267-166"><XS : complexType> attributs</span><span class="sxs-lookup"><span data-stu-id="9d267-166"><xs:complexType> attributes</span></span>

-   <span data-ttu-id="9d267-167">Résumé générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-167">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-168">bloquer générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-168">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-169">final générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-169">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-170">ID ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-170">id Ignored.</span></span>
-   <span data-ttu-id="9d267-171">Générer un avertissement sur la fonctionnalité non prise en charge, revenir à la structure avec la \_ \_ mémoire tampon WS XML si la valeur est true.</span><span class="sxs-lookup"><span data-stu-id="9d267-171">mixed Generate warning about unsupported feature, fallback to structure with WS\_XML\_BUFFER if true.</span></span>
-   <span data-ttu-id="9d267-172">nom pris en charge et mappé au nom du type de structure.</span><span class="sxs-lookup"><span data-stu-id="9d267-172">name Supported and mapped to structure type name.</span></span>

<span data-ttu-id="9d267-173"><XS : complexType> contenu</span><span class="sxs-lookup"><span data-stu-id="9d267-173"><xs:complexType> contents</span></span>

<span data-ttu-id="9d267-174">Il s’agit de la définition de type pour la structure.</span><span class="sxs-lookup"><span data-stu-id="9d267-174">This is type definition for structure.</span></span> <span data-ttu-id="9d267-175">la restriction complexContent n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d267-175">complexContent restriction is not supported.</span></span>

-   <span data-ttu-id="9d267-176">complexContent prend en charge l’extension de contenu complexe.</span><span class="sxs-lookup"><span data-stu-id="9d267-176">complexContent Support complex content extension.</span></span> <span data-ttu-id="9d267-177">Mappe à l’héritage de la structure.</span><span class="sxs-lookup"><span data-stu-id="9d267-177">Maps to structure inheritance.</span></span>
-   <span data-ttu-id="9d267-178">Groupe de secours actuellement à la structure avec le \_ champ de tampon WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="9d267-178">group Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="9d267-179">Peut être pris en charge en fonction de la particule sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="9d267-179">Can be supported according to the underneath particle.</span></span>
-   <span data-ttu-id="9d267-180">choix pris en charge en tant qu’Union.</span><span class="sxs-lookup"><span data-stu-id="9d267-180">choice supported as union.</span></span> <span data-ttu-id="9d267-181">Cela n’est pas pris en charge dans le contrat de données.</span><span class="sxs-lookup"><span data-stu-id="9d267-181">This is not supported in data contract.</span></span>
-   <span data-ttu-id="9d267-182">Sequence pris en charge : correspond aux champs d’une structure</span><span class="sxs-lookup"><span data-stu-id="9d267-182">sequence Supported - maps to fields of a structure</span></span>
-   <span data-ttu-id="9d267-183">attribut pris en charge avec une exception de « interdit ».</span><span class="sxs-lookup"><span data-stu-id="9d267-183">attribute supported with one exception of 'prohibited'.</span></span> <span data-ttu-id="9d267-184">secours à la structure avec \_ la \_ mémoire tampon XML WS si « interdit ».</span><span class="sxs-lookup"><span data-stu-id="9d267-184">fallback to structure with WS\_XML\_BUFFER if 'prohibited'.</span></span>
-   <span data-ttu-id="9d267-185">attributeGroup pris en charge : correspond à la séquence d’attributs</span><span class="sxs-lookup"><span data-stu-id="9d267-185">attributeGroup supported - maps to sequence of attributes</span></span>
-   <span data-ttu-id="9d267-186">anyAttribute ignoré</span><span class="sxs-lookup"><span data-stu-id="9d267-186">anyAttribute Ignored</span></span>
-   <span data-ttu-id="9d267-187">AttributeGroupRef pris en charge : correspond à la séquence d’attributs.</span><span class="sxs-lookup"><span data-stu-id="9d267-187">AttributeGroupRef Supported - maps to sequence of attributes.</span></span>
-   <span data-ttu-id="9d267-188">GroupRef est actuellement en train de revenir à la structure avec le \_ champ de tampon WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="9d267-188">GroupRef Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="9d267-189">Peut être pris en charge selon le groupe sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9d267-189">Can be supported according to the underneath group.</span></span>
-   <span data-ttu-id="9d267-190">Tout pris en charge, mappe à une \_ mémoire tampon XML</span><span class="sxs-lookup"><span data-stu-id="9d267-190">Any Supported, maps to XML\_BUFFER</span></span>
-   <span data-ttu-id="9d267-191">(vide) pris en charge, mappage à la description de struct vide sans struct généré.</span><span class="sxs-lookup"><span data-stu-id="9d267-191">(blank) supported map to empty struct description with no struct generated.</span></span>

<span data-ttu-id="9d267-192"><xs:sequence> dans un type complexe : contenu</span><span class="sxs-lookup"><span data-stu-id="9d267-192"><xs:sequence> in a complex type: contents</span></span>

<span data-ttu-id="9d267-193">Wsutil prend entièrement en charge la séquence de minOccurs = 1 et maxOccurs = 1 ; dans le cas contraire, le type complexe est actuellement transmis à la \_ \_ mémoire tampon WS XML.</span><span class="sxs-lookup"><span data-stu-id="9d267-193">wsutil only fully support sequence of minOccurs = 1 and maxOccurs = 1; otherwise the complex type is currently fall backed to WS\_XML\_BUFFER.</span></span> <span data-ttu-id="9d267-194">Il peut être pris en charge en tant que tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="9d267-194">It can be supported as array of structures.</span></span>

-   <span data-ttu-id="9d267-195">élément pris en charge ; chaque instance est mappée à un champ de la structure.</span><span class="sxs-lookup"><span data-stu-id="9d267-195">element Supported; each instance maps to a field in the structure.</span></span>
-   <span data-ttu-id="9d267-196">Groupe de secours ; le complexType est de secours à \_ la \_ mémoire tampon XML WS.</span><span class="sxs-lookup"><span data-stu-id="9d267-196">Group fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="9d267-197">Tout secours ; le complexType est de secours à \_ la \_ mémoire tampon XML WS.</span><span class="sxs-lookup"><span data-stu-id="9d267-197">All fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="9d267-198">choix pris en charge ; mappage au champ d’Union.</span><span class="sxs-lookup"><span data-stu-id="9d267-198">choice supported; map to union field.</span></span>
-   <span data-ttu-id="9d267-199">séquence de secours ; le complexType est de secours à \_ la \_ mémoire tampon XML WS.</span><span class="sxs-lookup"><span data-stu-id="9d267-199">sequence fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="9d267-200">tout pris en charge ; mappé à la \_ mémoire tampon XML.</span><span class="sxs-lookup"><span data-stu-id="9d267-200">any Supported; mapped to XML\_BUFFER.</span></span>
-   <span data-ttu-id="9d267-201">(vide) pris en charge ; complexType peut être une structure vide s’il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="9d267-201">(blank) supported; complexType can be an empty structure if there is no attributes.</span></span>

## <a name="elements"></a><span data-ttu-id="9d267-202">Éléments</span><span class="sxs-lookup"><span data-stu-id="9d267-202">Elements</span></span>

<span data-ttu-id="9d267-203"><XS : ELEMENT>peut se produire dans trois contextes.</span><span class="sxs-lookup"><span data-stu-id="9d267-203"><xs:element>may occur in three contexts.</span></span>

-   <span data-ttu-id="9d267-204">Elle peut se produire dans un <XS : Sequence> décrivant un champ d’un struct normal.</span><span class="sxs-lookup"><span data-stu-id="9d267-204">It may occur within an <xs:sequence>, describing a field of a regular struct.</span></span> <span data-ttu-id="9d267-205">Dans ce cas, l’attribut maxOccurs doit avoir la 1.</span><span class="sxs-lookup"><span data-stu-id="9d267-205">In this case, the maxOccurs attribute must be 1.</span></span> <span data-ttu-id="9d267-206">Le champ est facultatif si minOccurs a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="9d267-206">The field is optional if minOccurs is 0.</span></span>
-   <span data-ttu-id="9d267-207">Elle peut se produire dans un <XS : Sequence> décrivant un champ d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="9d267-207">It may occur within an <xs:sequence>, describing a field of an array.</span></span> <span data-ttu-id="9d267-208">Dans ce cas, l’attribut maxOccurs doit être supérieur à 1 ou non lié.</span><span class="sxs-lookup"><span data-stu-id="9d267-208">In this case, the maxOccurs attribute must be greater than 1 or 'unbounded'.</span></span>
-   <span data-ttu-id="9d267-209">Elle peut se produire dans un <XS : Schema> comme une description globale de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9d267-209">It may occur within an <xs:schema> as a global element description.</span></span>

<span data-ttu-id="9d267-210"><XS : ELEMENT> dans un <XS : Sequence> ou <XS : Choice> en tant que champ dans une structure</span><span class="sxs-lookup"><span data-stu-id="9d267-210"><xs:element> within an <xs:sequence> or <xs:choice> as a field in a structure</span></span>

-   <span data-ttu-id="9d267-211">Prise en charge de la référence ; résolu en référence à un élément global.</span><span class="sxs-lookup"><span data-stu-id="9d267-211">ref Supported; resolved to reference to global element.</span></span>
-   <span data-ttu-id="9d267-212">nom pris en charge, mappe au nom du champ.</span><span class="sxs-lookup"><span data-stu-id="9d267-212">name Supported, maps to field name.</span></span>
-   <span data-ttu-id="9d267-213">type pris en charge, mappe au type de champ.</span><span class="sxs-lookup"><span data-stu-id="9d267-213">type Supported, maps to field type.</span></span> <span data-ttu-id="9d267-214">Pour plus d’informations, consultez « mappage de type ».</span><span class="sxs-lookup"><span data-stu-id="9d267-214">For more information, see 'Type Mapping'.</span></span> <span data-ttu-id="9d267-215">S’il n’est pas spécifié (et que l’élément ne contient pas de type anonyme), XS : anyType est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d267-215">If not specified (and the element does not contain an anonymous type), xs:anyType is assumed.</span></span>
-   <span data-ttu-id="9d267-216">bloquer générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-216">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-217">par défaut, générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-217">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-218">correction de la génération d’un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-218">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-219">formulaire ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-219">form Ignored.</span></span> <span data-ttu-id="9d267-220">Notre couche de sérialisation prend en charge les formulaires qualifiés et non qualifiés.</span><span class="sxs-lookup"><span data-stu-id="9d267-220">Our serialization layer supports both qualified and unqualified forms.</span></span>
-   <span data-ttu-id="9d267-221">ID ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-221">id Ignored.</span></span>
-   <span data-ttu-id="9d267-222">maxOccurs est mappé à un champ de données unique si est égal à 1.</span><span class="sxs-lookup"><span data-stu-id="9d267-222">maxOccurs maps to a single data field if equals 1.</span></span> <span data-ttu-id="9d267-223">elle est mappée à un champ de tableau (élément répétitif) si maxOccurs est supérieur à 1.</span><span class="sxs-lookup"><span data-stu-id="9d267-223">it is mapped to an array field (repeating element) if maxOccurs is larger than 1.</span></span>
-   <span data-ttu-id="9d267-224">minOccurs si la valeur est 0, le champ options est défini sur champ \_ facultatif, si la valeur nillable n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="9d267-224">minOccurs if 0, the field options is set to FIELD\_OPTIONAL, if nillable is not set.</span></span>
-   <span data-ttu-id="9d267-225">nillable le champ est nillable.</span><span class="sxs-lookup"><span data-stu-id="9d267-225">nillable The field is nillable.</span></span> <span data-ttu-id="9d267-226">Pour plus d’informations, consultez [sérialisation](serialization.md) .</span><span class="sxs-lookup"><span data-stu-id="9d267-226">See [Serialization](serialization.md) for more detail.</span></span>

<span data-ttu-id="9d267-227"><XS : ELEMENT> en tant qu’élément global : attributs</span><span class="sxs-lookup"><span data-stu-id="9d267-227"><xs:element> as global element: attributes</span></span>

<span data-ttu-id="9d267-228">les attributs minOccurs et maxOccurs ne sont pas valides en tant que Description d’élément global.</span><span class="sxs-lookup"><span data-stu-id="9d267-228">minOccurs and maxOccurs attributes are invalid as global element description.</span></span> <span data-ttu-id="9d267-229">L’application peut utiliser directement la description de l’élément généré dans la couche de sérialisation ou les couches de canal.</span><span class="sxs-lookup"><span data-stu-id="9d267-229">Application can use generated element description in serialization layer or channel layers directly.</span></span>

-   <span data-ttu-id="9d267-230">Résumé générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-230">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-231">bloquer générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-231">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-232">par défaut, générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-232">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-233">final générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-233">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-234">correction de la génération d’un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-234">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-235">ID ignoré.</span><span class="sxs-lookup"><span data-stu-id="9d267-235">id Ignored.</span></span>
-   <span data-ttu-id="9d267-236">nom pris en charge : mappez le nom de la description de l’élément global et il s’agit de la base du type anonyme lorsqu’il est spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d267-236">name Supported- map to name of the global element description, and it is the base for the anonymous type when specified.</span></span>
-   <span data-ttu-id="9d267-237">nillable ignoré-l’application doit appeler avec l’indicateur Right.</span><span class="sxs-lookup"><span data-stu-id="9d267-237">nillable Ignored-application needs to call with right flag.</span></span>
-   <span data-ttu-id="9d267-238">l’ensemble de la solution de secours à la structure avec la \_ mémoire tampon XML WS est \_ définie.</span><span class="sxs-lookup"><span data-stu-id="9d267-238">substitutionGroup fallback to structure with WS\_XML\_BUFFER if set.</span></span> <span data-ttu-id="9d267-239">Wsutil ne prend pas en charge substitutionGroup.</span><span class="sxs-lookup"><span data-stu-id="9d267-239">wsutil does not support substitutionGroup.</span></span>
-   <span data-ttu-id="9d267-240">tapez pris en charge et mappez au type de l’élément.</span><span class="sxs-lookup"><span data-stu-id="9d267-240">type Supported and map to the type of the element.</span></span>

<span data-ttu-id="9d267-241"><XS : ELEMENT> en tant qu’élément global : contenu</span><span class="sxs-lookup"><span data-stu-id="9d267-241"><xs:element> as global element: contents</span></span>

-   <span data-ttu-id="9d267-242">simpleType pris en charge ; correspond à la définition de type.</span><span class="sxs-lookup"><span data-stu-id="9d267-242">simpleType Supported; maps to type definition.</span></span>
-   <span data-ttu-id="9d267-243">complexType pris en charge ; correspond à un type complexe.</span><span class="sxs-lookup"><span data-stu-id="9d267-243">complexType supported; maps to a complex type.</span></span>
-   <span data-ttu-id="9d267-244">génération unique avertissement sur la fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-244">unique Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="9d267-245">Wsutil ne prend pas en charge les contraintes d’élément.</span><span class="sxs-lookup"><span data-stu-id="9d267-245">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="9d267-246">clé générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-246">key Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="9d267-247">Wsutil ne prend pas en charge les contraintes d’élément.</span><span class="sxs-lookup"><span data-stu-id="9d267-247">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="9d267-248">keyref générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-248">keyref Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="9d267-249">Wsutil ne prend pas en charge les contraintes d’élément.</span><span class="sxs-lookup"><span data-stu-id="9d267-249">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="9d267-250">Occult Géré l’élément sans spécification de type est traité comme XS : anyType.</span><span class="sxs-lookup"><span data-stu-id="9d267-250">(blank) Supported; element with no type specification is treated as xs:anyType.</span></span>

## <a name="simple-types"></a><span data-ttu-id="9d267-251">Types simples</span><span class="sxs-lookup"><span data-stu-id="9d267-251">Simple Types</span></span>

<span data-ttu-id="9d267-252"><XS : simpleType> attributs</span><span class="sxs-lookup"><span data-stu-id="9d267-252"><xs:simpleType> attributes</span></span>

-   <span data-ttu-id="9d267-253">Final générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-253">Final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-254">ID ignoré</span><span class="sxs-lookup"><span data-stu-id="9d267-254">Id Ignored</span></span>
-   <span data-ttu-id="9d267-255">Nom pris en charge, mappe au nom de type.</span><span class="sxs-lookup"><span data-stu-id="9d267-255">Name Supported, maps to type name.</span></span>

<span data-ttu-id="9d267-256"><XS : simpleType> contenu</span><span class="sxs-lookup"><span data-stu-id="9d267-256"><xs:simpleType> contents</span></span>

-   <span data-ttu-id="9d267-257">Restriction prise en charge, mappe au type ou à la plage d’énumération.</span><span class="sxs-lookup"><span data-stu-id="9d267-257">Restriction Supported, maps to enum type or range.</span></span> <span data-ttu-id="9d267-258">Consultez la section « restrictions XS : simpleType ».</span><span class="sxs-lookup"><span data-stu-id="9d267-258">See "xs:simpleType restrictions" section.</span></span>
-   <span data-ttu-id="9d267-259">Liste générer un avertissement sur les fonctionnalités non prises en charge, de secours à la \_ mémoire tampon XML.</span><span class="sxs-lookup"><span data-stu-id="9d267-259">List Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>
-   <span data-ttu-id="9d267-260">L’Union génère un avertissement sur la fonctionnalité non prise en charge, de secours à la \_ mémoire tampon XML.</span><span class="sxs-lookup"><span data-stu-id="9d267-260">Union Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>

## <a name="simple-type-restriction"></a><span data-ttu-id="9d267-261">Restriction de type simple</span><span class="sxs-lookup"><span data-stu-id="9d267-261">Simple Type restriction</span></span>

<span data-ttu-id="9d267-262">Certaines facettes sont autorisées dans des types intégraux et des chaînes pour permettre la prise en charge de Range et d’enum.</span><span class="sxs-lookup"><span data-stu-id="9d267-262">Certain facets are allowed in integral types and strings type to allow range and enum support.</span></span>

<span data-ttu-id="9d267-263">prise en charge de l’énumération</span><span class="sxs-lookup"><span data-stu-id="9d267-263">enumeration support</span></span>

<span data-ttu-id="9d267-264"><XS : Enumeration> restriction de type simple pour le type de base de String est traitée comme un type enum.</span><span class="sxs-lookup"><span data-stu-id="9d267-264"><xs:enumeration> simple type restriction for base type of string is treated as enum type.</span></span> <span data-ttu-id="9d267-265">Dans ce cas, l’attribut de base doit être de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="9d267-265">In this case, the Base attribute MUST be string type.</span></span> <span data-ttu-id="9d267-266">Dans le cas d’énumération, toutes les autres facettes sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="9d267-266">In enumeration case, all other facets are ignored.</span></span>

<span data-ttu-id="9d267-267">plage sur la prise en charge de type simple</span><span class="sxs-lookup"><span data-stu-id="9d267-267">range on simple type support</span></span>

<span data-ttu-id="9d267-268">Certaines facettes sont prises en charge dans les types simples. elles prennent en charge efficacement la plage autorisée sur le type.</span><span class="sxs-lookup"><span data-stu-id="9d267-268">Some facets are support in simple types support effectively range allowed on the type.</span></span> <span data-ttu-id="9d267-269">Les éléments suivants sont des restrictions pour les types intégraux et les types float/double.</span><span class="sxs-lookup"><span data-stu-id="9d267-269">Following are restriction for integral types and float/double types.</span></span> <span data-ttu-id="9d267-270">Les types simples avec d’autres facettes sont représentées dans le \_ type de chaîne WS</span><span class="sxs-lookup"><span data-stu-id="9d267-270">Simple types with other facets are fall backed to WS\_STRING type</span></span>

-   <span data-ttu-id="9d267-271">minExclusive pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d267-271">minExclusive Supported</span></span>
-   <span data-ttu-id="9d267-272">minInclusive pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d267-272">minInclusive Supported</span></span>
-   <span data-ttu-id="9d267-273">maxExclusive pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d267-273">maxExclusive Supported</span></span>
-   <span data-ttu-id="9d267-274">maxInclusive pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d267-274">maxInclusive Supported</span></span>
-   <span data-ttu-id="9d267-275">totalDigits générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-275">totalDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-276">fractionDigits générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-276">fractionDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-277">longueur générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-277">length Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-278">minLength générer un avertissement sur la fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-278">minLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-279">maxLength génère un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-279">maxLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-280">l’énumération génère un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-280">enumeration Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-281">whiteSpace générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-281">whiteSpace Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-282">modèle générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.</span><span class="sxs-lookup"><span data-stu-id="9d267-282">pattern Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="9d267-283">Occult Géré.</span><span class="sxs-lookup"><span data-stu-id="9d267-283">(blank) Supported.</span></span>

<span data-ttu-id="9d267-284">les fonctions minLength et maxLength sur String ne sont pas prises en charge actuellement, mais cette fonctionnalité est souhaitable pour la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9d267-284">minLength and maxLength on string is not supported currently but is a desirable feature to support.</span></span>

## <a name="inheritance"></a><span data-ttu-id="9d267-285">Héritage</span><span class="sxs-lookup"><span data-stu-id="9d267-285">Inheritance</span></span>

<span data-ttu-id="9d267-286">Wsutil prend en charge l’héritage de types complexes, autrement dit, une structure peut hériter d’une autre structure, similaire à l’héritage d’interface en C++.</span><span class="sxs-lookup"><span data-stu-id="9d267-286">Wsutil supports inheritance of complex types, that is, a structure can inherit from another structure, similar to interface inheritance in C++.</span></span> <span data-ttu-id="9d267-287">Pour ce faire, <> XS : complexContentExtension.</span><span class="sxs-lookup"><span data-stu-id="9d267-287">This is done through <xs:complexContentExtension>.</span></span> <span data-ttu-id="9d267-288"><XS : simpleContentExtension> est pris en charge, mais est généré en tant que structure simple avec le type de base comme premier champ au lieu de l’héritage de type.</span><span class="sxs-lookup"><span data-stu-id="9d267-288"><xs:simpleContentExtension> is supported but is generated as plain structure with base type as first field instead of type inheritance.</span></span>

## <a name="typeprimitive-mapping"></a><span data-ttu-id="9d267-289">Mappage de type/primitif</span><span class="sxs-lookup"><span data-stu-id="9d267-289">Type/primitive mapping</span></span>

<span data-ttu-id="9d267-290">Les identificateurs doivent être normalisés lors de la traduction à partir de NCName en XML.</span><span class="sxs-lookup"><span data-stu-id="9d267-290">Identifiers needs to be normalized when translating from NCNames in XML.</span></span> <span data-ttu-id="9d267-291">Les chaînes sont null ; les types de pointeur sont nillable ; les types intégraux et float/double sont nillable et defaultValue prend la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="9d267-291">Strings are nillable; pointer types are nillable; integral types and float/double are nillable and defaultValue is set to 0.</span></span>

![Tableau présentant le mappage entre les types XSD et les types de données saphir.](images/schematypemap.png)

 

 





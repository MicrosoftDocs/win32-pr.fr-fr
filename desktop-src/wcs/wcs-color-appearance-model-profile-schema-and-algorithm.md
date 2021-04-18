---
title: Algorithme et schéma de profil de modèle d’apparence de couleur WCS
description: Algorithme et schéma de profil de modèle d’apparence de couleur WCS
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Système de couleurs Windows (WCS), profil de modèle d’apparence de couleur (CAMP)
- WCS (système de couleurs Windows), profil de modèle d’apparence de couleur (CAMP)
- gestion des couleurs des images, profil de modèle d’apparence de couleur (CAMP)
- gestion des couleurs, profil de modèle d’apparence de couleur (CAMP)
- couleurs, profil de modèle d’apparence de couleur (CAMP)
- Système de couleurs Windows (WCS), profils
- WCS (système de couleurs Windows), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- Profil de modèle d’apparence de couleur (CAMP)
- CAMP (modèle d’apparence de couleur)
- schémas, profil de modèle d’apparence de couleur (CAMP)
- algorithmes, profil de modèle d’apparence de couleur (CAMP)
- Profil du modèle d’apparence des couleurs WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106520216"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a><span data-ttu-id="385a2-118">Algorithme et schéma de profil de modèle d’apparence de couleur WCS</span><span class="sxs-lookup"><span data-stu-id="385a2-118">WCS Color Appearance Model Profile Schema and Algorithm</span></span>

[<span data-ttu-id="385a2-119">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="385a2-119">Overview</span></span>](#overview)

[<span data-ttu-id="385a2-120">Architecture de profil de modèle d’apparence de couleur (CAMP)</span><span class="sxs-lookup"><span data-stu-id="385a2-120">Color Appearance Model Profile (CAMP) Architecture</span></span>](#color-appearance-model-profile-architecture)

[<span data-ttu-id="385a2-121">Schéma CAMP</span><span class="sxs-lookup"><span data-stu-id="385a2-121">The CAMP Schema</span></span>](#the-camp-schema)

[<span data-ttu-id="385a2-122">Éléments du schéma CAMP</span><span class="sxs-lookup"><span data-stu-id="385a2-122">The CAMP Schema Elements</span></span>](#the-camp-schema-elements)

[<span data-ttu-id="385a2-123">Algorithme CAMP</span><span class="sxs-lookup"><span data-stu-id="385a2-123">The CAMP Algorithm</span></span>](#the-camp-algorithm)

### <a name="overview"></a><span data-ttu-id="385a2-124">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="385a2-124">Overview</span></span>

<span data-ttu-id="385a2-125">Ce schéma est utilisé pour spécifier le contenu d’un profil de modèle d’apparence de couleur (CAMP).</span><span class="sxs-lookup"><span data-stu-id="385a2-125">This schema is used to specify the content of a color appearance model profile (CAMP).</span></span> <span data-ttu-id="385a2-126">Les algorithmes de base de référence associés sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="385a2-126">The associated baseline algorithms are described in the following sections.</span></span>

<span data-ttu-id="385a2-127">Le CAMP est composé de balises XML qui fournissent des valeurs paramétriques aux variables de modèle d’apparence de couleur de ligne de base CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="385a2-127">The CAMP is composed of XML tags that provide parametric values to the CIECAM02 baseline color appearance model variables.</span></span> <span data-ttu-id="385a2-128">Des détails sur les plages de paramètres sont fournis dans la spécification modèle d’apparence de couleur de ligne de base et recommandation CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="385a2-128">Details on the ranges for parameters are provided in the baseline color appearance model specification and CIECAM02 recommendation.</span></span>

### <a name="color-appearance-model-profile-architecture"></a><span data-ttu-id="385a2-129">Architecture du modèle d’apparence de couleur</span><span class="sxs-lookup"><span data-stu-id="385a2-129">Color Appearance Model Profile Architecture</span></span>

![Diagramme qui montre l’architecture du profil CAMP constituée de balises X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a><span data-ttu-id="385a2-131">Schéma CAMP</span><span class="sxs-lookup"><span data-stu-id="385a2-131">The CAMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a><span data-ttu-id="385a2-132">Éléments du schéma CAMP</span><span class="sxs-lookup"><span data-stu-id="385a2-132">The CAMP Schema Elements</span></span>

## <a name="colorappearancemodel"></a><span data-ttu-id="385a2-133">ColorAppearanceModel</span><span class="sxs-lookup"><span data-stu-id="385a2-133">ColorAppearanceModel</span></span>

<span data-ttu-id="385a2-134">Cet élément est une séquence de :</span><span class="sxs-lookup"><span data-stu-id="385a2-134">This element is a sequence of:</span></span>

1.  <span data-ttu-id="385a2-135">Chaîne ProfileName,</span><span class="sxs-lookup"><span data-stu-id="385a2-135">ProfileName string,</span></span>
2.  <span data-ttu-id="385a2-136">chaîne de description facultative,</span><span class="sxs-lookup"><span data-stu-id="385a2-136">optional Description string,</span></span>
3.  <span data-ttu-id="385a2-137">chaîne d’auteur facultative,</span><span class="sxs-lookup"><span data-stu-id="385a2-137">optional Author string,</span></span>
4.  <span data-ttu-id="385a2-138">Élément ViewingConditions.</span><span class="sxs-lookup"><span data-stu-id="385a2-138">ViewingConditions element.</span></span>

<span data-ttu-id="385a2-139">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="385a2-139">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="385a2-140">Les longueurs de chaîne sont limitées à 10 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="385a2-140">String lengths are limited to 10,000 characters.</span></span>

## <a name="namespace"></a><span data-ttu-id="385a2-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="385a2-141">Namespace</span></span>

<span data-ttu-id="385a2-142">xmlns : CAM = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="385a2-142">xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

<span data-ttu-id="385a2-143">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="385a2-143">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

## <a name="version"></a><span data-ttu-id="385a2-144">Version</span><span class="sxs-lookup"><span data-stu-id="385a2-144">Version</span></span>

<span data-ttu-id="385a2-145">Version &gt; 0,1 ou &lt; = « 1,0 » avec la première version de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="385a2-145">Version &gt;0.1 or &lt;= "1.0" with the first release of Windows Vista.</span></span>

<span data-ttu-id="385a2-146">**Conditions de validation :** Toute valeur de version &lt; = 2,0 est également valide pour prendre en charge des modifications sans rupture au format.</span><span class="sxs-lookup"><span data-stu-id="385a2-146">**Validation conditions:** Any version value &lt;=2.0 is also valid to support non-breaking changes to the format.</span></span>

## <a name="documentation"></a><span data-ttu-id="385a2-147">Documentation</span><span class="sxs-lookup"><span data-stu-id="385a2-147">Documentation</span></span>

<span data-ttu-id="385a2-148">Schéma de profil du modèle d’apparence des couleurs.</span><span class="sxs-lookup"><span data-stu-id="385a2-148">Color Appearance Model Profile Schema.</span></span>

<span data-ttu-id="385a2-149">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="385a2-149">Copyright (C) Microsoft.</span></span> <span data-ttu-id="385a2-150">Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="385a2-150">All rights reserved.</span></span>

<span data-ttu-id="385a2-151">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="385a2-151">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="surroundtype"></a><span data-ttu-id="385a2-152">SurroundType</span><span class="sxs-lookup"><span data-stu-id="385a2-152">SurroundType</span></span>

<span data-ttu-id="385a2-153">Cet élément est soit une énumération de paramètres CIECAM02 « Average », « Dim » ou « Dark », soit les paramètres quantitatifs réels de la recommandation CIECAM02 c, l’impact de l’entourage.</span><span class="sxs-lookup"><span data-stu-id="385a2-153">This element is a either an enumeration of "Average," "Dim," or "Dark" CIECAM02 parameters or the actual quantitative parameters from the CIECAM02 recommendation c, impact of the surround.</span></span>

<span data-ttu-id="385a2-154">**Conditions de validation :** Le paramètre c peut être compris entre 0,525 et 0,69.</span><span class="sxs-lookup"><span data-stu-id="385a2-154">**Validation conditions:** The c parameter can range from 0.525 to 0.69.</span></span>

## <a name="viewingconditions"></a><span data-ttu-id="385a2-155">ViewingConditions</span><span class="sxs-lookup"><span data-stu-id="385a2-155">ViewingConditions</span></span>

<span data-ttu-id="385a2-156">Cet élément se compose des sous-éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="385a2-156">This element consists of the following sub-elements:</span></span>



| <span data-ttu-id="385a2-157">Élément</span><span class="sxs-lookup"><span data-stu-id="385a2-157">Element</span></span>                    | <span data-ttu-id="385a2-158">Type</span><span class="sxs-lookup"><span data-stu-id="385a2-158">Type</span></span>           |
|----------------------------|----------------|
| <span data-ttu-id="385a2-159">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="385a2-159">WhitePoint</span></span>                 | <span data-ttu-id="385a2-160">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="385a2-160">WhitePointType</span></span> |
| <span data-ttu-id="385a2-161">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="385a2-161">Background</span></span>                 | <span data-ttu-id="385a2-162">CIEXYZ</span><span class="sxs-lookup"><span data-stu-id="385a2-162">CIEXYZ</span></span>         |
| <span data-ttu-id="385a2-163">Son</span><span class="sxs-lookup"><span data-stu-id="385a2-163">Surround</span></span>                   | <span data-ttu-id="385a2-164">SurroundType</span><span class="sxs-lookup"><span data-stu-id="385a2-164">SurroundType</span></span>   |
| <span data-ttu-id="385a2-165">LuminanceOfAdaptingField</span><span class="sxs-lookup"><span data-stu-id="385a2-165">LuminanceOfAdaptingField</span></span>   | <span data-ttu-id="385a2-166">float</span><span class="sxs-lookup"><span data-stu-id="385a2-166">float</span></span>          |
| <span data-ttu-id="385a2-167">DegreeOfAdaptation</span><span class="sxs-lookup"><span data-stu-id="385a2-167">DegreeOfAdaptation</span></span>         | <span data-ttu-id="385a2-168">float</span><span class="sxs-lookup"><span data-stu-id="385a2-168">float</span></span>          |
| <span data-ttu-id="385a2-169">NormalizeToMediaWhitePoint</span><span class="sxs-lookup"><span data-stu-id="385a2-169">NormalizeToMediaWhitePoint</span></span> | <span data-ttu-id="385a2-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="385a2-170">Boolean</span></span>        |



 

<span data-ttu-id="385a2-171">**Conditions de validation :** Les sous-éléments CIEXYZ sont validés par NonNegativeXYZType.</span><span class="sxs-lookup"><span data-stu-id="385a2-171">**Validation conditions:** CIEXYZ sub-elements are validated by NonNegativeXYZType.</span></span> <span data-ttu-id="385a2-172">LuminanceOfAdaptingField est un maximum de 10, 000cd/m ^ 2.</span><span class="sxs-lookup"><span data-stu-id="385a2-172">The LuminanceOfAdaptingField is a maximum of 10,000cd/m^2.</span></span> <span data-ttu-id="385a2-173">Le DegreeOfAdaptation peut être compris entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-173">The DegreeOfAdaptation can range from 0.0 to 1.0.</span></span> <span data-ttu-id="385a2-174">La valeur NormalizeToMediaWhitePoint peut être « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="385a2-174">The NormalizeToMediaWhitePoint value can be either "true" or "false."</span></span> <span data-ttu-id="385a2-175">Si le sous-élément NormalizeToMediaWhitePoint est absent, sa valeur par défaut est « true ».</span><span class="sxs-lookup"><span data-stu-id="385a2-175">If the NormalizeToMediaWhitePoint sub-element is absent, it effectively defaults to "true."</span></span> <span data-ttu-id="385a2-176">Consultez la section relative à l’algorithme CAMP suivante.</span><span class="sxs-lookup"><span data-stu-id="385a2-176">See the following CAMP algorithm section.</span></span>

## <a name="whitepointtype"></a><span data-ttu-id="385a2-177">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="385a2-177">WhitePointType</span></span>

<span data-ttu-id="385a2-178">Cet élément est soit une énumération de la valeur de la source de lumière CIE (« D50 », « D65 », « A » ou « F2 »), soit un sous-élément CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="385a2-178">This element is a either an enumeration of CIE light source value ("D50," "D65," "A," or "F2") or a CIEXYZ sub-element.</span></span>

<span data-ttu-id="385a2-179">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="385a2-179">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="ciexyztype"></a><span data-ttu-id="385a2-180">CIEXYZType</span><span class="sxs-lookup"><span data-stu-id="385a2-180">CIEXYZType</span></span>

<span data-ttu-id="385a2-181">L’élément CIEXYZType est composé de trois éléments à virgule flottante IEEE simple précision NonNegativeFloatType, nommés « X », « Y » et « Z ».</span><span class="sxs-lookup"><span data-stu-id="385a2-181">The CIEXYZType element is composed of three NonNegativeFloatType single-precision IEEE floating-point elements, named "X," "Y," and "Z."</span></span> <span data-ttu-id="385a2-182">Ces mesures peuvent être absolues (non relatives) CIEXYZ 1931 valeurs réfléchissantes ou valeurs réfléchies absolues (non relatives) CIEXYZ 1931 (transmissif) dans candelas par unités au carré du compteur.</span><span class="sxs-lookup"><span data-stu-id="385a2-182">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="385a2-183">**Conditions de validation :** Cela signifie que seules les valeurs réelles sont valides et que les valeurs de mesure CIEXYZ négatives ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="385a2-183">**Validation conditions:** This means that only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="385a2-184">Étant donné qu’il s’agit de valeurs absolues, les valeurs peuvent être comprises bien au-delà de 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="385a2-184">Since these are absolute values, values can range well beyond 1.0f.</span></span> <span data-ttu-id="385a2-185">Une limite raisonnable pour toute valeur X, Y ou Z sera arbitrairement définie sur 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="385a2-185">A reasonable limit for any X, Y, or Z value will be arbitrarily set to 10000.0f.</span></span>

 

### <a name="the-camp-algorithm"></a><span data-ttu-id="385a2-186">Algorithme CAMP</span><span class="sxs-lookup"><span data-stu-id="385a2-186">The CAMP Algorithm</span></span>

<span data-ttu-id="385a2-187">Le modèle d’apparence des couleurs (CAM) est basé sur les équations du modèle d’apparence des couleurs CIE CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="385a2-187">The color appearance model (CAM) is based on the CIE CIECAM02 color appearance model equations.</span></span>

<span data-ttu-id="385a2-188">Cette classe implémente la modélisation de l’apparence des couleurs.</span><span class="sxs-lookup"><span data-stu-id="385a2-188">This class implements the color appearance modeling.</span></span> <span data-ttu-id="385a2-189">Notez que le CAM WCS n’est *pas* remplaçable, par exemple, à l’aide d’un plug-in.</span><span class="sxs-lookup"><span data-stu-id="385a2-189">Note that the WCS CAM is *not* replaceable, for example, using a plug-in.</span></span> <span data-ttu-id="385a2-190">L’objectif de conception est de n’avoir qu’un seul modèle d’apparence des couleurs.</span><span class="sxs-lookup"><span data-stu-id="385a2-190">It is a design goal to have only one color appearance model.</span></span> <span data-ttu-id="385a2-191">Le CAM est basé sur les recommandations CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="385a2-191">The CAM is based on CIECAM02 recommendations.</span></span>

<span data-ttu-id="385a2-192">CIECAM02 peut être utilisé de deux manières.</span><span class="sxs-lookup"><span data-stu-id="385a2-192">CIECAM02 can be used in two ways.</span></span> <span data-ttu-id="385a2-193">Dans la direction de la colorimétrie à l’aspect, elle fournit un mappage de l’espace CIE XYZ à l’espace d’apparence de couleur.</span><span class="sxs-lookup"><span data-stu-id="385a2-193">In the colorimetric-to-appearance direction, it provides a mapping from CIE XYZ space to color appearance space.</span></span> <span data-ttu-id="385a2-194">Dans la direction de l’apparence à la colorimétrie, il mappe l’espace d’apparence de couleur à l’espace XYZ.</span><span class="sxs-lookup"><span data-stu-id="385a2-194">In the appearance-to-colorimetric direction, it maps from color appearance space back to XYZ space.</span></span> <span data-ttu-id="385a2-195">L’apparence des couleurs met en corrélation les clairs, J, chrominance, C et teinte, h.</span><span class="sxs-lookup"><span data-stu-id="385a2-195">The color appearance correlates lightness, J, chroma, C, and hue, h.</span></span> <span data-ttu-id="385a2-196">Ces trois valeurs forment un système de coordonnées cylindriques.</span><span class="sxs-lookup"><span data-stu-id="385a2-196">These three values form a cylindrical coordinate system.</span></span> <span data-ttu-id="385a2-197">Souvent, il s’avère plus pratique de travailler dans un système de coordonnées rectangulaires. par conséquent, calculez a = C COS h et b = C Sin h, pour fournir à CIECAM02 Jab.</span><span class="sxs-lookup"><span data-stu-id="385a2-197">Frequently, it turns out to be more convenient to work in a rectangular coordinate system, so compute a = C cos h and b = C sin h, to give CIECAM02 Jab.</span></span>

<span data-ttu-id="385a2-198">Vous pouvez utiliser des valeurs de clarté CAM supérieures à 100.</span><span class="sxs-lookup"><span data-stu-id="385a2-198">You can use CAM lightness values greater than 100.</span></span> <span data-ttu-id="385a2-199">Le Comité CIE qui a formulé CIECAM02 n’a pas résolu le comportement de l’axe de luminosité pour les valeurs d’entrée avec une luminance supérieure au point blanc adopté ; autrement dit, pour les valeurs Y d’entrée supérieures à la valeur Y du point blanc adopté.</span><span class="sxs-lookup"><span data-stu-id="385a2-199">The CIE committee that formulated CIECAM02 did not address the behavior of the lightness axis for input values with a luminance greater than the adopted white point; that is, for input Y values greater than the adopted white point Y value.</span></span> <span data-ttu-id="385a2-200">L’expérimentation a montré que les équations de luminance dans CIECAM02 se comportent raisonnablement pour ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="385a2-200">Experimentation has shown that the luminance equations in CIECAM02 behave reasonably for such values.</span></span> <span data-ttu-id="385a2-201">La luminosité augmente de façon exponentielle et suit le même exposant (environ 1/3).</span><span class="sxs-lookup"><span data-stu-id="385a2-201">The lightness increases exponentially and follows the same exponent (roughly 1/3).</span></span>

<span data-ttu-id="385a2-202">Les utilisateurs souhaitent parfois modifier la façon dont le degré d’adaptation (D) est calculé.</span><span class="sxs-lookup"><span data-stu-id="385a2-202">Users sometimes want to change the way that the degree of adaptation (D) is calculated.</span></span> <span data-ttu-id="385a2-203">La conception WCS permet aux utilisateurs de contrôler ce calcul en modifiant la valeur degreeOfadaptation dans les paramètres des conditions d’affichage.</span><span class="sxs-lookup"><span data-stu-id="385a2-203">The WCS design enables users to control this calculation by changing the degreeOfadaptation value in the viewing conditions parameters.</span></span>

<span data-ttu-id="385a2-204">Pour fournir une correspondance plus cohérente avec les attentes influencées par les utilisateurs, le degreeOfAdaptation dans le CAMPS par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-204">To provide a more consistent match to users' ICC-influenced expectations, the degreeOfAdaptation in the default CAMPS is 1.0.</span></span> <span data-ttu-id="385a2-205">Cela produit de meilleurs résultats dans tous les cas autres que le hachage absolu, où il peut être utile de permettre au WCS de calculer le degreeOfAdaptation (via degreeOfAdaptation =-1).</span><span class="sxs-lookup"><span data-stu-id="385a2-205">This produces better results in all cases other than MinCD Absolute, where one might want to let WCS compute the degreeOfAdaptation (via degreeOfAdaptation = -1).</span></span>

<span data-ttu-id="385a2-206">Au lieu d’utiliser une valeur surround « Average », « Dim » et « Dark », une valeur surround continue, calculée à partir de la valeur c, est fournie.</span><span class="sxs-lookup"><span data-stu-id="385a2-206">Instead of using a surround value of "Average," "Dim," and "Dark," a continuous surround value, computed from the value c, is provided.</span></span> <span data-ttu-id="385a2-207">La valeur de c doit être une valeur float comprise entre 0,525 et 0,69.</span><span class="sxs-lookup"><span data-stu-id="385a2-207">The value of c must be a float between 0.525 and 0.69.</span></span>

<span data-ttu-id="385a2-208">À partir de *c*, *NC* et *F* peuvent être calculés à l’aide d’une interpolation linéaire par morceaux entre les valeurs déjà fournies pour « Average », « Dim » et « Dark ».</span><span class="sxs-lookup"><span data-stu-id="385a2-208">From *c*, *Nc* and *F* can be computed, using piecewise linear interpolation between the values already provided for "Average," "Dim," and "Dark."</span></span> <span data-ttu-id="385a2-209">Ce modèle est illustré dans la figure 1 de la norme CIE 159:2004, la spécification CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="385a2-209">This models what is shown in Figure 1 of CIE 159:2004, the CIECAM02 specification.</span></span>



| <span data-ttu-id="385a2-210">degreeOfAdaption</span><span class="sxs-lookup"><span data-stu-id="385a2-210">degreeOfAdaption</span></span>                     | <span data-ttu-id="385a2-211">Comportement</span><span class="sxs-lookup"><span data-stu-id="385a2-211">Behavior</span></span>                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="385a2-212">-1.0</span><span class="sxs-lookup"><span data-stu-id="385a2-212">-1.0</span></span>                                 | ![Affiche une formule pour le comportement C I E C par défaut.](images/camp-image006.png)<span data-ttu-id="385a2-214">Il s’agit du comportement CIECAM02 par défaut.</span><span class="sxs-lookup"><span data-stu-id="385a2-214">This is the default CIECAM02 behavior.</span></span><br/> |
| <span data-ttu-id="385a2-215">0,0 &lt; = degreeOfAdaption &lt; = 1,0</span><span class="sxs-lookup"><span data-stu-id="385a2-215">0.0 &lt;= degreeOfAdaption &lt;= 1.0</span></span> | <span data-ttu-id="385a2-216">*D* = degreeOfAdaptation (valeur fournie par l’utilisateur)</span><span class="sxs-lookup"><span data-stu-id="385a2-216">*D* = degreeOfAdaptation (the value supplied by the user)</span></span>                      |



 

<span data-ttu-id="385a2-217">Une certaine quantité de vérification des erreurs a également été ajoutée à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="385a2-217">A certain amount of error checking has also been added to the implementation.</span></span> <span data-ttu-id="385a2-218">Les numéros d’équations suivants sont ceux utilisés dans la définition CIE 159:2004 de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="385a2-218">The following equation numbers are those used in the CIE 159:2004 definition of CIECAM02.</span></span>

<span data-ttu-id="385a2-219">**ColorimetricToAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="385a2-219">**ColorimetricToAppearanceColors**</span></span>

<span data-ttu-id="385a2-220">Les valeurs d’entrée sont vérifiées pour le caractère raisonnable : si X ou Z &lt; 0,0, ou si Y &lt; -1,0, le HRESULT est E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="385a2-220">The input values are checked for reasonableness: If X or Z &lt; 0.0, or if Y &lt; -1.0, then the HRESULT is E\_INVALIDARG.</span></span> <span data-ttu-id="385a2-221">Si-1,0 &lt; = Y &lt; 0,0, J, C et h sont tous définis sur 0,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-221">If -1.0 &lt;= Y &lt; 0.0, then J, C, and h are all set to 0.0.</span></span>

<span data-ttu-id="385a2-222">Certaines conditions internes peuvent produire des résultats d’erreur.</span><span class="sxs-lookup"><span data-stu-id="385a2-222">There are certain internal conditions that can produce error results.</span></span> <span data-ttu-id="385a2-223">Au lieu de produire de tels résultats, les résultats internes sont découpés pour produire des valeurs dans la plage.</span><span class="sxs-lookup"><span data-stu-id="385a2-223">Instead of producing such results, the internal results are clipped to produce in-range values.</span></span> <span data-ttu-id="385a2-224">Cela se produit pour les spécifications de couleurs qui seraient sombres et très probablement chromatiques : dans l’équation 7,23, si &lt; 0, a = 0.</span><span class="sxs-lookup"><span data-stu-id="385a2-224">This happens for specifications of colors that would be dark and impossibly chromatic: In equation 7.23, if A &lt; 0, A = 0.</span></span> <span data-ttu-id="385a2-225">Dans l’équation 7,26, si t &lt; 0, t = 0.</span><span class="sxs-lookup"><span data-stu-id="385a2-225">In equation 7.26, if t &lt; 0, t = 0.</span></span>

<span data-ttu-id="385a2-226">**AppearanceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="385a2-226">**AppearanceToColorimetricColors**</span></span>

<span data-ttu-id="385a2-227">Les valeurs d’entrée sont vérifiées pour obtenir un caractère raisonnable.</span><span class="sxs-lookup"><span data-stu-id="385a2-227">The input values are checked for reasonableness.</span></span> <span data-ttu-id="385a2-228">Si C &lt; 0, c &gt; 300 ou J &gt; 500, HRESULT est E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="385a2-228">If C &lt; 0 , C &gt; 300, or J &gt; 500, then the HRESULT is E\_INVALIDARG.</span></span>

<span data-ttu-id="385a2-229">*R'<sub>a ;</sub>*, *G'<sub>a</sub>*; et *B'<sub>a ;</sub>*, (les équations 8,19-8,21) sont découpés dans la plage 399,9.</span><span class="sxs-lookup"><span data-stu-id="385a2-229">*R'<sub>a;</sub>*, *G'<sub>a;</sub>*, and *B'<sub>a;</sub>*, (equations 8.19 - 8.21) are clipped to the range   399.9 .</span></span>

<span data-ttu-id="385a2-230">Pour tous les profils de modèle d’apparence des couleurs (CAMPs), le moteur WCS examine le point blanc adopté.</span><span class="sxs-lookup"><span data-stu-id="385a2-230">For all Color Appearance Model Profiles (CAMPs), the WCS engine will examine the adopted white point.</span></span> <span data-ttu-id="385a2-231">Si Y n’est pas 100,0, le point blanc adopté est mis à l’échelle afin que Y soit égal à 100,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-231">If Y is not 100.0, then the adopted white point will be scaled so that Y does equal 100.0.</span></span> <span data-ttu-id="385a2-232">La même mise à l’échelle sera appliquée à la valeur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="385a2-232">The same scaling will be applied to the background value.</span></span> <span data-ttu-id="385a2-233">Le facteur d’échelle est 100,0/adoptedWhitePoint. Y.</span><span class="sxs-lookup"><span data-stu-id="385a2-233">The scaling factor is 100.0/adoptedWhitePoint.Y.</span></span> <span data-ttu-id="385a2-234">Le même facteur d’échelle est appliqué à chacun des X, Y et Z. Si le champ NormalizeToMediaWhitePoint est défini sur « true » ou s’il est absent du CAMP, le moteur met également à l’échelle toutes les couleurs de l’appareil vers DeviceToColorimetric afin que la valeur Y du point blanc du média de l’appareil soit égale à 100,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-234">The same scaling factor is applied to each of X, Y, and Z. If the NormalizeToMediaWhitePoint field is set to "True," or if it is absent from the CAMP, the engine also scales all device colors input to DeviceToColorimetric so that the Y value of the device media white point equals 100.0.</span></span> <span data-ttu-id="385a2-235">Les couleurs de l’appareil provenant de ColorimetricToDevice seront mises à l’échelle par l’inverse multiplicatif de ce facteur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="385a2-235">Device colors coming from ColorimetricToDevice will be scaled by the multiplicative inverse of that scaling factor.</span></span> <span data-ttu-id="385a2-236">Si l’indicateur NormalizeToMediaWhitePoint a la valeur « false », les données de colorimétrie ne sont pas mises à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="385a2-236">If the NormalizeToMediaWhitePoint flag is set to "False," then the colorimetric data is not scaled.</span></span>

<span data-ttu-id="385a2-237">Pour certaines tâches, il est logique de mettre à l’échelle les valeurs colorimétriques provenant de DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="385a2-237">For some tasks, it makes sense to scale the colorimetric values coming from DeviceToColorimetric.</span></span> <span data-ttu-id="385a2-238">Les équations de luminosité hyperbolique dans le CAM sont vraiment conçues pour une luminance de point blanc de 100,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-238">The hyperbolic lightness equations in the CAM are really designed for a white point luminance of 100.0.</span></span> <span data-ttu-id="385a2-239">Le seul endroit où une différence dans la luminance absolue (ou éclairage) entre en lecture est dans la luminance du champ d’adaptation.</span><span class="sxs-lookup"><span data-stu-id="385a2-239">The only place where a difference in the absolute luminance (or illuminance) comes into play is in the luminance of the adapting field.</span></span> <span data-ttu-id="385a2-240">La came doit donc être initialisée avec un point blanc Y de 100,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-240">So the CAM must be initialized with a white point Y of 100.0.</span></span> <span data-ttu-id="385a2-241">Mais si le point blanc moyen du modèle de périphérique est utilisé comme point blanc adopté, toutes les couleurs provenant de l’appareil doivent être mises à l’échelle en conséquence, ou le périphérique blanc ne sera pas fourni avec une valeur J de 100,0.</span><span class="sxs-lookup"><span data-stu-id="385a2-241">But if the device model's medium white point is being used as the adopted white point, then all colors coming from the device must be scaled accordingly, or device white will not come out with a J value of 100.0.</span></span> <span data-ttu-id="385a2-242">Par conséquent, les valeurs Y doivent être mises à l’échelle dans les mesures.</span><span class="sxs-lookup"><span data-stu-id="385a2-242">So the Y values have to be scaled in the measurements.</span></span> <span data-ttu-id="385a2-243">Les valeurs de mesure peuvent être mises à l’échelle avant d’initialiser le modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="385a2-243">The measurement values could be scaled before initializing the device model.</span></span> <span data-ttu-id="385a2-244">Les résultats se trouvent déjà dans la plage appropriée.</span><span class="sxs-lookup"><span data-stu-id="385a2-244">Then results would already be in the proper range.</span></span> <span data-ttu-id="385a2-245">Mais cela rendrait le test du modèle d’appareil plus difficile, car les valeurs sortantes nécessitent une mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="385a2-245">But that would make testing the device model more difficult, because the values coming out would require scaling.</span></span> <span data-ttu-id="385a2-246">Pour les tâches dans lesquelles le point blanc moyen de l’appareil est perçu comme un vrai blanc, la normalisation par le média de l’appareil est souhaitable.</span><span class="sxs-lookup"><span data-stu-id="385a2-246">For tasks in which the device medium white point is perceived to be a true white, normalizing by the device media white point is desirable.</span></span>

<span data-ttu-id="385a2-247">La came est initialisée directement à partir du CAMP.</span><span class="sxs-lookup"><span data-stu-id="385a2-247">The CAM is initialized directly from the CAMP.</span></span> <span data-ttu-id="385a2-248">Cela permet aux développeurs de bénéficier d’une certaine flexibilité dans l’initialisation du CAM, en fonction de la tâche qu’ils souhaitent effectuer.</span><span class="sxs-lookup"><span data-stu-id="385a2-248">This allows developers some flexibility in initializing the CAM, based upon the task they want to perform.</span></span> <span data-ttu-id="385a2-249">Dans certaines tâches, les observateurs ignorent tout Chroma dans les points blancs des médias, car ils « savent » de façon cognitive que les supports source et de destination sont « blancs ».</span><span class="sxs-lookup"><span data-stu-id="385a2-249">In some tasks, observers will ignore any chroma in the media white points, because they cognitively "know" that the source and destination media are "white."</span></span> <span data-ttu-id="385a2-250">Dans ce cas, les développeurs veulent initialiser les cames avant et inverse avec leurs points blancs de média respectifs.</span><span class="sxs-lookup"><span data-stu-id="385a2-250">In such cases, developers will want to initialize the forward and inverse CAMs with their respective media white points.</span></span> <span data-ttu-id="385a2-251">Dans certains cas, les observateurs peuvent comparer la couleur des arrière-plans du support.</span><span class="sxs-lookup"><span data-stu-id="385a2-251">In some cases, observers may be comparing the color of the media backgrounds.</span></span> <span data-ttu-id="385a2-252">Dans ces cas-là, il est recommandé d’utiliser un CAM pour les deux appareils, et il peut être souhaitable de ne pas mettre à l’échelle les valeurs de colorimétrie de chaque appareil par le point blanc moyen de ce périphérique.</span><span class="sxs-lookup"><span data-stu-id="385a2-252">In these cases, it is advisable to use one CAM for both devices, and it may be desirable not to scale each device's colorimetric values by that device's medium white point.</span></span> <span data-ttu-id="385a2-253">Les différentes valeurs de tristimulus du média aboutissent à des valeurs d’apparence différentes dans CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="385a2-253">Then the different tristimulus values of the media will lead to different appearance values in CIECAM02.</span></span>

## <a name="related-topics"></a><span data-ttu-id="385a2-254">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="385a2-254">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="385a2-255">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="385a2-255">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="385a2-256">Schémas et algorithmes du système de couleurs Windows</span><span class="sxs-lookup"><span data-stu-id="385a2-256">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 






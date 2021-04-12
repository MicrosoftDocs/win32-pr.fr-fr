---
description: Pour plus d’informations sur les attributs de contrôle, consultez le lien vers le contrôle particulier que vous devez créer dans les contrôles, ainsi que les liens vers des attributs de contrôle particuliers dans les listes suivantes.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Attributs du contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320093"
---
# <a name="control-attributes"></a><span data-ttu-id="6759d-103">Attributs du contrôle</span><span class="sxs-lookup"><span data-stu-id="6759d-103">Control Attributes</span></span>

<span data-ttu-id="6759d-104">Pour plus d’informations sur les attributs de contrôle, consultez le lien vers le contrôle particulier que vous devez créer dans les [contrôles](controls.md) , ainsi que les liens vers des attributs de contrôle particuliers dans les listes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6759d-104">For information on control attributes, see the link to the particular control that you need to create in [Controls](controls.md) as well as the links to particular control attributes in the following lists.</span></span>

<span data-ttu-id="6759d-105">Les méthodes suivantes sont utilisées pour spécifier les attributs d’un contrôle :</span><span class="sxs-lookup"><span data-stu-id="6759d-105">The following methods are used for specifying the attributes of a control:</span></span>

-   <span data-ttu-id="6759d-106">Utilisez la [table ControlCondition](controlcondition-table.md) pour désactiver, activer, masquer ou afficher un contrôle en fonction de la valeur d’une propriété ou d’une instruction conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="6759d-106">Use the [ControlCondition table](controlcondition-table.md) to disable, enable, hide, or show a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="6759d-107">Vous pouvez également utiliser ce tableau pour remplacer le contrôle par défaut spécifié dans la [table de boîtes de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="6759d-107">You can also use this table to override the default control specified in the [Dialog table](dialog-table.md).</span></span>
-   <span data-ttu-id="6759d-108">Abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="6759d-108">Subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="6759d-109">Entrez l’identificateur de l’attribut dans la colonne d’attribut et l’identificateur de ControlEvent, dans la colonne d’événement de cette table.</span><span class="sxs-lookup"><span data-stu-id="6759d-109">Enter the attribute's identifier in the Attribute column and the ControlEvent's identifier in the Event column of this table.</span></span>
-   <span data-ttu-id="6759d-110">Définissez les indicateurs de bits d’attribut de contrôle pour le contrôle dans la colonne attribut de la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="6759d-110">Set the control attribute bit flags for the control in the Attribute column of the [Control table](control-table.md).</span></span> <span data-ttu-id="6759d-111">Cela définit les attributs lors de la création du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6759d-111">This sets the attributes upon the creation of the control.</span></span>

<span data-ttu-id="6759d-112">Certains attributs ne peuvent pas être définis pour chaque contrôle ou être spécifiés par toutes les méthodes ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="6759d-112">Some attributes cannot be set for every control or be specified by all of the above methods.</span></span> <span data-ttu-id="6759d-113">Pour plus d’informations, consultez les rubriques de contrôle et d’attribut spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6759d-113">See the particular control and attribute topics for details.</span></span>

<span data-ttu-id="6759d-114">Les valeurs initiales de certains attributs de contrôle peuvent être définies avec des bits dans la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="6759d-114">The initial values of some control attributes can be set with bits in the [Control table](control-table.md).</span></span>



| <span data-ttu-id="6759d-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-115">Attribute</span></span>                                          | <span data-ttu-id="6759d-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-116">Decimal</span></span> | <span data-ttu-id="6759d-117">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-117">Hexadecimal</span></span> | <span data-ttu-id="6759d-118">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-118">Constant</span></span>                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [<span data-ttu-id="6759d-119">BiDi</span><span class="sxs-lookup"><span data-stu-id="6759d-119">BiDi</span></span>](bidi-control-attribute.md)                 | <span data-ttu-id="6759d-120">224</span><span class="sxs-lookup"><span data-stu-id="6759d-120">224</span></span>     | <span data-ttu-id="6759d-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="6759d-121">0x000000E0</span></span>  | <span data-ttu-id="6759d-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="6759d-122">**msidbControlAttributesBiDi**</span></span>         |
| [<span data-ttu-id="6759d-123">Enabled</span><span class="sxs-lookup"><span data-stu-id="6759d-123">Enabled</span></span>](enabled-control-attribute.md)           | <span data-ttu-id="6759d-124">2</span><span class="sxs-lookup"><span data-stu-id="6759d-124">2</span></span>       | <span data-ttu-id="6759d-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6759d-125">0x00000002</span></span>  | <span data-ttu-id="6759d-126">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="6759d-126">**msidbControlAttributesEnabled**</span></span>      |
| [<span data-ttu-id="6759d-127">Indirect</span><span class="sxs-lookup"><span data-stu-id="6759d-127">Indirect</span></span>](indirect-control-attribute.md)         | <span data-ttu-id="6759d-128">8</span><span class="sxs-lookup"><span data-stu-id="6759d-128">8</span></span>       | <span data-ttu-id="6759d-129">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6759d-129">0x00000008</span></span>  | <span data-ttu-id="6759d-130">**msidbControlAttributesIndirect**</span><span class="sxs-lookup"><span data-stu-id="6759d-130">**msidbControlAttributesIndirect**</span></span>     |
| [<span data-ttu-id="6759d-131">Contrôle entier</span><span class="sxs-lookup"><span data-stu-id="6759d-131">Integer Control</span></span>](integer-control-attribute.md)   | <span data-ttu-id="6759d-132">16</span><span class="sxs-lookup"><span data-stu-id="6759d-132">16</span></span>      | <span data-ttu-id="6759d-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6759d-133">0x00000010</span></span>  | <span data-ttu-id="6759d-134">**msidbControlAttributesInteger**</span><span class="sxs-lookup"><span data-stu-id="6759d-134">**msidbControlAttributesInteger**</span></span>      |
| [<span data-ttu-id="6759d-135">LeftScroll</span><span class="sxs-lookup"><span data-stu-id="6759d-135">LeftScroll</span></span>](leftscroll-control-attribute.md)     | <span data-ttu-id="6759d-136">128</span><span class="sxs-lookup"><span data-stu-id="6759d-136">128</span></span>     | <span data-ttu-id="6759d-137">0x00000080</span><span class="sxs-lookup"><span data-stu-id="6759d-137">0x00000080</span></span>  | <span data-ttu-id="6759d-138">**msidbControlAttributesLeftScroll**</span><span class="sxs-lookup"><span data-stu-id="6759d-138">**msidbControlAttributesLeftScroll**</span></span>   |
| [<span data-ttu-id="6759d-139">RightAligned</span><span class="sxs-lookup"><span data-stu-id="6759d-139">RightAligned</span></span>](rightaligned-control-attribute.md) | <span data-ttu-id="6759d-140">64</span><span class="sxs-lookup"><span data-stu-id="6759d-140">64</span></span>      | <span data-ttu-id="6759d-141">0x00000040</span><span class="sxs-lookup"><span data-stu-id="6759d-141">0x00000040</span></span>  | <span data-ttu-id="6759d-142">**msidbControlAttributesRightAligned**</span><span class="sxs-lookup"><span data-stu-id="6759d-142">**msidbControlAttributesRightAligned**</span></span> |
| [<span data-ttu-id="6759d-143">RTLRO</span><span class="sxs-lookup"><span data-stu-id="6759d-143">RTLRO</span></span>](rtlro-control-attribute.md)               | <span data-ttu-id="6759d-144">32</span><span class="sxs-lookup"><span data-stu-id="6759d-144">32</span></span>      | <span data-ttu-id="6759d-145">0x00000020</span><span class="sxs-lookup"><span data-stu-id="6759d-145">0x00000020</span></span>  | <span data-ttu-id="6759d-146">**msidbControlAttributesRTLRO**</span><span class="sxs-lookup"><span data-stu-id="6759d-146">**msidbControlAttributesRTLRO**</span></span>        |
| [<span data-ttu-id="6759d-147">Sunken</span><span class="sxs-lookup"><span data-stu-id="6759d-147">Sunken</span></span>](sunken-control-attribute.md)             | <span data-ttu-id="6759d-148">4</span><span class="sxs-lookup"><span data-stu-id="6759d-148">4</span></span>       | <span data-ttu-id="6759d-149">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6759d-149">0x00000004</span></span>  | <span data-ttu-id="6759d-150">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="6759d-150">**msidbControlAttributesSunken**</span></span>       |
| [<span data-ttu-id="6759d-151">Visible</span><span class="sxs-lookup"><span data-stu-id="6759d-151">Visible</span></span>](visible-control-attribute.md)           | <span data-ttu-id="6759d-152">1</span><span class="sxs-lookup"><span data-stu-id="6759d-152">1</span></span>       | <span data-ttu-id="6759d-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6759d-153">0x00000001</span></span>  | <span data-ttu-id="6759d-154">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="6759d-154">**msidbControlAttributesVisible**</span></span>      |



 

<span data-ttu-id="6759d-155">Ces attributs de contrôles de texte sont définis avec bits.</span><span class="sxs-lookup"><span data-stu-id="6759d-155">These attributes of Text controls are set with bits.</span></span>



| <span data-ttu-id="6759d-156">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-156">Attribute</span></span>                                            | <span data-ttu-id="6759d-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-157">Decimal</span></span> | <span data-ttu-id="6759d-158">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-158">Hexadecimal</span></span> | <span data-ttu-id="6759d-159">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-159">Constant</span></span>                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [<span data-ttu-id="6759d-160">Formatage</span><span class="sxs-lookup"><span data-stu-id="6759d-160">FormatSize</span></span>](formatsize-control-attribute.md)       | <span data-ttu-id="6759d-161">524 288</span><span class="sxs-lookup"><span data-stu-id="6759d-161">524288</span></span>  | <span data-ttu-id="6759d-162">0x00080000</span><span class="sxs-lookup"><span data-stu-id="6759d-162">0x00080000</span></span>  | <span data-ttu-id="6759d-163">**msidbControlAttributesFormatSize**</span><span class="sxs-lookup"><span data-stu-id="6759d-163">**msidbControlAttributesFormatSize**</span></span>    |
| [<span data-ttu-id="6759d-164">Préfixe</span><span class="sxs-lookup"><span data-stu-id="6759d-164">NoPrefix</span></span>](noprefix-control-attribute.md)           | <span data-ttu-id="6759d-165">131 072</span><span class="sxs-lookup"><span data-stu-id="6759d-165">131072</span></span>  | <span data-ttu-id="6759d-166">0x00020000</span><span class="sxs-lookup"><span data-stu-id="6759d-166">0x00020000</span></span>  | <span data-ttu-id="6759d-167">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="6759d-167">**msidbControlAttributesNoPrefix**</span></span>      |
| [<span data-ttu-id="6759d-168">NoWrap</span><span class="sxs-lookup"><span data-stu-id="6759d-168">NoWrap</span></span>](nowrap-control-attribute.md)               | <span data-ttu-id="6759d-169">262 144</span><span class="sxs-lookup"><span data-stu-id="6759d-169">262144</span></span>  | <span data-ttu-id="6759d-170">0x00040000</span><span class="sxs-lookup"><span data-stu-id="6759d-170">0x00040000</span></span>  | <span data-ttu-id="6759d-171">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="6759d-171">**msidbControlAttributesNoWrap**</span></span>        |
| [<span data-ttu-id="6759d-172">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="6759d-172">Password</span></span>](password-control-attribute.md)           | <span data-ttu-id="6759d-173">2 097 152</span><span class="sxs-lookup"><span data-stu-id="6759d-173">2097152</span></span> | <span data-ttu-id="6759d-174">0x00200000</span><span class="sxs-lookup"><span data-stu-id="6759d-174">0x00200000</span></span>  | <span data-ttu-id="6759d-175">**msidbControlAttributesPasswordInput**</span><span class="sxs-lookup"><span data-stu-id="6759d-175">**msidbControlAttributesPasswordInput**</span></span> |
| [<span data-ttu-id="6759d-176">Transparent</span><span class="sxs-lookup"><span data-stu-id="6759d-176">Transparent</span></span>](transparent-control-attribute.md)     | <span data-ttu-id="6759d-177">65536</span><span class="sxs-lookup"><span data-stu-id="6759d-177">65536</span></span>   | <span data-ttu-id="6759d-178">0x00010000</span><span class="sxs-lookup"><span data-stu-id="6759d-178">0x00010000</span></span>  | <span data-ttu-id="6759d-179">**msidbControlAttributesTransparent**</span><span class="sxs-lookup"><span data-stu-id="6759d-179">**msidbControlAttributesTransparent**</span></span>   |
| [<span data-ttu-id="6759d-180">UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="6759d-180">UsersLanguage</span></span>](userslanguage-control-attribute.md) | <span data-ttu-id="6759d-181">1 048 576</span><span class="sxs-lookup"><span data-stu-id="6759d-181">1048576</span></span> | <span data-ttu-id="6759d-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="6759d-182">0x00100000</span></span>  | <span data-ttu-id="6759d-183">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="6759d-183">**msidbControlAttributesUsersLanguage**</span></span> |



 

<span data-ttu-id="6759d-184">Cet attribut du contrôle ProgressBar est défini avec un bit.</span><span class="sxs-lookup"><span data-stu-id="6759d-184">This attribute of the ProgressBar control is set with a bit.</span></span>



| <span data-ttu-id="6759d-185">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-185">Attribute</span></span>                                      | <span data-ttu-id="6759d-186">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-186">Decimal</span></span> | <span data-ttu-id="6759d-187">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-187">Hexadecimal</span></span> | <span data-ttu-id="6759d-188">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-188">Constant</span></span>                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="6759d-189">Progress95</span><span class="sxs-lookup"><span data-stu-id="6759d-189">Progress95</span></span>](progress95-control-attribute.md) | <span data-ttu-id="6759d-190">65536</span><span class="sxs-lookup"><span data-stu-id="6759d-190">65536</span></span>   | <span data-ttu-id="6759d-191">0x00010000</span><span class="sxs-lookup"><span data-stu-id="6759d-191">0x00010000</span></span>  | <span data-ttu-id="6759d-192">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="6759d-192">**msidbControlAttributesProgress95**</span></span> |



 

<span data-ttu-id="6759d-193">Ces attributs des contrôles SelectCombo des volumes et des répertoires sont définis avec bits.</span><span class="sxs-lookup"><span data-stu-id="6759d-193">These attributes of Volume and Directory SelectCombo controls are set with bits.</span></span>



| <span data-ttu-id="6759d-194">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-194">Attribute</span></span>                                                | <span data-ttu-id="6759d-195">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-195">Decimal</span></span> | <span data-ttu-id="6759d-196">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-196">Hexadecimal</span></span> | <span data-ttu-id="6759d-197">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-197">Constant</span></span>                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="6759d-198">CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="6759d-198">CDROMVolume</span></span>](cdromvolume-control-attribute.md)         | <span data-ttu-id="6759d-199">524 288</span><span class="sxs-lookup"><span data-stu-id="6759d-199">524288</span></span>  | <span data-ttu-id="6759d-200">0x00080000</span><span class="sxs-lookup"><span data-stu-id="6759d-200">0x00080000</span></span>  | <span data-ttu-id="6759d-201">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="6759d-201">**msidbControlAttributesCDROMVolume**</span></span>     |
| [<span data-ttu-id="6759d-202">FixedVolume</span><span class="sxs-lookup"><span data-stu-id="6759d-202">FixedVolume</span></span>](fixedvolume-control-attribute.md)         | <span data-ttu-id="6759d-203">131 072</span><span class="sxs-lookup"><span data-stu-id="6759d-203">131072</span></span>  | <span data-ttu-id="6759d-204">0x00020000</span><span class="sxs-lookup"><span data-stu-id="6759d-204">0x00020000</span></span>  | <span data-ttu-id="6759d-205">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="6759d-205">**msidbControlAttributesFixedVolume**</span></span>     |
| [<span data-ttu-id="6759d-206">FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="6759d-206">FloppyVolume</span></span>](floppyvolume-control-attribute.md)       | <span data-ttu-id="6759d-207">2 097 152</span><span class="sxs-lookup"><span data-stu-id="6759d-207">2097152</span></span> | <span data-ttu-id="6759d-208">0x00200000</span><span class="sxs-lookup"><span data-stu-id="6759d-208">0x00200000</span></span>  | <span data-ttu-id="6759d-209">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="6759d-209">**msidbControlAttributesFloppyVolume**</span></span>    |
| [<span data-ttu-id="6759d-210">RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="6759d-210">RAMDiskVolume</span></span>](ramdiskvolume-control-attribute.md)     | <span data-ttu-id="6759d-211">1 048 576</span><span class="sxs-lookup"><span data-stu-id="6759d-211">1048576</span></span> | <span data-ttu-id="6759d-212">0x00100000</span><span class="sxs-lookup"><span data-stu-id="6759d-212">0x00100000</span></span>  | <span data-ttu-id="6759d-213">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="6759d-213">**msidbControlAttributesRAMDiskVolume**</span></span>   |
| [<span data-ttu-id="6759d-214">RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="6759d-214">RemoteVolume</span></span>](remotevolume-control-attribute.md)       | <span data-ttu-id="6759d-215">262 144</span><span class="sxs-lookup"><span data-stu-id="6759d-215">262144</span></span>  | <span data-ttu-id="6759d-216">0x00040000</span><span class="sxs-lookup"><span data-stu-id="6759d-216">0x00040000</span></span>  | <span data-ttu-id="6759d-217">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="6759d-217">**msidbControlAttributesRemoteVolume**</span></span>    |
| [<span data-ttu-id="6759d-218">RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="6759d-218">RemovableVolume</span></span>](removablevolume-control-attribute.md) | <span data-ttu-id="6759d-219">65536</span><span class="sxs-lookup"><span data-stu-id="6759d-219">65536</span></span>   | <span data-ttu-id="6759d-220">0x00010000</span><span class="sxs-lookup"><span data-stu-id="6759d-220">0x00010000</span></span>  | <span data-ttu-id="6759d-221">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="6759d-221">**msidbControlAttributesRemovableVolume**</span></span> |



 

<span data-ttu-id="6759d-222">Ces attributs des contrôles ListBox et ComboBox sont définis avec bits.</span><span class="sxs-lookup"><span data-stu-id="6759d-222">These attributes of ListBox and ComboBox controls are set with bits.</span></span>



| <span data-ttu-id="6759d-223">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-223">Attribute</span></span>                                            | <span data-ttu-id="6759d-224">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-224">Decimal</span></span> | <span data-ttu-id="6759d-225">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-225">Hexadecimal</span></span> | <span data-ttu-id="6759d-226">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-226">Constant</span></span>                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="6759d-227">Contrôle ComboList</span><span class="sxs-lookup"><span data-stu-id="6759d-227">ComboList Control</span></span>](combolist-control-attribute.md) | <span data-ttu-id="6759d-228">131 072</span><span class="sxs-lookup"><span data-stu-id="6759d-228">131072</span></span>  | <span data-ttu-id="6759d-229">0x00020000</span><span class="sxs-lookup"><span data-stu-id="6759d-229">0x00020000</span></span>  | <span data-ttu-id="6759d-230">**msidbControlAttributesComboList**</span><span class="sxs-lookup"><span data-stu-id="6759d-230">**msidbControlAttributesComboList**</span></span> |
| [<span data-ttu-id="6759d-231">Contrôle trié</span><span class="sxs-lookup"><span data-stu-id="6759d-231">Sorted Control</span></span>](sorted-control-attribute.md)       | <span data-ttu-id="6759d-232">65536</span><span class="sxs-lookup"><span data-stu-id="6759d-232">65536</span></span>   | <span data-ttu-id="6759d-233">0x00010000</span><span class="sxs-lookup"><span data-stu-id="6759d-233">0x00010000</span></span>  | <span data-ttu-id="6759d-234">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="6759d-234">**msidbControlAttributesSorted**</span></span>    |



 

<span data-ttu-id="6759d-235">Cet attribut du contrôle d’édition est défini avec un bit.</span><span class="sxs-lookup"><span data-stu-id="6759d-235">This attribute of the Edit control is set with a bit.</span></span>



| <span data-ttu-id="6759d-236">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-236">Attribute</span></span>                                    | <span data-ttu-id="6759d-237">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-237">Decimal</span></span> | <span data-ttu-id="6759d-238">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-238">Hexadecimal</span></span> | <span data-ttu-id="6759d-239">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-239">Constant</span></span>                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="6759d-240">Lambda</span><span class="sxs-lookup"><span data-stu-id="6759d-240">MultiLine</span></span>](multiline-control-attribute.md) | <span data-ttu-id="6759d-241">65536</span><span class="sxs-lookup"><span data-stu-id="6759d-241">65536</span></span>   | <span data-ttu-id="6759d-242">0x00010000</span><span class="sxs-lookup"><span data-stu-id="6759d-242">0x00010000</span></span>  | <span data-ttu-id="6759d-243">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="6759d-243">**msidbControlAttributesMultiline**</span></span> |



 

<span data-ttu-id="6759d-244">Ces attributs des contrôles PictureButton sont définis avec bits.</span><span class="sxs-lookup"><span data-stu-id="6759d-244">These attributes of PictureButton controls are set with bits.</span></span>



| <span data-ttu-id="6759d-245">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-245">Attribute</span></span>                                          | <span data-ttu-id="6759d-246">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-246">Decimal</span></span> | <span data-ttu-id="6759d-247">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-247">Hexadecimal</span></span> | <span data-ttu-id="6759d-248">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-248">Constant</span></span>                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="6759d-249">Bitmap</span><span class="sxs-lookup"><span data-stu-id="6759d-249">Bitmap</span></span>](bitmap-control-attribute.md)             | <span data-ttu-id="6759d-250">262 144</span><span class="sxs-lookup"><span data-stu-id="6759d-250">262144</span></span>  | <span data-ttu-id="6759d-251">0x00040000</span><span class="sxs-lookup"><span data-stu-id="6759d-251">0x00040000</span></span>  | <span data-ttu-id="6759d-252">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="6759d-252">**msidbControlAttributesBitmap**</span></span>     |
| [<span data-ttu-id="6759d-253">FixedSize</span><span class="sxs-lookup"><span data-stu-id="6759d-253">FixedSize</span></span>](fixedsize-control-attribute.md)       | <span data-ttu-id="6759d-254">1 048 576</span><span class="sxs-lookup"><span data-stu-id="6759d-254">1048576</span></span> | <span data-ttu-id="6759d-255">0x00100000</span><span class="sxs-lookup"><span data-stu-id="6759d-255">0x00100000</span></span>  | <span data-ttu-id="6759d-256">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="6759d-256">**msidbControlAttributesFixedSize**</span></span>  |
| [<span data-ttu-id="6759d-257">Icône</span><span class="sxs-lookup"><span data-stu-id="6759d-257">Icon</span></span>](icon-control-attribute.md)                 | <span data-ttu-id="6759d-258">524 288</span><span class="sxs-lookup"><span data-stu-id="6759d-258">524288</span></span>  | <span data-ttu-id="6759d-259">0x00080000</span><span class="sxs-lookup"><span data-stu-id="6759d-259">0x00080000</span></span>  | <span data-ttu-id="6759d-260">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="6759d-260">**msidbControlAttributesIcon**</span></span>       |
| [<span data-ttu-id="6759d-261">IconSize16</span><span class="sxs-lookup"><span data-stu-id="6759d-261">IconSize16</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="6759d-262">2 097 152</span><span class="sxs-lookup"><span data-stu-id="6759d-262">2097152</span></span> | <span data-ttu-id="6759d-263">0x00200000</span><span class="sxs-lookup"><span data-stu-id="6759d-263">0x00200000</span></span>  | <span data-ttu-id="6759d-264">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="6759d-264">**msidbControlAttributesIconSize16**</span></span> |
| [<span data-ttu-id="6759d-265">IconSize32</span><span class="sxs-lookup"><span data-stu-id="6759d-265">IconSize32</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="6759d-266">4 194 304</span><span class="sxs-lookup"><span data-stu-id="6759d-266">4194304</span></span> | <span data-ttu-id="6759d-267">0x00400000</span><span class="sxs-lookup"><span data-stu-id="6759d-267">0x00400000</span></span>  | <span data-ttu-id="6759d-268">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="6759d-268">**msidbControlAttributesIconSize32**</span></span> |
| [<span data-ttu-id="6759d-269">IconSize48</span><span class="sxs-lookup"><span data-stu-id="6759d-269">IconSize48</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="6759d-270">6291456</span><span class="sxs-lookup"><span data-stu-id="6759d-270">6291456</span></span> | <span data-ttu-id="6759d-271">0x00600000</span><span class="sxs-lookup"><span data-stu-id="6759d-271">0x00600000</span></span>  | <span data-ttu-id="6759d-272">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="6759d-272">**msidbControlAttributesIconSize48**</span></span> |
| [<span data-ttu-id="6759d-273">Contrôle PushLike</span><span class="sxs-lookup"><span data-stu-id="6759d-273">PushLike Control</span></span>](pushlike-control-attribute.md) | <span data-ttu-id="6759d-274">131 072</span><span class="sxs-lookup"><span data-stu-id="6759d-274">131072</span></span>  | <span data-ttu-id="6759d-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="6759d-275">0x00020000</span></span>  | <span data-ttu-id="6759d-276">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="6759d-276">**msidbControlAttributesPushLike**</span></span>   |



 

<span data-ttu-id="6759d-277">Cet attribut du contrôle RadioButton est défini avec un bit.</span><span class="sxs-lookup"><span data-stu-id="6759d-277">This attribute of RadioButton control is set with a bit.</span></span>



| <span data-ttu-id="6759d-278">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-278">Attribute</span></span>                                    | <span data-ttu-id="6759d-279">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-279">Decimal</span></span>  | <span data-ttu-id="6759d-280">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-280">Hexadecimal</span></span> | <span data-ttu-id="6759d-281">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-281">Constant</span></span>                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [<span data-ttu-id="6759d-282">HasBorder</span><span class="sxs-lookup"><span data-stu-id="6759d-282">HasBorder</span></span>](hasborder-control-attribute.md) | <span data-ttu-id="6759d-283">16 777 216</span><span class="sxs-lookup"><span data-stu-id="6759d-283">16777216</span></span> | <span data-ttu-id="6759d-284">0x01000000</span><span class="sxs-lookup"><span data-stu-id="6759d-284">0x01000000</span></span>  | <span data-ttu-id="6759d-285">**msidbControlAttributesHasBorder**</span><span class="sxs-lookup"><span data-stu-id="6759d-285">**msidbControlAttributesHasBorder**</span></span> |



 

<span data-ttu-id="6759d-286">Cet attribut du contrôle PushButton est défini avec un bit.</span><span class="sxs-lookup"><span data-stu-id="6759d-286">This attribute of PushButton control is set with a bit.</span></span>



| <span data-ttu-id="6759d-287">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-287">Attribute</span></span>                                        | <span data-ttu-id="6759d-288">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-288">Decimal</span></span> | <span data-ttu-id="6759d-289">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-289">Hexadecimal</span></span> | <span data-ttu-id="6759d-290">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-290">Constant</span></span>                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="6759d-291">ElevationShield</span><span class="sxs-lookup"><span data-stu-id="6759d-291">ElevationShield</span></span>](elevationshield-attribute.md) | <span data-ttu-id="6759d-292">8388608</span><span class="sxs-lookup"><span data-stu-id="6759d-292">8388608</span></span> | <span data-ttu-id="6759d-293">0x00800000</span><span class="sxs-lookup"><span data-stu-id="6759d-293">0x00800000</span></span>  | <span data-ttu-id="6759d-294">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="6759d-294">**msidbControlAttributesElevationShield**</span></span> |



 

<span data-ttu-id="6759d-295">Cet attribut du contrôle VolumeCostList est défini sur un bit.</span><span class="sxs-lookup"><span data-stu-id="6759d-295">This attribute of VolumeCostList control is set with a bit.</span></span>



| <span data-ttu-id="6759d-296">Attribut</span><span class="sxs-lookup"><span data-stu-id="6759d-296">Attribute</span></span>                                                                | <span data-ttu-id="6759d-297">Decimal</span><span class="sxs-lookup"><span data-stu-id="6759d-297">Decimal</span></span> | <span data-ttu-id="6759d-298">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6759d-298">Hexadecimal</span></span> | <span data-ttu-id="6759d-299">Constante</span><span class="sxs-lookup"><span data-stu-id="6759d-299">Constant</span></span>                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [<span data-ttu-id="6759d-300">ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="6759d-300">ControlShowRollbackCost</span></span>](controlshowrollbackcost-control-attribute.md) | <span data-ttu-id="6759d-301">4 194 304</span><span class="sxs-lookup"><span data-stu-id="6759d-301">4194304</span></span> | <span data-ttu-id="6759d-302">0x00400000</span><span class="sxs-lookup"><span data-stu-id="6759d-302">0x00400000</span></span>  | <span data-ttu-id="6759d-303">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="6759d-303">**msidbControlShowRollbackCost**</span></span> |



 

<span data-ttu-id="6759d-304">Les attributs de contrôle suivants ne sont pas définis avec bits.</span><span class="sxs-lookup"><span data-stu-id="6759d-304">The following control attributes are not set with bits.</span></span> <span data-ttu-id="6759d-305">Ces attributs sont créés dans les tables de l’interface utilisateur ou sont définis à l’aide d' [événements de contrôle](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="6759d-305">These attributes are authored into the user interface tables or are set using [Control Events](control-events.md).</span></span>

[<span data-ttu-id="6759d-306">BillboardName</span><span class="sxs-lookup"><span data-stu-id="6759d-306">BillboardName</span></span>](billboardname-control-attribute.md)

 

[<span data-ttu-id="6759d-307">IndirectPropertyName</span><span class="sxs-lookup"><span data-stu-id="6759d-307">IndirectPropertyName</span></span>](indirectpropertyname-control-attribute.md)

 

[<span data-ttu-id="6759d-308">Position</span><span class="sxs-lookup"><span data-stu-id="6759d-308">Position</span></span>](position-control-attribute.md)

 

[<span data-ttu-id="6759d-309">Contrôle de progression</span><span class="sxs-lookup"><span data-stu-id="6759d-309">Progress Control</span></span>](progress-control-attribute.md)

 

[<span data-ttu-id="6759d-310">PropertyName</span><span class="sxs-lookup"><span data-stu-id="6759d-310">PropertyName</span></span>](propertyname-control-attribute.md)

 

[<span data-ttu-id="6759d-311">PropertyValue</span><span class="sxs-lookup"><span data-stu-id="6759d-311">PropertyValue</span></span>](propertyvalue-control-attribute.md)

 

[<span data-ttu-id="6759d-312">Text Control</span><span class="sxs-lookup"><span data-stu-id="6759d-312">Text Control</span></span>](text-control-attribute.md)

 

[<span data-ttu-id="6759d-313">TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="6759d-313">TimeRemaining</span></span>](timeremaining-control-attribute.md)

<span data-ttu-id="6759d-314">Consultez [Ajout de contrôles et de texte](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="6759d-314">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

 

 




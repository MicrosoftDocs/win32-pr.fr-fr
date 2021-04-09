---
description: Avec Windows Vista, l’arborescence des éléments de l’acquisition d’images Windows (WIA) a changé de manière significative.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: À propos de l’arborescence d’éléments IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865257"
---
# <a name="about-the-iwiaitem2-item-tree"></a><span data-ttu-id="a79b5-103">À propos de l’arborescence d’éléments IWiaItem2</span><span class="sxs-lookup"><span data-stu-id="a79b5-103">About the IWiaItem2 Item Tree</span></span>

<span data-ttu-id="a79b5-104">Avec Windows Vista, l’arborescence des éléments de l’acquisition d’images Windows (WIA) a changé de manière significative.</span><span class="sxs-lookup"><span data-stu-id="a79b5-104">With Windows Vista, the Windows Image Acquisition (WIA) item tree has changed significantly.</span></span> <span data-ttu-id="a79b5-105">Les éléments [**IWiaItem2**](-wia-iwiaitem2.md) sont utilisés pour représenter des attributs d’appareil et des données de périphérique.</span><span class="sxs-lookup"><span data-stu-id="a79b5-105">[**IWiaItem2**](-wia-iwiaitem2.md) items are used to represent device attributes and device data.</span></span> <span data-ttu-id="a79b5-106">Les applications de création d’images voient un appareil WIA (Windows Image Acquisition) 2,0 sous la forme d’une arborescence d’éléments hiérarchique, avec l’élément racine représentant l’appareil lui-même et les éléments enfants représentant des éléments tels que des sources de données programmables, des images ou des dossiers qui contiennent des images.</span><span class="sxs-lookup"><span data-stu-id="a79b5-106">Imaging applications see a Windows Image Acquisition (WIA) 2.0 device as a hierarchical tree of items, with the root item representing the device itself and the child items representing things like programmable data sources, images, or folders that contain images.</span></span>

-   [<span data-ttu-id="a79b5-107">Éléments d’application</span><span class="sxs-lookup"><span data-stu-id="a79b5-107">Application Items</span></span>](#application-items)
-   [<span data-ttu-id="a79b5-108">Indicateurs d’élément</span><span class="sxs-lookup"><span data-stu-id="a79b5-108">Item Flags</span></span>](#item-flags)
-   [<span data-ttu-id="a79b5-109">Catégories d’éléments</span><span class="sxs-lookup"><span data-stu-id="a79b5-109">Item Categories</span></span>](#item-categories)
-   [<span data-ttu-id="a79b5-110">Élément racine</span><span class="sxs-lookup"><span data-stu-id="a79b5-110">Root Item</span></span>](#root-item)
-   [<span data-ttu-id="a79b5-111">Élément de données</span><span class="sxs-lookup"><span data-stu-id="a79b5-111">Data Item</span></span>](#data-item)
-   [<span data-ttu-id="a79b5-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a79b5-112">Related topics</span></span>](#related-topics)

## <a name="application-items"></a><span data-ttu-id="a79b5-113">Éléments d’application</span><span class="sxs-lookup"><span data-stu-id="a79b5-113">Application Items</span></span>

<span data-ttu-id="a79b5-114">L’arborescence d’éléments WIA 2,0 qu’une application peut voir est distincte de l’arborescence créée et gérée par un minipilote WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="a79b5-114">The WIA 2.0 item tree that an application can see is separate from the tree created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="a79b5-115">Lorsqu’un minipilote crée une arborescence, le service WIA 2,0 utilise cette arborescence d’éléments WIA 2,0 comme guide pour créer une copie de l’arborescence qui peut être affichée par des applications de création d’images.</span><span class="sxs-lookup"><span data-stu-id="a79b5-115">When a minidriver creates a tree, the WIA 2.0 service uses this WIA 2.0 item tree as a guide to create a copy of the tree that can be viewed by imaging applications.</span></span> <span data-ttu-id="a79b5-116">Les éléments de l’arborescence copiée sont appelés éléments d' *application* .</span><span class="sxs-lookup"><span data-stu-id="a79b5-116">Items in the copied tree are called *application* items.</span></span> <span data-ttu-id="a79b5-117">Les éléments de l’arborescence créés par un *minipilote* sont appelés éléments de pilote.</span><span class="sxs-lookup"><span data-stu-id="a79b5-117">Items in the tree created by a minidriver are called *driver* items.</span></span>

<span data-ttu-id="a79b5-118">Un élément WIA peut représenter une source de données programmable pour le chargeur de documents d’un scanneur ou les données stockées sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="a79b5-118">A WIA item can represent a programmable data source for a scanner's document feeder or the data stored on that device.</span></span> <span data-ttu-id="a79b5-119">Un appareil WIA doit être divisé en éléments individuels qui décrivent les différentes données produites par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="a79b5-119">A WIA device should be divided into individual items that describe different data produced by that device.</span></span>

<span data-ttu-id="a79b5-120">Par exemple, un scanneur WIA qui prend en charge la numérisation à plat et l’analyse du flux de documents peut être divisé en deux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="a79b5-120">For example, a WIA scanner that supports both flatbed scanning and document feeder scanning might be divided into two child items.</span></span> <span data-ttu-id="a79b5-121">L’une représente la fonctionnalité d’analyse à plat et l’autre représente la fonctionnalité d’analyse du flux de documents.</span><span class="sxs-lookup"><span data-stu-id="a79b5-121">One represents the flatbed scanning functionality and the other represents the document feeder scanning functionality.</span></span>

<span data-ttu-id="a79b5-122">Plusieurs images disposées sur un scanneur à plat et analysées en même temps peuvent être placées dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="a79b5-122">Multiple images laid out on a flatbed scanner and scanned at the same time can be placed in one folder.</span></span> <span data-ttu-id="a79b5-123">À l’aide du filtre de segmentation ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), chaque image ou sous-région peut ensuite être créée en tant qu’élément enfant du dossier.</span><span class="sxs-lookup"><span data-stu-id="a79b5-123">Using the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), each image or subregion can then be created as a child item of the folder.</span></span>

<span data-ttu-id="a79b5-124">L’arborescence WIA pour un appareil photo qui stocke des photos (« film ») peut être divisée en éléments qui représentent des dossiers, des sous-dossiers et des photos.</span><span class="sxs-lookup"><span data-stu-id="a79b5-124">The WIA tree for a camera device that stores photos ("Film") can be divided into items that represent folders, subfolders, and photos.</span></span>

## <a name="item-flags"></a><span data-ttu-id="a79b5-125">Indicateurs d’élément</span><span class="sxs-lookup"><span data-stu-id="a79b5-125">Item Flags</span></span>

<span data-ttu-id="a79b5-126">Les indicateurs d’élément WIA aident à classifier le contenu ou le comportement pris en charge d’un élément WIA particulier.</span><span class="sxs-lookup"><span data-stu-id="a79b5-126">WIA item flags help classify the content or supported behavior of a particular WIA item.</span></span> <span data-ttu-id="a79b5-127">Les indicateurs d’élément WIA se répartissent en deux groupes.</span><span class="sxs-lookup"><span data-stu-id="a79b5-127">WIA item flags fall into two groups.</span></span>

1.  <span data-ttu-id="a79b5-128">Les indicateurs d’état de l’élément signalent l’état actuel de l’élément WIA, par exemple [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, etc.</span><span class="sxs-lookup"><span data-stu-id="a79b5-128">Item status flags report the current state of the WIA item, for example, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, and so forth.</span></span>
2.  <span data-ttu-id="a79b5-129">Les indicateurs d’utilisation/représentation des données d’élément signalent les données que l’élément WIA représente ou peuvent produire en cas de transfert.</span><span class="sxs-lookup"><span data-stu-id="a79b5-129">Item data representation/usage flags report the data that the WIA item represents or can produce if transferred.</span></span> <span data-ttu-id="a79b5-130">Par exemple, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) est un indicateur de représentation de données qui indique à l’application que les données associées à l’élément WIA actuel sont des données image et doivent avoir des propriétés de données image.</span><span class="sxs-lookup"><span data-stu-id="a79b5-130">For example, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) is a data representation flag that tells the application the data associated with the current WIA item is image data and should have image data properties.</span></span> <span data-ttu-id="a79b5-131">**WIA \_ Les \_ \_ indicateurs d’élément** de la Loi sont un indicateur d’utilisation d’élément qui indique à l’application que l’élément WIA est configurable et qui suit un ensemble de règles de configuration prédéfinies basées sur la catégorie d’éléments de la [**\_ Loi \_ \_ WIA**](-wia-wiaitempropcommonitem.md) et que la configuration peut éventuellement modifier le résultat pour chaque transfert de données.</span><span class="sxs-lookup"><span data-stu-id="a79b5-131">**WIA\_IPA\_ITEM\_FLAGS** is an item usage flag that tells the application that the WIA item is configurable and follows a set of predefined configuration rules based on the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) and that the configuration can possibly change the result for each data transfer.</span></span> <span data-ttu-id="a79b5-132">(Pour plus d’informations sur les définitions de catégorie, consultez catégories d’éléments catégories [d’éléments.](#item-categories) )</span><span class="sxs-lookup"><span data-stu-id="a79b5-132">(For more information about category definitions, see [Item Categories](#item-categories) item categories.)</span></span>

<span data-ttu-id="a79b5-133">Le graphique suivant montre un exemple d’arborescence d’éléments WIA et les différents indicateurs qui peuvent être associés à chaque élément.</span><span class="sxs-lookup"><span data-stu-id="a79b5-133">The following graphic shows an example of a WIA item tree and the various flags that might be associated with each item.</span></span>

![exemples d’indicateurs d’élément pour les éléments d’une arborescence](images/scannertree1.jpg)

## <a name="item-categories"></a><span data-ttu-id="a79b5-135">Catégories d’éléments</span><span class="sxs-lookup"><span data-stu-id="a79b5-135">Item Categories</span></span>

<span data-ttu-id="a79b5-136">Les éléments WIA sont regroupés en catégories à l’aide des valeurs de propriété de [**\_ \_ \_ catégorie d’élément WIA**](-wia-wiaitempropcommonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b5-136">WIA items are grouped into categories using the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) property values.</span></span> <span data-ttu-id="a79b5-137">Ces catégories définissent la façon dont un élément WIA doit être traité ou utilisé.</span><span class="sxs-lookup"><span data-stu-id="a79b5-137">These categories define how a WIA item is to be treated or used.</span></span> <span data-ttu-id="a79b5-138">Par exemple, si l’élément représente un fichier fini ( \_ fichier de catégorie WIA \_ terminé \_ ), une application WIA doit supposer que les données sont statiques et situées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a79b5-138">For example, if the item represents a finished file (WIA\_CATEGORY\_FINISHED\_FILE), a WIA application should assume that the data is static and located on the device.</span></span> <span data-ttu-id="a79b5-139">Si l’élément représente un alimentation (chargeur de \_ catégorie WIA \_ ), l’application doit s’attendre à ce qu’elle contienne les propriétés du chargeur de documents requis et fonctionne comme un chargeur de documents.</span><span class="sxs-lookup"><span data-stu-id="a79b5-139">If the item represents a feeder (WIA\_CATEGORY\_FEEDER), the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span>

<span data-ttu-id="a79b5-140">Les catégories définies par WIA sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a79b5-140">The categories defined by WIA are:</span></span>

-   <span data-ttu-id="a79b5-141">WIA \_ catégorie \_ auto</span><span class="sxs-lookup"><span data-stu-id="a79b5-141">WIA\_CATEGORY\_AUTO</span></span>
-   <span data-ttu-id="a79b5-142">\_chargeur de catégorie WIA \_</span><span class="sxs-lookup"><span data-stu-id="a79b5-142">WIA\_CATEGORY\_FEEDER</span></span>
-   <span data-ttu-id="a79b5-143">\_film de catégorie WIA \_</span><span class="sxs-lookup"><span data-stu-id="a79b5-143">WIA\_CATEGORY\_FILM</span></span>
-   <span data-ttu-id="a79b5-144">\_fichier de catégorie WIA \_ terminé \_</span><span class="sxs-lookup"><span data-stu-id="a79b5-144">WIA\_CATEGORY\_FINISHED\_FILE</span></span>
-   <span data-ttu-id="a79b5-145">\_plateau de catégorie WIA \_</span><span class="sxs-lookup"><span data-stu-id="a79b5-145">WIA\_CATEGORY\_FLATBED</span></span>

<span data-ttu-id="a79b5-146">Par exemple, l’élément à plat WIA d’un scanneur peut avoir les indicateurs d’élément de la [**\_ Loi \_ \_ WIA**](-wia-wiaitempropcommonitem.md) définis sur [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** et **WiaItemTypeProgrammableDataSource**, et la propriété de **\_ \_ \_ catégorie d’élément WIA** de l’acquisition d’images est définie sur le plateau de catégorie WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a79b5-146">For example, a scanner's flatbed item may have the [**WIA\_IPA\_ITEM\_FLAGS**](-wia-wiaitempropcommonitem.md) set to [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer**, and **WiaItemTypeProgrammableDataSource**, and the **WIA\_IPA\_ITEM\_CATEGORY** property set to WIA\_CATEGORY\_FLATBED.</span></span>

<span data-ttu-id="a79b5-147">Le tableau suivant montre le regroupement des catégories WIA avec les indicateurs d’élément et les éléments WIA.</span><span class="sxs-lookup"><span data-stu-id="a79b5-147">The following table shows WIA category grouping with item flags and WIA items.</span></span> <span data-ttu-id="a79b5-148">Cette table n’inclut pas une liste complète des indicateurs d’éléments WIA définis par WIA.</span><span class="sxs-lookup"><span data-stu-id="a79b5-148">This table does not include a full list of the WIA item flags defined by WIA.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a79b5-149">Catégorie WIA</span><span class="sxs-lookup"><span data-stu-id="a79b5-149">WIA Category</span></span></th>
<th><span data-ttu-id="a79b5-150">Indicateurs d’élément WIA valides</span><span class="sxs-lookup"><span data-stu-id="a79b5-150">Valid WIA Item Flags</span></span></th>
<th><span data-ttu-id="a79b5-151">Jeu de propriétés WIA</span><span class="sxs-lookup"><span data-stu-id="a79b5-151">WIA Property Set</span></span></th>
<th><span data-ttu-id="a79b5-152">Éléments WIA</span><span class="sxs-lookup"><span data-stu-id="a79b5-152">WIA Items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a79b5-153">WIA_CATEGORY_AUTO</span><span class="sxs-lookup"><span data-stu-id="a79b5-153">WIA_CATEGORY_AUTO</span></span></td>
<td><ul>
<li><span data-ttu-id="a79b5-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="a79b5-158">Le jeu de propriétés comprend les propriétés de l’analyseur configuré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a79b5-158">Property set includes auto-configured scanner properties.</span></span></td>
<td><span data-ttu-id="a79b5-159">Élément auto WIA qui représente les paramètres d’analyse automatique configurés pour le scanneur.</span><span class="sxs-lookup"><span data-stu-id="a79b5-159">WIA auto item that represents the scanner's auto-configured scanning settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a79b5-160">WIA_CATEGORY_FEEDER</span><span class="sxs-lookup"><span data-stu-id="a79b5-160">WIA_CATEGORY_FEEDER</span></span></td>
<td><ul>
<li><span data-ttu-id="a79b5-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="a79b5-166">Le jeu de propriétés comprend les propriétés du contrôle de l’analyseur du chargeur (généralement un jeu de propriétés d’image et de document spécifique).</span><span class="sxs-lookup"><span data-stu-id="a79b5-166">Property set includes feeder scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="a79b5-167">Éléments de chargeur WIA, y compris les éléments enfants qui représentent les pages frontale et précédente d’un document.</span><span class="sxs-lookup"><span data-stu-id="a79b5-167">WIA Feeder items, including child items that represent the front and back pages of a document.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a79b5-168">WIA_CATEGORY_FILM</span><span class="sxs-lookup"><span data-stu-id="a79b5-168">WIA_CATEGORY_FILM</span></span></td>
<td><ul>
<li><span data-ttu-id="a79b5-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="a79b5-173">Le jeu de propriétés comprend les propriétés du contrôle scanner de film (généralement un jeu de propriétés d’image et de document spécifique).</span><span class="sxs-lookup"><span data-stu-id="a79b5-173">Property set includes film scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="a79b5-174">Éléments de film WIA, y compris les éléments enfants qui représentent les trames d’analyse individuelles.</span><span class="sxs-lookup"><span data-stu-id="a79b5-174">WIA Film items, including child items that represent the individual scanning frames.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a79b5-175">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="a79b5-175">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><ul>
<li><span data-ttu-id="a79b5-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="a79b5-182">La propriété définie sur cet élément dépend du type d’élément signalé.</span><span class="sxs-lookup"><span data-stu-id="a79b5-182">The property set on this item depends on the item type reported.</span></span> <span data-ttu-id="a79b5-183">Par exemple, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> doit inclure des propriétés d’élément d’image, telles que les bits par pixel et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a79b5-183">For example, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> should include some image item properties, like bits per pixel and so forth.</span></span></td>
<td><span data-ttu-id="a79b5-184">Éléments de stockage WIA, y compris les éléments enfants qui représentent le contenu du fichier fini (fichiers de données tels que JPEG, HTML, TXT, etc.).</span><span class="sxs-lookup"><span data-stu-id="a79b5-184">WIA storage items, including child items that represent finished file content (data files like JPEG, HTML, TXT, and so forth).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a79b5-185">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="a79b5-185">WIA_CATEGORY_FLATBED</span></span></td>
<td><ul>
<li><span data-ttu-id="a79b5-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="a79b5-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="a79b5-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>: peut être présent si le scanneur prend en charge l’analyse de plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="a79b5-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—may be present if the scanner supports multi-item scanning.</span></span></li>
<li><span data-ttu-id="a79b5-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>: peut être présent si l’application génère un élément WIA au cours d’une session d’analyse de plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="a79b5-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>—may be present if the application generates a WIA item during a multi-item scanning session.</span></span></li>
</ul></td>
<td><span data-ttu-id="a79b5-192">Le jeu de propriétés comprend des propriétés de contrôle de scanneur à plat (généralement un jeu de propriétés d’image et de document spécifique).</span><span class="sxs-lookup"><span data-stu-id="a79b5-192">The property set includes flatbed scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="a79b5-193">Éléments à plat WIA, y compris les éléments enfants qui représentent des régions en cours d’analyse sur le plateau à plateau du scanneur.</span><span class="sxs-lookup"><span data-stu-id="a79b5-193">WIA flatbed items, including child items that represent regions being scanned on the scanner's flatbed platen.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a79b5-194">Le graphique suivant montre un exemple d’arborescence d’éléments WIA et les différentes catégories qui peuvent être associées à chaque élément.</span><span class="sxs-lookup"><span data-stu-id="a79b5-194">The following graphic shows an example of a WIA item tree and the various categories that might be associated with each item.</span></span>

![exemples de catégories d’éléments pour les éléments d’une arborescence](images/scannertree2.jpg)

## <a name="root-item"></a><span data-ttu-id="a79b5-196">Élément racine</span><span class="sxs-lookup"><span data-stu-id="a79b5-196">Root Item</span></span>

<span data-ttu-id="a79b5-197">Un élément racine WIA est un élément de dossier marqué avec des indicateurs [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) et **WiaItemTypeDevice** qui représente l’appareil lui-même.</span><span class="sxs-lookup"><span data-stu-id="a79b5-197">A WIA root item is a folder item marked with [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) and **WiaItemTypeDevice** flags that represents the device itself.</span></span> <span data-ttu-id="a79b5-198">Il contient des attributs d’appareil tels que le fabricant, le nom de périphérique et les attributs de pilote tels que la version de pilote et l’identificateur de classe d’interface utilisateur (CLSID).</span><span class="sxs-lookup"><span data-stu-id="a79b5-198">It contains device attributes like manufacturer, device name, and driver attributes like driver version and user interface class identifier (CLSID).</span></span> <span data-ttu-id="a79b5-199">Les applications d’acquisition d’images obtiennent la racine de l’arborescence des éléments WIA en appelant la méthode [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b5-199">Imaging applications get the root to the WIA item tree by calling [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) method.</span></span> <span data-ttu-id="a79b5-200">L’application utilise l’élément racine pour accéder aux éléments WIA enfants individuels en énumérant l’arborescence (voir [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span><span class="sxs-lookup"><span data-stu-id="a79b5-200">The application uses the root item to gain access to the individual child WIA items by enumerating the tree (see [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span></span>

## <a name="data-item"></a><span data-ttu-id="a79b5-201">DataItem</span><span class="sxs-lookup"><span data-stu-id="a79b5-201">Data Item</span></span>

<span data-ttu-id="a79b5-202">Tout élément pouvant être utilisé pour transférer des données est considéré comme un élément de données.</span><span class="sxs-lookup"><span data-stu-id="a79b5-202">Any item that can be use to transfer data is considered a data item.</span></span> <span data-ttu-id="a79b5-203">Cela comprend les éléments marqués avec l’indicateur [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b5-203">This includes items marked with the [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) flag.</span></span>

<span data-ttu-id="a79b5-204">Les éléments de dossier et les éléments sans dossier peuvent exposer la possibilité de transférer des données en étant marqués avec l’indicateur [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b5-204">Folder items and nonfolder items can expose the ability to transfer data by being marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag.</span></span> <span data-ttu-id="a79b5-205">Tout élément avec cet indicateur doit fournir les propriétés d’élément WIA suivantes :</span><span class="sxs-lookup"><span data-stu-id="a79b5-205">Any item with this flag set has to provide the following WIA item properties:</span></span>

-   [<span data-ttu-id="a79b5-206">**\_droits d' \_ accès WIA pour WIA \_**</span><span class="sxs-lookup"><span data-stu-id="a79b5-206">**WIA\_IPA\_ACCESS\_RIGHTS**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="a79b5-207">**taille de l’élément WIA de la \_ Loi WIA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a79b5-207">**WIA\_IPA\_ITEM\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="a79b5-208">**taille de la \_ \_ mémoire tampon WIA de la loi WIA \_**</span><span class="sxs-lookup"><span data-stu-id="a79b5-208">**WIA\_IPA\_BUFFER\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="a79b5-209">**FORMAT WIA de la \_ Loi WIA \_**</span><span class="sxs-lookup"><span data-stu-id="a79b5-209">**WIA\_IPA\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="a79b5-210">**\_ \_ format préféré WIA de la loi WIA \_**</span><span class="sxs-lookup"><span data-stu-id="a79b5-210">**WIA\_IPA\_PREFERRED\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="a79b5-211">**TYMED de la \_ Loi WIA \_**</span><span class="sxs-lookup"><span data-stu-id="a79b5-211">**WIA\_IPA\_TYMED**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="a79b5-212">**\_extension de \_ nom de fichier WIA de la loi WIA \_**</span><span class="sxs-lookup"><span data-stu-id="a79b5-212">**WIA\_IPA\_FILENAME\_EXTENSION**</span></span>](-wia-wiaitempropcommonitem.md)

<span data-ttu-id="a79b5-213">Les éléments de source de données programmables marqués avec l’indicateur [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) doivent également fournir le jeu de propriétés d’élément de données requis.</span><span class="sxs-lookup"><span data-stu-id="a79b5-213">Programmable data source items marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag must also supply the data item required property set.</span></span>

<span data-ttu-id="a79b5-214">Les éléments de données WIA peuvent avoir des propriétés supplémentaires en fonction des paramètres de l’indicateur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a79b5-214">WIA data items may have additional properties depending on the item's flag settings.</span></span> <span data-ttu-id="a79b5-215">Par exemple, les éléments WIA marqués avec l’indicateur [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) doivent avoir des propriétés d’informations spécifiques à l’image, telles que WIA et le **\_ \_ nombre \_ de \_ lignes WIA de** la loi WIA. [**\_ \_**](-wia-wiaitempropcommonitem.md)</span><span class="sxs-lookup"><span data-stu-id="a79b5-215">For example, WIA items marked with the [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) flag should have image specific information properties, like [**WIA\_IPA\_DEPTH**](-wia-wiaitempropcommonitem.md) and **WIA\_IPA\_NUMBER\_OF\_LINES**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a79b5-216">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a79b5-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a79b5-217">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="a79b5-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a79b5-218">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="a79b5-218">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="a79b5-219">**IEnumWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="a79b5-219">**IEnumWiaItem2**</span></span>](-wia-ienumwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="a79b5-220">**IWiaDevMgr2**</span><span class="sxs-lookup"><span data-stu-id="a79b5-220">**IWiaDevMgr2**</span></span>](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 




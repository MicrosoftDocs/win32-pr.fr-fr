---
description: Ces constantes définissent des valeurs qui spécifient le type d’objets IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Types de nœuds de contexte (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111699"
---
# <a name="context-node-types"></a><span data-ttu-id="be517-103">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="be517-103">Context Node Types</span></span>

<span data-ttu-id="be517-104">Ces constantes définissent des valeurs qui spécifient le type d’objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="be517-104">These constants define values that specify the type of [**IContextNode**](icontextnode.md) objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="be517-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="be517-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="be517-106">Description</span><span class="sxs-lookup"><span data-stu-id="be517-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <span data-ttu-id="be517-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(ANALYSISHINT)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-108">Représente un nœud qui contient des informations de contexte supplémentaires pour une région que le <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> utilise pour améliorer son analyse.</span><span class="sxs-lookup"><span data-stu-id="be517-108">Represents a node that contains additional context information for a region that the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> uses to improve its analysis.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <span data-ttu-id="be517-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CUSTOMRECOGNIZER)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CustomRecognizer)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-110">Représente un nœud utilisé pour une opération de reconnaissance unique.</span><span class="sxs-lookup"><span data-stu-id="be517-110">Represents a node used for a single recognition operation.</span></span><br/> <span data-ttu-id="be517-111">Tous les traits et les nœuds qui se trouvent dans un nœud de reconnaissance personnalisé sont reconnus par une opération de reconnaissance indépendante et ne sont pas analysés par le <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="be517-111">All strokes and nodes that are within a custom recognizer node are recognized by an independent recognition operation and are not analyzed by the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span></span><br/> <span data-ttu-id="be517-112">Un nœud de reconnaissance personnalisé doit être l’enfant direct du nœud racine de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="be517-112">A custom recognizer node must be the direct child of ink analyzer's root node.</span></span><br/> <span data-ttu-id="be517-113">Un nœud de reconnaissance personnalisé peut contenir les types d’éléments enfants suivants :</span><span class="sxs-lookup"><span data-stu-id="be517-113">A custom recognizer node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="be517-114">N’importe quel nombre de nœuds UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="be517-114">Any number of UnclassifiedInk nodes.</span></span></li>
<li><span data-ttu-id="be517-115">N’importe quel nombre de nœuds d’objet.</span><span class="sxs-lookup"><span data-stu-id="be517-115">Any number of Object nodes.</span></span></li>
<li><span data-ttu-id="be517-116">N’importe quel nombre de nœuds de ligne.</span><span class="sxs-lookup"><span data-stu-id="be517-116">Any number of Line nodes.</span></span></li>
<li><span data-ttu-id="be517-117">N’importe quel nombre de nœuds InkWord.</span><span class="sxs-lookup"><span data-stu-id="be517-117">Any number of InkWord nodes.</span></span></li>
<li><span data-ttu-id="be517-118">N’importe quel nombre de nœuds avec une valeur Guid inconnue.</span><span class="sxs-lookup"><span data-stu-id="be517-118">Any number of nodes with an unknown Guid value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <span data-ttu-id="be517-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(image)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Image)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-120">Représente un nœud pour une région à deux dimensions où des images non manuscrites peuvent exister dans le document.</span><span class="sxs-lookup"><span data-stu-id="be517-120">Represents a node for a two-dimensional region where any non-ink images can exist in the document.</span></span><br/> <span data-ttu-id="be517-121"><a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> ne produit pas de nœuds d’image.</span><span class="sxs-lookup"><span data-stu-id="be517-121">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce image nodes.</span></span> <span data-ttu-id="be517-122">Utilisez <a href="icontextnode-createsubnode.md"><strong>IContextNode :: CreateSubNode</strong></a> pour ajouter un nœud d’image à l’arborescence du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="be517-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add an image node to the context node tree.</span></span> <span data-ttu-id="be517-123">Le <strong>IInkAnalyzer</strong> utilise ensuite les régions définies par le nœud image pour déterminer si une encre annote l’image non manuscrite.</span><span class="sxs-lookup"><span data-stu-id="be517-123">The <strong>IInkAnalyzer</strong> then uses the regions defined by the image node to determine if any ink annotates the non-ink image.</span></span><br/> <span data-ttu-id="be517-124">Un nœud d’image ne peut pas avoir d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="be517-124">An image node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <span data-ttu-id="be517-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(INKBULLET)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-126">Le ContextNodeType InkBullet représente une collection de traits qui composent une puce dans une liste à puces.</span><span class="sxs-lookup"><span data-stu-id="be517-126">The InkBullet ContextNodeType represents a collection of strokes that make up a bullet in a bulleted list.</span></span><br/> <span data-ttu-id="be517-127">Un ContextNode de type InkBullet ne peut pas avoir d’enfants.</span><span class="sxs-lookup"><span data-stu-id="be517-127">A ContextNode of type InkBullet cannot have any children.</span></span> <span data-ttu-id="be517-128">Il peut uniquement être un enfant d’un paragraphe ContextNode.</span><span class="sxs-lookup"><span data-stu-id="be517-128">It can only be a child of a Paragraph ContextNode.</span></span> <span data-ttu-id="be517-129">Un seul InkBullet peut apparaître dans un ContextNode de paragraphe unique.</span><span class="sxs-lookup"><span data-stu-id="be517-129">Only one InkBullet can appear in a single Paragraph ContextNode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <span data-ttu-id="be517-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(INKDRAWING)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-131">Représente un nœud pour une collection de traits qui constitue un dessin.</span><span class="sxs-lookup"><span data-stu-id="be517-131">Represents a node for a collection of strokes that constitutes a drawing.</span></span><br/> <span data-ttu-id="be517-132">Les dessins sont des traits qui sont déterminés comme étant des formes ou des croquis abstraits.</span><span class="sxs-lookup"><span data-stu-id="be517-132">Drawings are strokes that are determined to be shapes or abstract sketches.</span></span> <span data-ttu-id="be517-133">Il s’agit généralement de traits qui ne sont pas classés comme traits d’écriture.</span><span class="sxs-lookup"><span data-stu-id="be517-133">They are generally any strokes that are not classified as writing strokes.</span></span><br/> <span data-ttu-id="be517-134">Un nœud de dessin d’encre ne peut pas avoir d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="be517-134">An ink drawing node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <span data-ttu-id="be517-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(INKWORD)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-136">Représente un nœud pour une collection de traits qui constitue un regroupement logique pour former un mot reconnaissable.</span><span class="sxs-lookup"><span data-stu-id="be517-136">Represents a node for a collection of strokes that constitutes a logical grouping to form a recognizable word.</span></span><br/> <span data-ttu-id="be517-137">Un nœud de mot Ink ne peut pas contenir d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="be517-137">An ink word node cannot contain any child elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <span data-ttu-id="be517-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(ligne)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Line)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-139">Représente un nœud pour une ligne de mots.</span><span class="sxs-lookup"><span data-stu-id="be517-139">Represents a node for a line of words.</span></span><br/> <span data-ttu-id="be517-140">Un nœud de ligne peut contenir les types d’éléments enfants suivants :</span><span class="sxs-lookup"><span data-stu-id="be517-140">A line node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="be517-141">N’importe quel nombre de nœuds de mots manuscrits.</span><span class="sxs-lookup"><span data-stu-id="be517-141">Any number of ink word nodes.</span></span></li>
<li><span data-ttu-id="be517-142">Un nombre quelconque de nœuds de mots de texte.</span><span class="sxs-lookup"><span data-stu-id="be517-142">Any number of text word nodes.</span></span></li>
<li><span data-ttu-id="be517-143">N’importe quel nombre de nœuds avec une valeur <strong>GUID</strong> inconnue.</span><span class="sxs-lookup"><span data-stu-id="be517-143">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <span data-ttu-id="be517-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(objet)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Object)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-145">Représente un nœud pour un objet retourné à partir d’un module de &quot; &quot; reconnaissance personnalisé d’objet.</span><span class="sxs-lookup"><span data-stu-id="be517-145">Represents a node for an object that is returned from an &quot;object&quot; custom recognizer.</span></span><br/> <span data-ttu-id="be517-146">Un nœud d’objet ne peut pas contenir d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="be517-146">An object node cannot contain any child elements.</span></span><br/> <span data-ttu-id="be517-147">Seuls les nœuds de reconnaissance personnalisés peuvent contenir des nœuds d’objet.</span><span class="sxs-lookup"><span data-stu-id="be517-147">Only custom recognizer nodes can contain object nodes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <span data-ttu-id="be517-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(paragraphe)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Paragraph)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-149">Représente un nœud pour une collection de nœuds qui constitue un regroupement logique de lignes.</span><span class="sxs-lookup"><span data-stu-id="be517-149">Represents a node for a collection of nodes that constitutes a logical grouping of lines.</span></span><br/> <span data-ttu-id="be517-150">La définition exacte d’un paragraphe est déterminée par les moteurs d’analyse.</span><span class="sxs-lookup"><span data-stu-id="be517-150">The exact definition of a paragraph is determined by the analyzing engines.</span></span> <span data-ttu-id="be517-151">En général, un paragraphe contient des groupes de lignes qui sont redistribuées ensemble si la zone qui contient les lignes a été redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="be517-151">In general, a paragraph contains groups of lines that would reflow together if the box that contains the lines were resized.</span></span><br/> <span data-ttu-id="be517-152">Un nœud de paragraphe peut contenir les types d’éléments enfants suivants :</span><span class="sxs-lookup"><span data-stu-id="be517-152">A paragraph node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="be517-153">N’importe quel nombre de nœuds de puces manuscrits.</span><span class="sxs-lookup"><span data-stu-id="be517-153">Any number of ink bullet nodes.</span></span></li>
<li><span data-ttu-id="be517-154">N’importe quel nombre de nœuds de ligne.</span><span class="sxs-lookup"><span data-stu-id="be517-154">Any number of line nodes.</span></span></li>
<li><span data-ttu-id="be517-155">N’importe quel nombre de nœuds avec une valeur <strong>GUID</strong> inconnue.</span><span class="sxs-lookup"><span data-stu-id="be517-155">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <span data-ttu-id="be517-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(racine)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(Root)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-157">Représente un nœud pour le nœud supérieur d’une arborescence de nœuds qui décrivent les résultats de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="be517-157">Represents a node for the top node of a tree of nodes that describe the results of ink analysis.</span></span><br/> <span data-ttu-id="be517-158">Les nœuds racine sont généralement obtenus à partir de la méthode de <a href="iinkanalyzer-getrootnode.md"><strong>méthode IInkAnalyzer :: GetRootNode</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="be517-158">Root nodes are generally obtained from the <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode Method</strong></a> method.</span></span><br/> <span data-ttu-id="be517-159">Un nœud racine peut contenir les types d’éléments enfants suivants :</span><span class="sxs-lookup"><span data-stu-id="be517-159">A root node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="be517-160">Un nombre quelconque de nœuds d’indicateurs d’analyse.</span><span class="sxs-lookup"><span data-stu-id="be517-160">Any number of analysis hint nodes.</span></span></li>
<li><span data-ttu-id="be517-161">N’importe quel nombre de nœuds de reconnaissance personnalisés.</span><span class="sxs-lookup"><span data-stu-id="be517-161">Any number of custom recognizer nodes.</span></span></li>
<li><span data-ttu-id="be517-162">N’importe quel nombre de nœuds image.</span><span class="sxs-lookup"><span data-stu-id="be517-162">Any number of image nodes.</span></span></li>
<li><span data-ttu-id="be517-163">N’importe quel nombre de nœuds de dessin de l’encre.</span><span class="sxs-lookup"><span data-stu-id="be517-163">Any number of ink drawing nodes.</span></span></li>
<li><span data-ttu-id="be517-164">N’importe quel nombre de nœuds de région d’écriture.</span><span class="sxs-lookup"><span data-stu-id="be517-164">Any number of writing region nodes.</span></span></li>
<li><span data-ttu-id="be517-165">N’importe quel nombre de nœuds d’encre non classifiés.</span><span class="sxs-lookup"><span data-stu-id="be517-165">Any number of unclassified ink nodes.</span></span></li>
<li><span data-ttu-id="be517-166">N’importe quel nombre de nœuds avec une valeur <strong>GUID</strong> inconnue.</span><span class="sxs-lookup"><span data-stu-id="be517-166">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <span data-ttu-id="be517-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TEXTWORD)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TextWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-168">Représente un nœud pour la région à deux dimensions où tout texte non manuscrit peut exister dans le document.</span><span class="sxs-lookup"><span data-stu-id="be517-168">Represents a node for the two-dimensional region where any non-ink text can exist in the document.</span></span><br/> <span data-ttu-id="be517-169"><a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> ne produit pas de nœuds de mots de texte.</span><span class="sxs-lookup"><span data-stu-id="be517-169">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce text word nodes.</span></span> <span data-ttu-id="be517-170">Utilisez <a href="icontextnode-createsubnode.md"><strong>IContextNode :: CreateSubNode</strong></a> pour ajouter un nœud de mot de texte à l’arborescence du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="be517-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add a text word node to the context node tree.</span></span> <span data-ttu-id="be517-171">Le <strong>IInkAnalyzer</strong> utilise ensuite les régions définies par le nœud mot de texte pour déterminer si une encre annote le texte non manuscrit.</span><span class="sxs-lookup"><span data-stu-id="be517-171">The <strong>IInkAnalyzer</strong> then uses the regions defined by the text word node to determine if any ink annotates the non-ink text.</span></span><br/> <span data-ttu-id="be517-172">Les futurs reconnaisseurs peuvent utiliser la région définie par un nœud de mot de texte pour déterminer si une encre annote le mot non manuscrit.</span><span class="sxs-lookup"><span data-stu-id="be517-172">Future recognizers may use the region defined by a text word node to determine if any ink annotates the non-ink word.</span></span><br/> <span data-ttu-id="be517-173">Un nœud de mot de texte ne peut pas avoir d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="be517-173">A text word node cannot have any child elements</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <span data-ttu-id="be517-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span><span class="sxs-lookup"><span data-stu-id="be517-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="be517-175">Représente un nœud pour tous les traits qui n’ont pas encore été classifiés ou reconnus.</span><span class="sxs-lookup"><span data-stu-id="be517-175">Represents a node for any strokes that have not yet been classified or recognized.</span></span><br/> <span data-ttu-id="be517-176">Un nœud d’encre non classifié ne peut pas avoir d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="be517-176">An unclassified ink node cannot have any child elements.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="be517-177">Notes</span><span class="sxs-lookup"><span data-stu-id="be517-177">Remarks</span></span>

<span data-ttu-id="be517-178">Pour plus d’informations sur les différents types de nœuds de contexte, consultez [vue d’ensemble de l’analyse d’encre](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="be517-178">For more information about the different context node types, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be517-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be517-179">Requirements</span></span>



| <span data-ttu-id="be517-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be517-180">Requirement</span></span> | <span data-ttu-id="be517-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="be517-181">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be517-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be517-182">Minimum supported client</span></span><br/> | <span data-ttu-id="be517-183">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be517-183">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="be517-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be517-184">Minimum supported server</span></span><br/> | <span data-ttu-id="be517-185">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be517-185">None supported</span></span><br/>                                                           |
| <span data-ttu-id="be517-186">En-tête</span><span class="sxs-lookup"><span data-stu-id="be517-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="be517-187"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="be517-187"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be517-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be517-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be517-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="be517-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="be517-190">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="be517-190">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="be517-191">**IContextNode :: GetType**</span><span class="sxs-lookup"><span data-stu-id="be517-191">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="be517-192">**IInkAnalyzer :: CreateAnalysisHint, méthode**</span><span class="sxs-lookup"><span data-stu-id="be517-192">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="be517-193">**IInkAnalyzer :: CreateCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="be517-193">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="be517-194">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="be517-194">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="be517-195">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="be517-195">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="be517-196">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="be517-196">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="be517-197">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="be517-197">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 





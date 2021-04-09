---
title: Informations de référence sur les métafichiers Windows Media
description: Informations de référence sur les métafichiers Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Fichiers Windows Media, référence
- sous-fichiers, référence
- référence pour les fichiers Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029174"
---
# <a name="windows-media-metafile-reference"></a><span data-ttu-id="6af7a-106">Informations de référence sur les métafichiers Windows Media</span><span class="sxs-lookup"><span data-stu-id="6af7a-106">Windows Media Metafile Reference</span></span>

<span data-ttu-id="6af7a-107">Cette référence décrit les éléments et les extensions de nom de fichier pour les fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6af7a-107">This reference documents elements and file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="6af7a-108">La référence est divisée en sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6af7a-108">The reference is divided into the following sections.</span></span>



| <span data-ttu-id="6af7a-109">Section</span><span class="sxs-lookup"><span data-stu-id="6af7a-109">Section</span></span>                                                                                    | <span data-ttu-id="6af7a-110">Description</span><span class="sxs-lookup"><span data-stu-id="6af7a-110">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6af7a-111">Informations de référence sur les éléments de métafichier Windows Media</span><span class="sxs-lookup"><span data-stu-id="6af7a-111">Windows Media Metafile Elements Reference</span></span>](windows-media-metafile-elements-reference.md) | <span data-ttu-id="6af7a-112">Documente les éléments de métafichier, y compris les définitions, les attributs et leurs valeurs, ainsi que les conditions spéciales associées à chaque élément.</span><span class="sxs-lookup"><span data-stu-id="6af7a-112">Documents metafile elements, including definitions, attributes and their values, and special conditions related to each element.</span></span> |
| [<span data-ttu-id="6af7a-113">Extensions de noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="6af7a-113">File Name Extensions</span></span>](file-name-extensions.md)                                           | <span data-ttu-id="6af7a-114">Documente les extensions de nom de fichier de métafichier avec des règles et des instructions sur leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="6af7a-114">Documents metafile file name extensions with rules and guidelines on their use.</span></span>                                                  |



 

<span data-ttu-id="6af7a-115">Les fichiers Windows Media sont des fichiers texte qui fournissent des informations sur un flux de fichier et sa présentation.</span><span class="sxs-lookup"><span data-stu-id="6af7a-115">Windows Media metafiles are text files that provide information about a file stream and its presentation.</span></span> <span data-ttu-id="6af7a-116">Les sous-fichiers sont basés sur la syntaxe du Extensible Markup Language (XML) et sont constitués d’éléments de type XML avec leurs balises et leurs attributs.</span><span class="sxs-lookup"><span data-stu-id="6af7a-116">The metafiles are based on the Extensible Markup Language (XML) syntax, and are made up of various XML-like elements with their tags and attributes.</span></span> <span data-ttu-id="6af7a-117">Chaque élément définit un paramètre ou une action pour la diffusion multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="6af7a-117">Each element defines a setting or action for streaming media.</span></span>

<span data-ttu-id="6af7a-118">Deux ensembles de balises d’éléments sont disponibles pour les fichiers de configuration.</span><span class="sxs-lookup"><span data-stu-id="6af7a-118">There are two sets of element tags available for metafiles.</span></span> <span data-ttu-id="6af7a-119">Les fichiers de configuration côté client ont un ensemble d’éléments, et les fichiers de configuration côté serveur ont un autre ensemble d’éléments.</span><span class="sxs-lookup"><span data-stu-id="6af7a-119">Client-side metafiles have one set of elements, and server-side metafiles have another set of elements.</span></span>

<span data-ttu-id="6af7a-120">Si une balise d’élément n’a pas d’éléments enfants (ceux qui modifient ou sont contenus dans un autre élément), un caractère de barre oblique (/) peut être utilisé à la fin de la balise d’ouverture à la place d’une balise de fermeture.</span><span class="sxs-lookup"><span data-stu-id="6af7a-120">If an element tag does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag in place of a closing tag.</span></span> <span data-ttu-id="6af7a-121">Si les éléments enfants n’apparaissent pas entre les balises d’ouverture et de fermeture d’un élément, ils ne sont pas des éléments enfants pour cet élément et sont ignorés ou provoquent une erreur dans la syntaxe du métafichier.</span><span class="sxs-lookup"><span data-stu-id="6af7a-121">If child elements do not appear between the opening and closing tag for an element, they are not child elements for that element, and are ignored or cause an error in the syntax of the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6af7a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6af7a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6af7a-123">**À propos des fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6af7a-123">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="6af7a-124">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6af7a-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="6af7a-125">**Fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6af7a-125">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





---
title: Paramètre MSWMExt (déconseillé)
description: Paramètre MSWMExt (déconseillé)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Fichiers Windows Media, paramètre MSWMExt
- MSWMExt, paramètre
- Paramètre MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381597"
---
# <a name="mswmext-parameter-deprecated"></a><span data-ttu-id="cce73-106">Paramètre MSWMExt (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="cce73-106">MSWMExt Parameter (deprecated)</span></span>

<span data-ttu-id="cce73-107">Le paramètre *MSWMExt* indique à un programme client le format d’un fichier référencé.</span><span class="sxs-lookup"><span data-stu-id="cce73-107">The *MSWMExt* parameter indicates to a client program the format of a referenced file.</span></span>

<span data-ttu-id="cce73-108">**Syntaxe**</span><span class="sxs-lookup"><span data-stu-id="cce73-108">**Syntax**</span></span>


```XML

URL?MSWMExt=.
ext
```



<span data-ttu-id="cce73-109">**Exemple de code**</span><span class="sxs-lookup"><span data-stu-id="cce73-109">**Example Code**</span></span>


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a><span data-ttu-id="cce73-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cce73-110">Remarks</span></span>

<span data-ttu-id="cce73-111">Les programmes clients utilisent parfois une extension de nom de fichier ou un type MIME pour déterminer s’il faut restituer un fichier multimédia en tant que flux, restituer le fichier après un téléchargement complet ou refuser le rendu du fichier.</span><span class="sxs-lookup"><span data-stu-id="cce73-111">Client programs sometimes use a file name extension or a MIME type to determine whether to render a media file as a stream, render the file after a full download, or refuse to render the file at all.</span></span> <span data-ttu-id="cce73-112">Si un programme client ne peut pas déterminer comment traiter un fichier multimédia basé sur l’extension de nom de fichier ou le type MIME, il peut déterminer comment traiter le fichier en inspectant le paramètre *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="cce73-112">If a client program cannot determine how to treat a media file based on the file name extension or the MIME type, it can determine how to treat the file by inspecting the *MSWMExt* parameter.</span></span> <span data-ttu-id="cce73-113">Par exemple, le client peut traiter le fichier comme s’il avait une extension égale à la valeur du paramètre *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="cce73-113">For example, the client could treat the file as if it had an extension equal to the value of the *MSWMExt* parameter.</span></span> <span data-ttu-id="cce73-114">Pour plus d’informations sur les types MIME et les extensions de nom de fichier, consultez [extensions de nom de fichier](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="cce73-114">For more information about MIME types and file name extensions, see [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="cce73-115">Pour plus d’informations sur le paramètre *MSWMExt* , voir l’article [236895](https://support.microsoft.com/kb/236895) de la base de connaissances Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cce73-115">For more information about the *MSWMExt* parameter, see article [236895](https://support.microsoft.com/kb/236895) in the Microsoft Knowledge Base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cce73-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cce73-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce73-117">**Versions précédentes des fichiers Windows Media (déconseillés)**</span><span class="sxs-lookup"><span data-stu-id="cce73-117">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 





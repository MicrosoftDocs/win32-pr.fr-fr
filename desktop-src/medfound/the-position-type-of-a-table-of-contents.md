---
description: Le type de position d’une table des matières
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Le type de position d’une table des matières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543486"
---
# <a name="the-position-type-of-a-table-of-contents"></a><span data-ttu-id="0a4c8-103">Le type de position d’une table des matières</span><span class="sxs-lookup"><span data-stu-id="0a4c8-103">The Position Type of a Table of Contents</span></span>

<span data-ttu-id="0a4c8-104">Certaines méthodes de l’interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) ont un paramètre nommé *enumTocPosType* qui est de type [**enum TOC \_ pos \_**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span><span class="sxs-lookup"><span data-stu-id="0a4c8-104">Some methods of the [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface have a parameter named *enumTocPosType* that has a type of [**enum TOC\_POS\_TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span></span> <span data-ttu-id="0a4c8-105">Ce paramètre spécifie la position dans un fichier multimédia où une table des matières est stockée.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-105">This parameter specifies the position in a media file where a table of contents is stored.</span></span> <span data-ttu-id="0a4c8-106">L’objectif était que la table des matières pouvait être stockée dans l’en-tête de fichier ou dans le corps du fichier sous la forme d’un objet de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-106">The intent was that the table of contents could be stored either in the file header or in the body of the file as a top level object.</span></span> <span data-ttu-id="0a4c8-107">Cette fonctionnalité n’a pas encore été implémentée.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-107">This functionality has not, as yet, been implemented.</span></span>

<span data-ttu-id="0a4c8-108">Actuellement, les tables de matières ne peuvent être stockées qu’en tant qu’objets de niveau supérieur. vous devez donc toujours définir le paramètre *enumTocPosType* sur **TOC \_ pos \_ TOPLEVELOBJECT**.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-108">Currently, tables of contents can only be stored as top level objects, so you must always set the *enumTocPosType* parameter to **TOC\_POS\_TOPLEVELOBJECT**.</span></span> <span data-ttu-id="0a4c8-109">Si vous affectez à *enumTocPosType* la valeur **\_ \_ en-tête de la table des matières TOC**, la méthode retourne **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="0a4c8-109">If you set *enumTocPosType* to **TOC\_POS\_INHEADER**, the method will return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="0a4c8-110">Les méthodes suivantes ont un paramètre *enumTocPosType* .</span><span class="sxs-lookup"><span data-stu-id="0a4c8-110">The following methods have an *enumTocPosType* parameter.</span></span>

-   [<span data-ttu-id="0a4c8-111">**GetTocCount**</span><span class="sxs-lookup"><span data-stu-id="0a4c8-111">**GetTocCount**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [<span data-ttu-id="0a4c8-112">**GetTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="0a4c8-112">**GetTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [<span data-ttu-id="0a4c8-113">**GetTocByType**</span><span class="sxs-lookup"><span data-stu-id="0a4c8-113">**GetTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [<span data-ttu-id="0a4c8-114">**AddToc**</span><span class="sxs-lookup"><span data-stu-id="0a4c8-114">**AddToc**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [<span data-ttu-id="0a4c8-115">**RemoveTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="0a4c8-115">**RemoveTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [<span data-ttu-id="0a4c8-116">**RemoveTocByType**</span><span class="sxs-lookup"><span data-stu-id="0a4c8-116">**RemoveTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a><span data-ttu-id="0a4c8-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a4c8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a4c8-118">Guide de programmation de l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="0a4c8-118">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 




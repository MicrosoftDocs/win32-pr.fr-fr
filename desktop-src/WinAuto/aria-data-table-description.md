---
title: Avertissement de la table de données ARIA
description: Avertissement de la table de données ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029732"
---
# <a name="aria-data-table-warning"></a><span data-ttu-id="dfccf-104">Avertissement de la table de données ARIA</span><span class="sxs-lookup"><span data-stu-id="dfccf-104">ARIA Data Table Warning</span></span>

## <a name="text"></a><span data-ttu-id="dfccf-105">Texte</span><span class="sxs-lookup"><span data-stu-id="dfccf-105">Text</span></span>

<span data-ttu-id="dfccf-106">La table contient des données, mais n’a pas de résumé ni d’attribut **Aria-DescribedBy** valide.</span><span class="sxs-lookup"><span data-stu-id="dfccf-106">Table contains data but has neither summary nor a valid **aria-describedby** attribute.</span></span>

## <a name="type"></a><span data-ttu-id="dfccf-107">Type</span><span class="sxs-lookup"><span data-stu-id="dfccf-107">Type</span></span>

<span data-ttu-id="dfccf-108">Avertissement</span><span class="sxs-lookup"><span data-stu-id="dfccf-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="dfccf-109">Description</span><span class="sxs-lookup"><span data-stu-id="dfccf-109">Description</span></span>

<span data-ttu-id="dfccf-110">Cet avertissement s’applique aux tableaux HTML contenant plusieurs cellules.</span><span class="sxs-lookup"><span data-stu-id="dfccf-110">This warning applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="dfccf-111">Elle ne s’applique pas aux tables avec `role="presentation"` , car celles-ci sont considérées comme des tables de disposition.</span><span class="sxs-lookup"><span data-stu-id="dfccf-111">It does not apply to tables with `role="presentation"` since these are considered to be layout tables.</span></span>

<span data-ttu-id="dfccf-112">Cet avertissement indique que la table est identifiée comme une table de données, mais qu’aucune description accessible n’est définie.</span><span class="sxs-lookup"><span data-stu-id="dfccf-112">This warning indicates that the table is identified as a data table but it doesn’t have an accessible description defined.</span></span>

> [!Note]  
> <span data-ttu-id="dfccf-113">Toutes les tables de données n’ont pas besoin d’une description accessible.</span><span class="sxs-lookup"><span data-stu-id="dfccf-113">Not all data tables are required to have an accessible description.</span></span> <span data-ttu-id="dfccf-114">Vous devez définir une description accessible si les utilisateurs ont besoin d’informations supplémentaires pour comprendre la structure et le contenu de la table de données.</span><span class="sxs-lookup"><span data-stu-id="dfccf-114">You should define an accessible description if users need more information to understand the data table structure and content.</span></span>

 

<span data-ttu-id="dfccf-115">Pour résoudre cet avertissement, définissez une description accessible à partir d’une table à l’aide de l’attribut Summary ou de l’attribut **Aria-DescribedBy** .</span><span class="sxs-lookup"><span data-stu-id="dfccf-115">To address this warning, define a table accessible description by using the summary attribute or the **aria-describedby** attribute.</span></span>

## <a name="example"></a><span data-ttu-id="dfccf-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="dfccf-116">Example</span></span>


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 





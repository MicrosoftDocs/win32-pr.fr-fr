---
description: Composants BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Composants BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204012"
---
# <a name="blob-components"></a><span data-ttu-id="d5658-103">Composants BLOB</span><span class="sxs-lookup"><span data-stu-id="d5658-103">BLOB Components</span></span>

<span data-ttu-id="d5658-104">Un objet BLOB (Binary Large Object) comprend les composants hiérarchiques suivants :</span><span class="sxs-lookup"><span data-stu-id="d5658-104">A binary large object (BLOB) includes the following hierarchical components:</span></span>

-   <span data-ttu-id="d5658-105">Propriétaires</span><span class="sxs-lookup"><span data-stu-id="d5658-105">Owners</span></span>
-   <span data-ttu-id="d5658-106">Catégories</span><span class="sxs-lookup"><span data-stu-id="d5658-106">Categories</span></span>
-   <span data-ttu-id="d5658-107">Balises</span><span class="sxs-lookup"><span data-stu-id="d5658-107">Tags</span></span>
-   <span data-ttu-id="d5658-108">Valeurs</span><span class="sxs-lookup"><span data-stu-id="d5658-108">Values</span></span>

## <a name="textual-representation"></a><span data-ttu-id="d5658-109">Représentation textuelle</span><span class="sxs-lookup"><span data-stu-id="d5658-109">Textual Representation</span></span>

<span data-ttu-id="d5658-110">Pour plus de commodité, les objets BLOB s’affichent dans le format propriétaire : catégorie : balise : valeur dans lequel ils apparaissent lorsqu’ils sont enregistrés dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="d5658-110">For convenience, BLOBs appear in the Owner:Category:Tag:Value format that they appear in when saved to a file.</span></span> <span data-ttu-id="d5658-111">La structure interne de l’objet BLOB est opaque, car elle représente les pointeurs et les tables.</span><span class="sxs-lookup"><span data-stu-id="d5658-111">The internal structure of the BLOB is opaque because it represents pointers and tables.</span></span> <span data-ttu-id="d5658-112">Par exemple, voici une entrée d’un objet BLOB qui peut être utilisée pour configurer un NPP :</span><span class="sxs-lookup"><span data-stu-id="d5658-112">For example, here is an entry from a BLOB that can be used to configure an NPP:</span></span>

``` syntax
NPP:Configure:BufferSize=32768
```

<span data-ttu-id="d5658-113">Le propriétaire est NPP.</span><span class="sxs-lookup"><span data-stu-id="d5658-113">The Owner is NPP.</span></span> <span data-ttu-id="d5658-114">La catégorie est configurer, la balise est BufferSize et la valeur est 32768.</span><span class="sxs-lookup"><span data-stu-id="d5658-114">The Category is Configure, the Tag is BufferSize, and the Value is 32768.</span></span>

 

 




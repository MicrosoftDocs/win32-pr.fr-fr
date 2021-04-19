---
title: Ressource curseur
description: Définit une bitmap qui définit la forme du curseur sur l’écran d’affichage ou un curseur animé.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menus des ressources de curseur et autres ressources
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511487"
---
# <a name="cursor-resource"></a><span data-ttu-id="e4b1b-104">Ressource curseur</span><span class="sxs-lookup"><span data-stu-id="e4b1b-104">CURSOR resource</span></span>

<span data-ttu-id="e4b1b-105">Définit une bitmap qui définit la forme du curseur sur l’écran d’affichage ou un curseur animé.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-105">Defines a bitmap that defines the shape of the cursor on the display screen or an animated cursor.</span></span>

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a><span data-ttu-id="e4b1b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4b1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b1b-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="e4b1b-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="e4b1b-108">Nom unique ou entier 16 bits non signé identifiant la ressource.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-108">Unique name or a 16-bit unsigned integer identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e4b1b-109"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="e4b1b-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="e4b1b-110">Nom du fichier qui contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="e4b1b-111">Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="e4b1b-112">Le chemin d’accès doit être une chaîne entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="e4b1b-113">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="e4b1b-114">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e4b1b-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b1b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e4b1b-115">Remarks</span></span>

<span data-ttu-id="e4b1b-116">Les ressources icône et curseur peuvent contenir plusieurs images.</span><span class="sxs-lookup"><span data-stu-id="e4b1b-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="e4b1b-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="e4b1b-117">Examples</span></span>

<span data-ttu-id="e4b1b-118">L’exemple suivant définit deux ressources de curseur ; un par nom (Cursor1) et l’autre par numéro (2) :</span><span class="sxs-lookup"><span data-stu-id="e4b1b-118">The following example defines two cursor resources; one by name (cursor1) and the other by number (2):</span></span>

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a><span data-ttu-id="e4b1b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4b1b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b1b-120">Utilisation de curseurs</span><span class="sxs-lookup"><span data-stu-id="e4b1b-120">Using Cursors</span></span>](./using-cursors.md)
</dt> </dl>

 

 
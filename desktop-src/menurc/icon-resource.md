---
title: Ressource icône
description: Définit une bitmap qui définit la forme de l’icône à utiliser pour une application donnée ou une icône animée.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ICÔNES des menus des ressources et d’autres ressources
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507878"
---
# <a name="icon-resource"></a><span data-ttu-id="be675-104">Ressource icône</span><span class="sxs-lookup"><span data-stu-id="be675-104">ICON resource</span></span>

<span data-ttu-id="be675-105">Définit une bitmap qui définit la forme de l’icône à utiliser pour une application donnée ou une icône animée.</span><span class="sxs-lookup"><span data-stu-id="be675-105">Defines a bitmap that defines the shape of the icon to be used for a given application or an animated icon.</span></span>

``` syntax
nameID ICON filename
```

## <a name="parameters"></a><span data-ttu-id="be675-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be675-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be675-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="be675-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="be675-108">Nom unique ou valeur d’entier non signé 16 bits identifiant la ressource.</span><span class="sxs-lookup"><span data-stu-id="be675-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="be675-109"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="be675-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="be675-110">Nom du fichier qui contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="be675-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="be675-111">Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="be675-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="be675-112">Le chemin d’accès doit être une chaîne entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="be675-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="be675-113">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="be675-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="be675-114">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="be675-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be675-115">Notes</span><span class="sxs-lookup"><span data-stu-id="be675-115">Remarks</span></span>

<span data-ttu-id="be675-116">Les ressources icône et curseur peuvent contenir plusieurs images.</span><span class="sxs-lookup"><span data-stu-id="be675-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="be675-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="be675-117">Examples</span></span>

<span data-ttu-id="be675-118">L’exemple suivant définit deux ressources d’icône :</span><span class="sxs-lookup"><span data-stu-id="be675-118">The following example defines two icon resources:</span></span>

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a><span data-ttu-id="be675-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be675-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be675-120">Utilisation des icônes</span><span class="sxs-lookup"><span data-stu-id="be675-120">Using Icons</span></span>](./using-icons.md)
</dt> </dl>

 

 
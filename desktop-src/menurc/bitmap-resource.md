---
title: Ressource BITMAP
description: Définit une image bitmap qu’une application utilise dans son affichage d’écran ou en tant qu’élément dans un menu ou un contrôle.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menus des ressources BITMAP et autres ressources
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381850"
---
# <a name="bitmap-resource"></a><span data-ttu-id="61ef6-104">Ressource BITMAP</span><span class="sxs-lookup"><span data-stu-id="61ef6-104">BITMAP resource</span></span>

<span data-ttu-id="61ef6-105">Définit une image bitmap qu’une application utilise dans son affichage d’écran ou en tant qu’élément dans un menu ou un contrôle.</span><span class="sxs-lookup"><span data-stu-id="61ef6-105">Defines a bitmap that an application uses in its screen display or as an item in a menu or control.</span></span>

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a><span data-ttu-id="61ef6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61ef6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61ef6-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="61ef6-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="61ef6-108">Nom unique ou valeur d’entier non signé 16 bits identifiant la ressource.</span><span class="sxs-lookup"><span data-stu-id="61ef6-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="61ef6-109"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="61ef6-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="61ef6-110">Nom du fichier qui contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="61ef6-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="61ef6-111">Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="61ef6-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="61ef6-112">Le chemin d’accès doit être une chaîne entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="61ef6-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="61ef6-113">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="61ef6-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="61ef6-114">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="61ef6-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="61ef6-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="61ef6-115">Examples</span></span>

<span data-ttu-id="61ef6-116">L’exemple suivant définit deux ressources bitmap :</span><span class="sxs-lookup"><span data-stu-id="61ef6-116">The following example defines two bitmap resources:</span></span>

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a><span data-ttu-id="61ef6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61ef6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ef6-118">Utilisation des bitmaps</span><span class="sxs-lookup"><span data-stu-id="61ef6-118">Using Bitmaps</span></span>](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[<span data-ttu-id="61ef6-119">**LoadBitmap**</span><span class="sxs-lookup"><span data-stu-id="61ef6-119">**LoadBitmap**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[<span data-ttu-id="61ef6-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="61ef6-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 
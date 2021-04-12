---
title: Contrôle ICON
description: Définit un contrôle d’icône. Ce contrôle est une icône affichée dans une boîte de dialogue.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menus de contrôle d’icône et autres ressources
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462546"
---
# <a name="icon-control"></a><span data-ttu-id="dbe80-105">Contrôle ICON</span><span class="sxs-lookup"><span data-stu-id="dbe80-105">ICON control</span></span>

<span data-ttu-id="dbe80-106">Définit un contrôle d’icône.</span><span class="sxs-lookup"><span data-stu-id="dbe80-106">Defines an icon control.</span></span> <span data-ttu-id="dbe80-107">Ce contrôle est une icône affichée dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dbe80-107">This control is an icon displayed in a dialog box.</span></span>

<span data-ttu-id="dbe80-108">L’instruction de contrôle **Icon** , que vous pouvez utiliser uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit l’identificateur de ressource d’icône, l’identificateur de contrôle d’icône, la position et les attributs d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="dbe80-108">The **ICON** control statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the icon-resource identifier, icon-control identifier, position, and attributes of a control.</span></span>

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="dbe80-109"><span id="text"></span><span id="TEXT"></span>*financière*</span><span class="sxs-lookup"><span data-stu-id="dbe80-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="dbe80-110">Nom d’une icône (pas un nom de fichier) définie ailleurs dans le fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="dbe80-110">Name of an icon (not a file name) defined elsewhere in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="dbe80-111"><span id="width"></span><span id="WIDTH"></span>*Largeur*</span><span class="sxs-lookup"><span data-stu-id="dbe80-111"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="dbe80-112">Cette valeur est ignorée et doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="dbe80-112">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dbe80-113"><span id="height"></span><span id="HEIGHT"></span>*celle*</span><span class="sxs-lookup"><span data-stu-id="dbe80-113"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="dbe80-114">Cette valeur est ignorée et doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="dbe80-114">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dbe80-115"><span id="style"></span><span id="STYLE"></span>*style*</span><span class="sxs-lookup"><span data-stu-id="dbe80-115"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="dbe80-116">Style de contrôle.</span><span class="sxs-lookup"><span data-stu-id="dbe80-116">Control style.</span></span> <span data-ttu-id="dbe80-117">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="dbe80-117">This parameter is optional.</span></span> <span data-ttu-id="dbe80-118">La seule valeur pouvant être spécifiée est le style **d' \_ icône SS** .</span><span class="sxs-lookup"><span data-stu-id="dbe80-118">The only value that can be specified is the **SS\_ICON** style.</span></span> <span data-ttu-id="dbe80-119">Il s’agit du style par défaut, que ce paramètre soit spécifié ou non.</span><span class="sxs-lookup"><span data-stu-id="dbe80-119">This is the default style whether this parameter is specified or not.</span></span>

</dd> </dl>

<span data-ttu-id="dbe80-120">Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dbe80-120">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dbe80-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="dbe80-121">Examples</span></span>

<span data-ttu-id="dbe80-122">Cet exemple définit un contrôle Icon dont l’identificateur d’icône est 901 et dont le nom est myicon :</span><span class="sxs-lookup"><span data-stu-id="dbe80-122">This example defines an icon control whose icon identifier is 901 and whose name is myicon:</span></span>

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a><span data-ttu-id="dbe80-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe80-124">**SITUÉE**</span><span class="sxs-lookup"><span data-stu-id="dbe80-124">**ICON**</span></span>](icon-resource.md)
</dt> </dl>

 

 





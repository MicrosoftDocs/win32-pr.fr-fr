---
description: Ajoute un élément à Microsoft Active Desktop.
title: Méthode ShellUIHelper. AddDesktopComponent (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842460"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="bd45d-103">Méthode ShellUIHelper. AddDesktopComponent</span><span class="sxs-lookup"><span data-stu-id="bd45d-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="bd45d-104">Ajoute un élément à Microsoft Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="bd45d-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd45d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd45d-105">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a><span data-ttu-id="bd45d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd45d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd45d-107">*surl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45d-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="bd45d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="bd45d-109">Valeur de **chaîne** qui spécifie l’URL du nouvel élément favori.</span><span class="sxs-lookup"><span data-stu-id="bd45d-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="bd45d-110">*sSpécification* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45d-111">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="bd45d-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="bd45d-112">Valeur de **chaîne** qui spécifie le type d’élément ajouté.</span><span class="sxs-lookup"><span data-stu-id="bd45d-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="bd45d-113">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bd45d-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="bd45d-114">image</span><span class="sxs-lookup"><span data-stu-id="bd45d-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="bd45d-115">Le composant est une image.</span><span class="sxs-lookup"><span data-stu-id="bd45d-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="bd45d-116">hameçonnage</span><span class="sxs-lookup"><span data-stu-id="bd45d-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="bd45d-117">Le composant est un site Web.</span><span class="sxs-lookup"><span data-stu-id="bd45d-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bd45d-118">À *gauche* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45d-119">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="bd45d-119">Type: **Variant**</span></span>

<span data-ttu-id="bd45d-120">Position du bord gauche du composant, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="bd45d-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="bd45d-121">En *haut* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45d-122">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="bd45d-122">Type: **Variant**</span></span>

<span data-ttu-id="bd45d-123">Position du bord supérieur du composant, en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="bd45d-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="bd45d-124">*Largeur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45d-125">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="bd45d-125">Type: **Variant**</span></span>

<span data-ttu-id="bd45d-126">Largeur du composant, en unités d’écran.</span><span class="sxs-lookup"><span data-stu-id="bd45d-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="bd45d-127">*Hauteur* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd45d-128">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="bd45d-128">Type: **Variant**</span></span>

<span data-ttu-id="bd45d-129">Hauteur du composant, en unités d’écran.</span><span class="sxs-lookup"><span data-stu-id="bd45d-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bd45d-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="bd45d-130">Examples</span></span>

<span data-ttu-id="bd45d-131">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bd45d-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="bd45d-132">Langage</span><span class="sxs-lookup"><span data-stu-id="bd45d-132">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



<span data-ttu-id="bd45d-133">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="bd45d-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bd45d-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bd45d-134">Requirements</span></span>



| <span data-ttu-id="bd45d-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd45d-135">Requirement</span></span> | <span data-ttu-id="bd45d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd45d-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd45d-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd45d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bd45d-138">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bd45d-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd45d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bd45d-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd45d-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bd45d-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd45d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd45d-142"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd45d-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="bd45d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bd45d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd45d-144"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="bd45d-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 

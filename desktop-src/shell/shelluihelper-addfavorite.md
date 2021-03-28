---
description: Affiche l’interface utilisateur par défaut pour la création d’un élément favori. L’interface utilisateur est initialisée avec les paramètres spécifiés.
title: Méthode ShellUIHelper. AddFavorite (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973734"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="fe94f-104">Méthode ShellUIHelper. AddFavorite</span><span class="sxs-lookup"><span data-stu-id="fe94f-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="fe94f-105">Affiche l’interface utilisateur par défaut pour la création d’un élément favori.</span><span class="sxs-lookup"><span data-stu-id="fe94f-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="fe94f-106">L’interface utilisateur est initialisée avec les paramètres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fe94f-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe94f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe94f-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="fe94f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe94f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe94f-109">*surl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe94f-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe94f-110">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fe94f-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fe94f-111">Valeur de **chaîne** qui spécifie l’URL de l’élément à ajouter au dossier **favoris** .</span><span class="sxs-lookup"><span data-stu-id="fe94f-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="fe94f-112">*vTitle* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fe94f-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe94f-113">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="fe94f-113">Type: \**Variant\** _</span></span>

<span data-ttu-id="fe94f-114">Valeur _ *Variant*\* qui spécifie le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="fe94f-114">A _ *Variant*\* value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="fe94f-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="fe94f-115">Examples</span></span>

<span data-ttu-id="fe94f-116">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fe94f-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="fe94f-117">Langage</span><span class="sxs-lookup"><span data-stu-id="fe94f-117">JScript:</span></span>


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
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



<span data-ttu-id="fe94f-118">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="fe94f-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fe94f-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe94f-119">Requirements</span></span>



| <span data-ttu-id="fe94f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe94f-120">Requirement</span></span> | <span data-ttu-id="fe94f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe94f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe94f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe94f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fe94f-123">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe94f-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fe94f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe94f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fe94f-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe94f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe94f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe94f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe94f-127"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe94f-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="fe94f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fe94f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe94f-129"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fe94f-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 

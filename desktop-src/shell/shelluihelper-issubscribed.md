---
description: Indique si une URL spécifiée est abonnée à.
title: Méthode ShellUIHelper. IsSubscribed (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: ca68d2e46ce74593b66aac6f995b88ddcb79796b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842490"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="11fc7-103">Méthode ShellUIHelper. IsSubscribed</span><span class="sxs-lookup"><span data-stu-id="11fc7-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="11fc7-104">Indique si une URL spécifiée est abonnée à.</span><span class="sxs-lookup"><span data-stu-id="11fc7-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="11fc7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11fc7-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="11fc7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11fc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fc7-107">*surl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11fc7-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11fc7-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="11fc7-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="11fc7-109">Valeur de **chaîne** qui spécifie l’URL.</span><span class="sxs-lookup"><span data-stu-id="11fc7-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fc7-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11fc7-110">Return value</span></span>

<span data-ttu-id="11fc7-111">Type : **booléen \***</span><span class="sxs-lookup"><span data-stu-id="11fc7-111">Type: **Boolean\***</span></span>

<span data-ttu-id="11fc7-112">**true** si l’URL est abonnée à ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="11fc7-112">**true** if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="11fc7-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="11fc7-113">Examples</span></span>

<span data-ttu-id="11fc7-114">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="11fc7-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="11fc7-115">Langage</span><span class="sxs-lookup"><span data-stu-id="11fc7-115">JScript:</span></span>


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
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



<span data-ttu-id="11fc7-116">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="11fc7-116">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="11fc7-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="11fc7-117">Requirements</span></span>



| <span data-ttu-id="11fc7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11fc7-118">Requirement</span></span> | <span data-ttu-id="11fc7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="11fc7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11fc7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11fc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="11fc7-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11fc7-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="11fc7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11fc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="11fc7-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11fc7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="11fc7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="11fc7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="11fc7-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11fc7-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="11fc7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="11fc7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11fc7-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="11fc7-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 

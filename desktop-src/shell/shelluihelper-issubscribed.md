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
ms.openlocfilehash: 2085f38e5f91f13a2f67ff4f22b003b533249386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034671"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="4802d-103">Méthode ShellUIHelper. IsSubscribed</span><span class="sxs-lookup"><span data-stu-id="4802d-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="4802d-104">Indique si une URL spécifiée est abonnée à.</span><span class="sxs-lookup"><span data-stu-id="4802d-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="4802d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4802d-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="4802d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4802d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4802d-107">*surl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4802d-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4802d-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4802d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4802d-109">Valeur de **chaîne** qui spécifie l’URL.</span><span class="sxs-lookup"><span data-stu-id="4802d-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4802d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4802d-110">Return value</span></span>

<span data-ttu-id="4802d-111">Type : \**booléen \** _</span><span class="sxs-lookup"><span data-stu-id="4802d-111">Type: \**Boolean\** _</span></span>

<span data-ttu-id="4802d-112">_ *true*\* si l’URL est abonnée à ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="4802d-112">_ *true*\* if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="4802d-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="4802d-113">Examples</span></span>

<span data-ttu-id="4802d-114">L’exemple suivant illustre l’utilisation correcte de cette méthode pour JScript Embedded en HTML et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4802d-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="4802d-115">Langage</span><span class="sxs-lookup"><span data-stu-id="4802d-115">JScript:</span></span>


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



<span data-ttu-id="4802d-116">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="4802d-116">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4802d-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4802d-117">Requirements</span></span>



| <span data-ttu-id="4802d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4802d-118">Requirement</span></span> | <span data-ttu-id="4802d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4802d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4802d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4802d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4802d-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4802d-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4802d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4802d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4802d-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4802d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4802d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4802d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4802d-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4802d-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="4802d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4802d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4802d-127"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="4802d-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 

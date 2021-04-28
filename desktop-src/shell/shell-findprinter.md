---
description: Shell. FindPrinter, méthode-affiche la boîte de dialogue Rechercher l’imprimante.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Shell. FindPrinter, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104307"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="87147-103">Shell. FindPrinter, méthode</span><span class="sxs-lookup"><span data-stu-id="87147-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="87147-104">Affiche la boîte de dialogue **Rechercher l’imprimante** .</span><span class="sxs-lookup"><span data-stu-id="87147-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="87147-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87147-105">Syntax</span></span>


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="87147-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87147-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87147-107">*sName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="87147-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87147-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="87147-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="87147-109">**Chaîne** qui contient le nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="87147-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="87147-110">*sLocation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="87147-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87147-111">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="87147-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="87147-112">**Chaîne** qui contient l’emplacement de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="87147-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="87147-113">*sModel* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="87147-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87147-114">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="87147-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="87147-115">**Chaîne** qui contient le modèle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="87147-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87147-116">Notes </span><span class="sxs-lookup"><span data-stu-id="87147-116">Remarks</span></span>

<span data-ttu-id="87147-117">Si vous assignez des chaînes à un ou plusieurs des paramètres facultatifs, ils s’affichent en tant que valeurs par défaut dans le contrôle d’édition associé lorsque la boîte de dialogue **Rechercher l’imprimante** est affichée.</span><span class="sxs-lookup"><span data-stu-id="87147-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="87147-118">L’utilisateur peut accepter ou remplacer ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="87147-118">The user can either accept or override these values.</span></span> <span data-ttu-id="87147-119">Si aucune valeur n’est assignée à un paramètre, la zone d’édition associée est vide et l’utilisateur doit entrer une valeur.</span><span class="sxs-lookup"><span data-stu-id="87147-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="87147-120">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="87147-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="87147-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="87147-121">Examples</span></span>

<span data-ttu-id="87147-122">Les exemples suivants illustrent l’utilisation de **FindPrinter** pour afficher la boîte de dialogue **Rechercher une imprimante** pour une application particulière.</span><span class="sxs-lookup"><span data-stu-id="87147-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="87147-123">L’utilisation est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="87147-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="87147-124">Langage</span><span class="sxs-lookup"><span data-stu-id="87147-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="87147-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="87147-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="87147-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87147-126">Requirements</span></span>



| <span data-ttu-id="87147-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87147-127">Requirement</span></span> | <span data-ttu-id="87147-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="87147-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87147-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87147-129">Minimum supported client</span></span><br/> | <span data-ttu-id="87147-130">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87147-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87147-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87147-131">Minimum supported server</span></span><br/> | <span data-ttu-id="87147-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87147-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="87147-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="87147-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="87147-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="87147-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="87147-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="87147-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87147-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87147-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="87147-137">DLL</span><span class="sxs-lookup"><span data-stu-id="87147-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87147-138"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="87147-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 

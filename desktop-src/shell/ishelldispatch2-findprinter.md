---
description: Affiche la boîte de dialogue Rechercher l’imprimante.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Méthode IShellDispatch2. FindPrinter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201710"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="c9f13-103">Méthode IShellDispatch2. FindPrinter</span><span class="sxs-lookup"><span data-stu-id="c9f13-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="c9f13-104">Affiche la boîte de dialogue **Rechercher l’imprimante** .</span><span class="sxs-lookup"><span data-stu-id="c9f13-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9f13-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="c9f13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9f13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f13-107">*sName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c9f13-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f13-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c9f13-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c9f13-109">**Chaîne** qui contient le nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c9f13-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="c9f13-110">*sLocation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c9f13-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f13-111">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c9f13-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c9f13-112">**Chaîne** qui contient l’emplacement de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c9f13-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="c9f13-113">*sModel* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c9f13-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f13-114">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c9f13-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c9f13-115">**Chaîne** qui contient le modèle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c9f13-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9f13-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c9f13-116">Remarks</span></span>

<span data-ttu-id="c9f13-117">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FindPrinter**](./shell-findprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f13-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="c9f13-118">Si vous assignez des chaînes à un ou plusieurs des paramètres facultatifs, ils s’affichent en tant que valeurs par défaut dans le contrôle d’édition associé lorsque la boîte de dialogue **Rechercher l’imprimante** est affichée.</span><span class="sxs-lookup"><span data-stu-id="c9f13-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="c9f13-119">L’utilisateur peut accepter ou remplacer ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c9f13-119">The user can either accept or override these values.</span></span> <span data-ttu-id="c9f13-120">Si aucune valeur n’est assignée à un paramètre, la zone d’édition associée est vide et l’utilisateur doit entrer une valeur.</span><span class="sxs-lookup"><span data-stu-id="c9f13-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="c9f13-121">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c9f13-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c9f13-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="c9f13-122">Examples</span></span>

<span data-ttu-id="c9f13-123">Les exemples suivants illustrent l’utilisation de **FindPrinter** pour afficher la boîte de dialogue **Rechercher une imprimante** pour une application particulière.</span><span class="sxs-lookup"><span data-stu-id="c9f13-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="c9f13-124">L’utilisation est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c9f13-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c9f13-125">Langage</span><span class="sxs-lookup"><span data-stu-id="c9f13-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="c9f13-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="c9f13-126">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c9f13-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c9f13-127">Requirements</span></span>



| <span data-ttu-id="c9f13-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9f13-128">Requirement</span></span> | <span data-ttu-id="c9f13-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9f13-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f13-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9f13-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f13-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9f13-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9f13-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9f13-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f13-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9f13-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c9f13-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9f13-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9f13-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9f13-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c9f13-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="c9f13-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9f13-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9f13-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c9f13-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c9f13-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9f13-139"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c9f13-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 

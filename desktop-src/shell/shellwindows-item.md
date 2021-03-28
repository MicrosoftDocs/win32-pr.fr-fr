---
description: Récupère un objet InternetExplorer qui représente la fenêtre de l’interpréteur de commandes.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: ShellWindows. Item, méthode (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203255"
---
# <a name="shellwindowsitem-method"></a><span data-ttu-id="83c82-103">ShellWindows. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="83c82-103">ShellWindows.Item method</span></span>

<span data-ttu-id="83c82-104">Récupère un objet [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) qui représente la fenêtre de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="83c82-104">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="83c82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83c82-105">Syntax</span></span>


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="83c82-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c82-107">*iIndex* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="83c82-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83c82-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="83c82-108">Type: **Variant**</span></span>

<span data-ttu-id="83c82-109">Index de base zéro de l'élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="83c82-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="83c82-110">Cette valeur doit être inférieure à la valeur de la propriété [**Count**](shellwindows-count.md) .</span><span class="sxs-lookup"><span data-stu-id="83c82-110">This value must be less than the value of the [**Count**](shellwindows-count.md) property.</span></span> <span data-ttu-id="83c82-111">Si cette valeur est omise, la valeur par défaut 0 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="83c82-111">If this value is omitted, a default value of 0 is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c82-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83c82-112">Return value</span></span>

<span data-ttu-id="83c82-113">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="83c82-113">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="83c82-114">Référence d’objet à l’objet [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) qui représente la fenêtre de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="83c82-114">An object reference to the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="examples"></a><span data-ttu-id="83c82-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="83c82-115">Examples</span></span>

<span data-ttu-id="83c82-116">L’exemple suivant utilise [**Item**](folderitemverbs-item.md) pour récupérer l’objet [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) qui représente le premier élément de la fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="83c82-116">The following example uses [**Item**](folderitemverbs-item.md) to retrieve the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the first Shell window item.</span></span> <span data-ttu-id="83c82-117">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="83c82-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="83c82-118">Langage</span><span class="sxs-lookup"><span data-stu-id="83c82-118">JScript:</span></span>


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



<span data-ttu-id="83c82-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="83c82-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="83c82-120">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="83c82-120">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="83c82-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="83c82-121">Requirements</span></span>



| <span data-ttu-id="83c82-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83c82-122">Requirement</span></span> | <span data-ttu-id="83c82-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="83c82-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c82-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c82-124">Minimum supported client</span></span><br/> | <span data-ttu-id="83c82-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83c82-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="83c82-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83c82-126">Minimum supported server</span></span><br/> | <span data-ttu-id="83c82-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83c82-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83c82-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="83c82-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c82-129"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c82-129"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="83c82-130">DLL</span><span class="sxs-lookup"><span data-stu-id="83c82-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83c82-131"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="83c82-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 

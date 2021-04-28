---
<span data-ttu-id="10620-101">Description : méthode Shell. FindComputer-affiche la boîte de dialogue résultats de la recherche : ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="10620-101">description: Shell.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="10620-102">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="10620-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="10620-103">ms. AssetID : 0304b955-AFDE-4DE4-824a-9ec9c9530360 title : Shell. FindComputer, méthode (shldisp. h) ms. topic : référence ms. Date : 05/31/2018 topic_type :</span><span class="sxs-lookup"><span data-stu-id="10620-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="10620-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="10620-104">APIRef</span></span>
- <span data-ttu-id="10620-105">api_name kbSyntax :</span><span class="sxs-lookup"><span data-stu-id="10620-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="10620-106">Api_type Shell. FindComputer :</span><span class="sxs-lookup"><span data-stu-id="10620-106">Shell.FindComputer api_type:</span></span> 
- <span data-ttu-id="10620-107">Api_location COM :</span><span class="sxs-lookup"><span data-stu-id="10620-107">COM api_location:</span></span> 
- <span data-ttu-id="10620-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="10620-108">Shell32.dll</span></span>
---

# <a name="shellfindcomputer-method"></a><span data-ttu-id="10620-109">Shell. FindComputer, méthode</span><span class="sxs-lookup"><span data-stu-id="10620-109">Shell.FindComputer method</span></span>

<span data-ttu-id="10620-110">Affiche la boîte de dialogue résultats de la **recherche : ordinateurs** .</span><span class="sxs-lookup"><span data-stu-id="10620-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="10620-111">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="10620-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="10620-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10620-112">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="10620-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10620-113">Parameters</span></span>

<span data-ttu-id="10620-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="10620-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10620-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="10620-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="10620-116">JScript</span><span class="sxs-lookup"><span data-stu-id="10620-116">JScript</span></span>

<span data-ttu-id="10620-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="10620-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="10620-118">VB</span><span class="sxs-lookup"><span data-stu-id="10620-118">VB</span></span>

<span data-ttu-id="10620-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="10620-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="10620-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="10620-120">Examples</span></span>

<span data-ttu-id="10620-121">L’exemple suivant montre **FindComputer** en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="10620-121">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="10620-122">Le résultat de ce code est le même que si vous appuyez sur le bouton **Démarrer** , sur **Rechercher**, sur l’option **imprimantes, ordinateurs ou personnes** , puis sur **un ordinateur sur le réseau**.</span><span class="sxs-lookup"><span data-stu-id="10620-122">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="10620-123">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="10620-123">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="10620-124">Langage</span><span class="sxs-lookup"><span data-stu-id="10620-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="10620-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="10620-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="10620-126">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="10620-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="10620-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10620-127">Requirements</span></span>



| <span data-ttu-id="10620-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10620-128">Requirement</span></span> | <span data-ttu-id="10620-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="10620-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10620-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10620-130">Minimum supported client</span></span><br/> | <span data-ttu-id="10620-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10620-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="10620-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10620-132">Minimum supported server</span></span><br/> | <span data-ttu-id="10620-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10620-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10620-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="10620-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="10620-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10620-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="10620-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="10620-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10620-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10620-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="10620-138">DLL</span><span class="sxs-lookup"><span data-stu-id="10620-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10620-139"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="10620-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





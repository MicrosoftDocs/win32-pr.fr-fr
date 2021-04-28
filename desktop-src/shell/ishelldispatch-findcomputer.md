---
<span data-ttu-id="38446-101">Description : IShellDispatch. FindComputer, méthode-affiche la boîte de dialogue résultats de la recherche : ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="38446-101">description: IShellDispatch.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="38446-102">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="38446-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="38446-103">ms. AssetID : 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title : IShellDispatch. FindComputer, méthode (shldisp. h) ms. topic : référence ms. Date : 05/31/2018 topic_type :</span><span class="sxs-lookup"><span data-stu-id="38446-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="38446-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="38446-104">APIRef</span></span>
- <span data-ttu-id="38446-105">api_name kbSyntax :</span><span class="sxs-lookup"><span data-stu-id="38446-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="38446-106">Api_type IShellDispatch. FindComputer :</span><span class="sxs-lookup"><span data-stu-id="38446-106">IShellDispatch.FindComputer api_type:</span></span> 
- <span data-ttu-id="38446-107">Api_location COM :</span><span class="sxs-lookup"><span data-stu-id="38446-107">COM api_location:</span></span> 
- <span data-ttu-id="38446-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="38446-108">Shell32.dll</span></span>
---

# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="38446-109">Méthode IShellDispatch. FindComputer</span><span class="sxs-lookup"><span data-stu-id="38446-109">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="38446-110">Affiche la boîte de dialogue résultats de la **recherche : ordinateurs** .</span><span class="sxs-lookup"><span data-stu-id="38446-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="38446-111">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="38446-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="38446-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38446-112">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="38446-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38446-113">Parameters</span></span>

<span data-ttu-id="38446-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="38446-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38446-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38446-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="38446-116">JScript</span><span class="sxs-lookup"><span data-stu-id="38446-116">JScript</span></span>

<span data-ttu-id="38446-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="38446-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="38446-118">VB</span><span class="sxs-lookup"><span data-stu-id="38446-118">VB</span></span>

<span data-ttu-id="38446-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="38446-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38446-120">Notes </span><span class="sxs-lookup"><span data-stu-id="38446-120">Remarks</span></span>

<span data-ttu-id="38446-121">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FindComputer**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="38446-121">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="38446-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="38446-122">Examples</span></span>

<span data-ttu-id="38446-123">Les exemples suivants illustrent l’utilisation de **FindComputer** dans JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="38446-123">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="38446-124">Langage</span><span class="sxs-lookup"><span data-stu-id="38446-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="38446-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="38446-125">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="38446-126">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="38446-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="38446-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38446-127">Requirements</span></span>



| <span data-ttu-id="38446-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38446-128">Requirement</span></span> | <span data-ttu-id="38446-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="38446-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38446-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38446-130">Minimum supported client</span></span><br/> | <span data-ttu-id="38446-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38446-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="38446-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38446-132">Minimum supported server</span></span><br/> | <span data-ttu-id="38446-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38446-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="38446-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="38446-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="38446-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38446-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="38446-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="38446-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38446-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38446-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="38446-138">DLL</span><span class="sxs-lookup"><span data-stu-id="38446-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38446-139"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="38446-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





---
description: IShellDispatch2. ShellExecute, méthode-effectue une opération spécifiée sur un fichier spécifié.
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: IShellDispatch2. ShellExecute, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117017"
---
# <a name="ishelldispatch2shellexecute-method"></a><span data-ttu-id="04c5b-103">IShellDispatch2. ShellExecute, méthode</span><span class="sxs-lookup"><span data-stu-id="04c5b-103">IShellDispatch2.ShellExecute method</span></span>

<span data-ttu-id="04c5b-104">Exécute une opération spécifiée sur un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="04c5b-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04c5b-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="04c5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04c5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04c5b-107">*sFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04c5b-107">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04c5b-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="04c5b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="04c5b-109">**Chaîne** qui contient le nom du fichier sur lequel **ShellExecute** effectue l’action spécifiée par *vOperation*.</span><span class="sxs-lookup"><span data-stu-id="04c5b-109">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="04c5b-110">*vArguments* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="04c5b-110">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04c5b-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="04c5b-111">Type: **Variant**</span></span>

<span data-ttu-id="04c5b-112">Chaîne qui contient les valeurs des paramètres de l’opération.</span><span class="sxs-lookup"><span data-stu-id="04c5b-112">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="04c5b-113">*vDirectory* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="04c5b-113">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04c5b-114">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="04c5b-114">Type: **Variant**</span></span>

<span data-ttu-id="04c5b-115">Chemin d’accès complet du répertoire qui contient le fichier spécifié par *sFile*.</span><span class="sxs-lookup"><span data-stu-id="04c5b-115">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="04c5b-116">Si ce paramètre n’est pas spécifié, le répertoire de travail actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="04c5b-116">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="04c5b-117">*vOperation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="04c5b-117">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04c5b-118">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="04c5b-118">Type: **Variant**</span></span>

<span data-ttu-id="04c5b-119">Opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="04c5b-119">The operation to be performed.</span></span> <span data-ttu-id="04c5b-120">Cette valeur est définie sur l’une des chaînes de verbe qui est prise en charge par le fichier.</span><span class="sxs-lookup"><span data-stu-id="04c5b-120">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="04c5b-121">Pour plus d’informations sur les verbes, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="04c5b-121">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="04c5b-122">Si ce paramètre n’est pas spécifié, l’opération par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="04c5b-122">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="04c5b-123">*vShow* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="04c5b-123">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="04c5b-124">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="04c5b-124">Type: **Variant**</span></span>

<span data-ttu-id="04c5b-125">Recommandation relative à l’affichage initial de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="04c5b-125">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="04c5b-126">L’application peut ignorer cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="04c5b-126">The application can ignore this recommendation.</span></span> <span data-ttu-id="04c5b-127">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="04c5b-127">This parameter can be one of the following values.</span></span> <span data-ttu-id="04c5b-128">Si ce paramètre n’est pas spécifié, l’application utilise sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="04c5b-128">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="04c5b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c5b-129">Value</span></span>                                                                                                                               | <span data-ttu-id="04c5b-130">Signification</span><span class="sxs-lookup"><span data-stu-id="04c5b-130">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04c5b-131"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-131"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="04c5b-132">Ouvrez l’application à l’aide d’une fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="04c5b-132">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="04c5b-133"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-133"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="04c5b-134">Ouvrez l’application avec une fenêtre normale.</span><span class="sxs-lookup"><span data-stu-id="04c5b-134">Open the application with a normal window.</span></span> <span data-ttu-id="04c5b-135">Si la fenêtre est réduite ou agrandie, le système la restaure à sa taille et à sa position d’origine.</span><span class="sxs-lookup"><span data-stu-id="04c5b-135">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="04c5b-136"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-136"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="04c5b-137">Ouvrez l’application avec une fenêtre réduite.</span><span class="sxs-lookup"><span data-stu-id="04c5b-137">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="04c5b-138"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-138"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="04c5b-139">Ouvrez l’application avec une fenêtre agrandie.</span><span class="sxs-lookup"><span data-stu-id="04c5b-139">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="04c5b-140"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-140"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="04c5b-141">Ouvre l’application avec sa fenêtre à sa taille et à sa position les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="04c5b-141">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="04c5b-142">La fenêtre active reste active.</span><span class="sxs-lookup"><span data-stu-id="04c5b-142">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="04c5b-143"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-143"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="04c5b-144">Ouvre l’application avec sa fenêtre à sa taille et à sa position actuelles.</span><span class="sxs-lookup"><span data-stu-id="04c5b-144">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="04c5b-145"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-145"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="04c5b-146">Ouvrez l’application avec une fenêtre réduite.</span><span class="sxs-lookup"><span data-stu-id="04c5b-146">Open the application with a minimized window.</span></span> <span data-ttu-id="04c5b-147">La fenêtre active reste active.</span><span class="sxs-lookup"><span data-stu-id="04c5b-147">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="04c5b-148"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-148"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="04c5b-149">Ouvre l’application avec sa fenêtre dans l’État par défaut spécifié par l’application.</span><span class="sxs-lookup"><span data-stu-id="04c5b-149">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04c5b-150">Notes </span><span class="sxs-lookup"><span data-stu-id="04c5b-150">Remarks</span></span>

<span data-ttu-id="04c5b-151">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ShellExecute**](./shell-shellexecute.md) .</span><span class="sxs-lookup"><span data-stu-id="04c5b-151">This method is implemented and accessed through the [**Shell.ShellExecute**](./shell-shellexecute.md) method.</span></span>

<span data-ttu-id="04c5b-152">Cette méthode est équivalente au lancement de l’une des commandes associées au menu contextuel d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="04c5b-152">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="04c5b-153">Chaque commande est représentée par une chaîne de verbe.</span><span class="sxs-lookup"><span data-stu-id="04c5b-153">Each command is represented by a verb string.</span></span> <span data-ttu-id="04c5b-154">L’ensemble des verbes pris en charge varie d’un fichier à un fichier.</span><span class="sxs-lookup"><span data-stu-id="04c5b-154">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="04c5b-155">Le verbe le plus couramment pris en charge est « Open », qui est généralement le verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="04c5b-155">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="04c5b-156">Les autres verbes peuvent être pris en charge uniquement par certains types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="04c5b-156">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="04c5b-157">Pour plus d’informations sur les verbes de Shell, consultez [lancement d’applications](launch.md) ou [extension des menus contextuels](context.md).</span><span class="sxs-lookup"><span data-stu-id="04c5b-157">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="04c5b-158">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="04c5b-158">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="04c5b-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="04c5b-159">Examples</span></span>

<span data-ttu-id="04c5b-160">Les exemples suivants illustrent l’utilisation de **ShellExecute** pour ouvrir le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="04c5b-160">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="04c5b-161">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="04c5b-161">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="04c5b-162">Langage</span><span class="sxs-lookup"><span data-stu-id="04c5b-162">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



<span data-ttu-id="04c5b-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="04c5b-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="04c5b-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04c5b-164">Requirements</span></span>



| <span data-ttu-id="04c5b-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04c5b-165">Requirement</span></span> | <span data-ttu-id="04c5b-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="04c5b-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04c5b-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04c5b-167">Minimum supported client</span></span><br/> | <span data-ttu-id="04c5b-168">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04c5b-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04c5b-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04c5b-169">Minimum supported server</span></span><br/> | <span data-ttu-id="04c5b-170">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04c5b-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="04c5b-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="04c5b-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="04c5b-172"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="04c5b-173">MIDL</span><span class="sxs-lookup"><span data-stu-id="04c5b-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04c5b-174"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="04c5b-175">DLL</span><span class="sxs-lookup"><span data-stu-id="04c5b-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04c5b-176"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="04c5b-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 

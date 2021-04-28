---
description: Shell. ShellExecute, méthode-effectue une opération spécifiée sur un fichier spécifié.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Méthode Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0fd31f0859fff5a1c94d5586f287e4a8980ddc02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104127"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="978f8-103">Shell. ShellExecute, méthode</span><span class="sxs-lookup"><span data-stu-id="978f8-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="978f8-104">Exécute une opération spécifiée sur un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="978f8-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="978f8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="978f8-105">Syntax</span></span>

<span data-ttu-id="978f8-106">Langage</span><span class="sxs-lookup"><span data-stu-id="978f8-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="978f8-107">VBScript</span><span class="sxs-lookup"><span data-stu-id="978f8-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="978f8-108">VB :</span><span class="sxs-lookup"><span data-stu-id="978f8-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="978f8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="978f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978f8-110">*sFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="978f8-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="978f8-111">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="978f8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="978f8-112">**Chaîne** qui contient le nom du fichier sur lequel **ShellExecute** effectue l’action spécifiée par *vOperation*.</span><span class="sxs-lookup"><span data-stu-id="978f8-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="978f8-113">*vArguments* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="978f8-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="978f8-114">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="978f8-114">Type: **Variant**</span></span>

<span data-ttu-id="978f8-115">Chaîne qui contient les valeurs des paramètres de l’opération.</span><span class="sxs-lookup"><span data-stu-id="978f8-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="978f8-116">*vDirectory* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="978f8-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="978f8-117">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="978f8-117">Type: **Variant**</span></span>

<span data-ttu-id="978f8-118">Chemin d’accès complet du répertoire qui contient le fichier spécifié par *sFile*.</span><span class="sxs-lookup"><span data-stu-id="978f8-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="978f8-119">Si ce paramètre n’est pas spécifié, le répertoire de travail actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="978f8-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="978f8-120">*vOperation* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="978f8-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="978f8-121">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="978f8-121">Type: **Variant**</span></span>

<span data-ttu-id="978f8-122">Opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="978f8-122">The operation to be performed.</span></span> <span data-ttu-id="978f8-123">Cette valeur est définie sur l’une des chaînes de verbe qui est prise en charge par le fichier.</span><span class="sxs-lookup"><span data-stu-id="978f8-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="978f8-124">Pour plus d’informations sur les verbes, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="978f8-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="978f8-125">Si ce paramètre n’est pas spécifié, l’opération par défaut est effectuée.</span><span class="sxs-lookup"><span data-stu-id="978f8-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="978f8-126">*vShow* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="978f8-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="978f8-127">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="978f8-127">Type: **Variant**</span></span>

<span data-ttu-id="978f8-128">Recommandation relative à l’affichage initial de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="978f8-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="978f8-129">L’application peut ignorer cette recommandation.</span><span class="sxs-lookup"><span data-stu-id="978f8-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="978f8-130">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="978f8-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="978f8-131">Si ce paramètre n’est pas spécifié, l’application utilise sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="978f8-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="978f8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="978f8-132">Value</span></span>                                                                                                                               | <span data-ttu-id="978f8-133">Signification</span><span class="sxs-lookup"><span data-stu-id="978f8-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="978f8-134"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="978f8-135">Ouvrez l’application à l’aide d’une fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="978f8-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="978f8-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="978f8-137">Ouvrez l’application avec une fenêtre normale.</span><span class="sxs-lookup"><span data-stu-id="978f8-137">Open the application with a normal window.</span></span> <span data-ttu-id="978f8-138">Si la fenêtre est réduite ou agrandie, le système la restaure à sa taille et à sa position d’origine.</span><span class="sxs-lookup"><span data-stu-id="978f8-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="978f8-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="978f8-140">Ouvrez l’application avec une fenêtre réduite.</span><span class="sxs-lookup"><span data-stu-id="978f8-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="978f8-141"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="978f8-142">Ouvrez l’application avec une fenêtre agrandie.</span><span class="sxs-lookup"><span data-stu-id="978f8-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="978f8-143"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="978f8-144">Ouvre l’application avec sa fenêtre à sa taille et à sa position les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="978f8-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="978f8-145">La fenêtre active reste active.</span><span class="sxs-lookup"><span data-stu-id="978f8-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="978f8-146"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="978f8-147">Ouvre l’application avec sa fenêtre à sa taille et à sa position actuelles.</span><span class="sxs-lookup"><span data-stu-id="978f8-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="978f8-148"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="978f8-149">Ouvrez l’application avec une fenêtre réduite.</span><span class="sxs-lookup"><span data-stu-id="978f8-149">Open the application with a minimized window.</span></span> <span data-ttu-id="978f8-150">La fenêtre active reste active.</span><span class="sxs-lookup"><span data-stu-id="978f8-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="978f8-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="978f8-152">Ouvre l’application avec sa fenêtre dans l’État par défaut spécifié par l’application.</span><span class="sxs-lookup"><span data-stu-id="978f8-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="978f8-153">Notes </span><span class="sxs-lookup"><span data-stu-id="978f8-153">Remarks</span></span>

<span data-ttu-id="978f8-154">Cette méthode est équivalente au lancement de l’une des commandes associées au menu contextuel d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="978f8-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="978f8-155">Chaque commande est représentée par une chaîne de verbe.</span><span class="sxs-lookup"><span data-stu-id="978f8-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="978f8-156">L’ensemble des verbes pris en charge varie d’un fichier à un fichier.</span><span class="sxs-lookup"><span data-stu-id="978f8-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="978f8-157">Le verbe le plus couramment pris en charge est « Open », qui est généralement le verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="978f8-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="978f8-158">Les autres verbes peuvent être pris en charge uniquement par certains types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="978f8-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="978f8-159">Pour plus d’informations sur les verbes de Shell, consultez [lancement d’applications](launch.md) ou [extension des menus contextuels](context.md).</span><span class="sxs-lookup"><span data-stu-id="978f8-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="978f8-160">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="978f8-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="978f8-161">Exemples</span><span class="sxs-lookup"><span data-stu-id="978f8-161">Examples</span></span>

<span data-ttu-id="978f8-162">Les exemples suivants illustrent l’utilisation de **ShellExecute** pour ouvrir le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="978f8-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="978f8-163">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="978f8-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="978f8-164">Langage</span><span class="sxs-lookup"><span data-stu-id="978f8-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="978f8-165">VBScript</span><span class="sxs-lookup"><span data-stu-id="978f8-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="978f8-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="978f8-166">Requirements</span></span>



| <span data-ttu-id="978f8-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="978f8-167">Requirement</span></span> | <span data-ttu-id="978f8-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="978f8-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="978f8-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="978f8-169">Minimum supported client</span></span><br/> | <span data-ttu-id="978f8-170">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="978f8-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="978f8-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="978f8-171">Minimum supported server</span></span><br/> | <span data-ttu-id="978f8-172">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="978f8-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="978f8-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="978f8-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="978f8-174"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="978f8-175">MIDL</span><span class="sxs-lookup"><span data-stu-id="978f8-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="978f8-176"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="978f8-177">DLL</span><span class="sxs-lookup"><span data-stu-id="978f8-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="978f8-178"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="978f8-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 

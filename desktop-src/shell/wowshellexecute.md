---
description: Effectue une opération sur un fichier spécifié.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106533529"
---
# <a name="wowshellexecute-function"></a><span data-ttu-id="c4469-103">WOWShellExecute fonction)</span><span class="sxs-lookup"><span data-stu-id="c4469-103">WOWShellExecute function</span></span>

<span data-ttu-id="c4469-104">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c4469-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="c4469-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4469-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c4469-106">Effectue une opération sur un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c4469-106">Performs an operation on a specified file.</span></span> <span data-ttu-id="c4469-107">**WOWShellExecute** existe uniquement pour une utilisation avec la machine DOS virtuelle Microsoft Windows NT (Ntvdm.exe), qui permet d’exécuter le système d’exploitation sur disque (dos) et le logiciel 16 bits sur un système Windows, et ne doit pas être utilisé par une autre personne.</span><span class="sxs-lookup"><span data-stu-id="c4469-107">**WOWShellExecute** exists only for use with the Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), which allows disk operating system (DOS) and 16-bit software to run on a Windows system, and should not be used by anyone else.</span></span> <span data-ttu-id="c4469-108">Utilisez à la place [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="c4469-108">Use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4469-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4469-109">Syntax</span></span>


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a><span data-ttu-id="c4469-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4469-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4469-111">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4469-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4469-112">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="c4469-112">Type: **HWND**</span></span>

<span data-ttu-id="c4469-113">Handle de la fenêtre propriétaire utilisée pour afficher une interface utilisateur ou des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c4469-113">A handle to the owner window used for displaying a UI or error messages.</span></span> <span data-ttu-id="c4469-114">Cette valeur peut être **null** si l’opération n’est pas associée à une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c4469-114">This value can be **NULL** if the operation is not associated with a window.</span></span>

</dd> <dt>

<span data-ttu-id="c4469-115">*lpOperation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4469-115">*lpOperation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4469-116">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c4469-116">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c4469-117">Pointeur vers une chaîne se terminant par un caractère **null**, référencé dans ce cas en tant que *verbe*, qui spécifie l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c4469-117">A pointer to a **null**-terminated string, referred to in this case as a *verb*, that specifies the action to be performed.</span></span> <span data-ttu-id="c4469-118">L’ensemble des verbes disponibles dépend du fichier ou du dossier particulier.</span><span class="sxs-lookup"><span data-stu-id="c4469-118">The set of available verbs depends on the particular file or folder.</span></span> <span data-ttu-id="c4469-119">En règle générale, les actions disponibles dans le menu contextuel d’un objet sont des verbes disponibles.</span><span class="sxs-lookup"><span data-stu-id="c4469-119">Generally, the actions available from an object's shortcut menu are available verbs.</span></span> <span data-ttu-id="c4469-120">Pour plus d’informations sur les verbes et leur disponibilité, consultez la section *verbes d’objet* du [lancement d’applications](launch.md).</span><span class="sxs-lookup"><span data-stu-id="c4469-120">For more information about verbs and their availability, see the *Object Verbs* section of [Launching Applications](launch.md).</span></span> <span data-ttu-id="c4469-121">Pour plus d’informations sur les menus contextuels, consultez [extension des menus contextuels](context.md) .</span><span class="sxs-lookup"><span data-stu-id="c4469-121">See [Extending Shortcut Menus](context.md) for further discussion of shortcut menus.</span></span> <span data-ttu-id="c4469-122">Les verbes suivants sont couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="c4469-122">The following verbs are commonly used.</span></span>

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span data-ttu-id="c4469-123"><span id="edit"></span><span id="EDIT"></span>**modifiés**</span><span class="sxs-lookup"><span data-stu-id="c4469-123"><span id="edit"></span><span id="EDIT"></span>**edit**</span></span>


</dt> <dd>

<span data-ttu-id="c4469-124">Lance un éditeur et ouvre le document en vue de sa modification.</span><span class="sxs-lookup"><span data-stu-id="c4469-124">Launches an editor and opens the document for editing.</span></span> <span data-ttu-id="c4469-125">Si *lpFile* n’est pas un fichier de document, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="c4469-125">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span data-ttu-id="c4469-126"><span id="explore"></span><span id="EXPLORE"></span>**Explorer**</span><span class="sxs-lookup"><span data-stu-id="c4469-126"><span id="explore"></span><span id="EXPLORE"></span>**explore**</span></span>


</dt> <dd>

<span data-ttu-id="c4469-127">Explore le dossier spécifié par *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="c4469-127">Explores the folder specified by *lpFile*.</span></span>

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span data-ttu-id="c4469-128"><span id="find"></span><span id="FIND"></span>**trouver**</span><span class="sxs-lookup"><span data-stu-id="c4469-128"><span id="find"></span><span id="FIND"></span>**find**</span></span>


</dt> <dd>

<span data-ttu-id="c4469-129">Lance une recherche à partir du répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="c4469-129">Initiates a search starting from the specified directory.</span></span>

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span data-ttu-id="c4469-130"><span id="open"></span><span id="OPEN"></span>**afficher**</span><span class="sxs-lookup"><span data-stu-id="c4469-130"><span id="open"></span><span id="OPEN"></span>**open**</span></span>


</dt> <dd>

<span data-ttu-id="c4469-131">Ouvre le fichier spécifié par le paramètre *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="c4469-131">Opens the file specified by the *lpFile* parameter.</span></span> <span data-ttu-id="c4469-132">Il peut s’agir d’un fichier exécutable, d’un fichier de document ou d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="c4469-132">The file can be an executable file, a document file, or a folder.</span></span>

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="c4469-133"><span id="print"></span><span id="PRINT"></span>**étendue**</span><span class="sxs-lookup"><span data-stu-id="c4469-133"><span id="print"></span><span id="PRINT"></span>**print**</span></span>


</dt> <dd>

<span data-ttu-id="c4469-134">Imprime le fichier de document spécifié par *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="c4469-134">Prints the document file specified by *lpFile*.</span></span> <span data-ttu-id="c4469-135">Si *lpFile* n’est pas un fichier de document, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="c4469-135">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span data-ttu-id="c4469-136"><span id="NULL"></span><span id="null"></span>**NUL**</span><span class="sxs-lookup"><span data-stu-id="c4469-136"><span id="NULL"></span><span id="null"></span>**NULL**</span></span>


</dt> <dd>

<span data-ttu-id="c4469-137">Pour les systèmes antérieurs à Windows 2000, le verbe par défaut est utilisé s’il est valide et disponible dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c4469-137">For systems prior to Windows 2000, the default verb is used if it is valid and available in the registry.</span></span> <span data-ttu-id="c4469-138">Si ce n’est pas le cas, le verbe « Open » est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c4469-138">If not, the "open" verb is used.</span></span>

<span data-ttu-id="c4469-139">Pour les systèmes Windows 2000 et versions ultérieures, le verbe par défaut est utilisé s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="c4469-139">For Windows 2000 and later systems, the default verb is used if available.</span></span> <span data-ttu-id="c4469-140">Si ce n’est pas le cas, le verbe « Open » est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c4469-140">If not, the "open" verb is used.</span></span> <span data-ttu-id="c4469-141">Si aucun verbe n’est disponible, le système utilise le premier verbe listé dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c4469-141">If neither verb is available, the system uses the first verb listed in the registry.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c4469-142">*lpFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4469-142">*lpFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4469-143">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c4469-143">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c4469-144">Pointeur vers une chaîne se terminant par un caractère **null** qui spécifie le fichier ou l’objet sur lequel exécuter le verbe spécifié.</span><span class="sxs-lookup"><span data-stu-id="c4469-144">A pointer to a **null**-terminated string that specifies the file or object on which to execute the specified verb.</span></span> <span data-ttu-id="c4469-145">Pour spécifier un objet d’espace de noms Shell, transmettez le nom complet de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="c4469-145">To specify a Shell namespace object, pass the fully qualified parse name.</span></span> <span data-ttu-id="c4469-146">Notez que tous les verbes ne sont pas pris en charge sur tous les objets.</span><span class="sxs-lookup"><span data-stu-id="c4469-146">Note that not all verbs are supported on all objects.</span></span> <span data-ttu-id="c4469-147">Par exemple, tous les types de documents ne prennent pas en charge le verbe « Print ».</span><span class="sxs-lookup"><span data-stu-id="c4469-147">For example, not all document types support the "print" verb.</span></span>

</dd> <dt>

<span data-ttu-id="c4469-148">*lpParameters* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4469-148">*lpParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4469-149">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c4469-149">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c4469-150">Si le paramètre *lpFile* spécifie un fichier exécutable, *lpParameters* est un pointeur vers une chaîne se terminant par un caractère **null** qui spécifie les paramètres à passer à l’application.</span><span class="sxs-lookup"><span data-stu-id="c4469-150">If the *lpFile* parameter specifies an executable file, *lpParameters* is a pointer to a **null**-terminated string that specifies the parameters to be passed to the application.</span></span> <span data-ttu-id="c4469-151">Le format de cette chaîne est déterminé par le verbe qui doit être appelé.</span><span class="sxs-lookup"><span data-stu-id="c4469-151">The format of this string is determined by the verb that is to be invoked.</span></span> <span data-ttu-id="c4469-152">Si *lpFile* spécifie un fichier de document, *lpParameters* doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c4469-152">If *lpFile* specifies a document file, *lpParameters* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4469-153">*lpDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4469-153">*lpDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4469-154">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c4469-154">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c4469-155">Pointeur vers une chaîne se terminant par un caractère **null** qui spécifie le répertoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="c4469-155">A pointer to a **null**-terminated string that specifies the default directory.</span></span>

</dd> <dt>

<span data-ttu-id="c4469-156">*nShowCmd* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4469-156">*nShowCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4469-157">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="c4469-157">Type: **INT**</span></span>

<span data-ttu-id="c4469-158">Indicateurs qui spécifient comment une application doit être affichée lorsqu’elle est ouverte.</span><span class="sxs-lookup"><span data-stu-id="c4469-158">The flags that specify how an application is to be displayed when it is opened.</span></span> <span data-ttu-id="c4469-159">Si *lpFile* spécifie un fichier de document, l’indicateur est simplement passé à l’application associée.</span><span class="sxs-lookup"><span data-stu-id="c4469-159">If *lpFile* specifies a document file, the flag is simply passed to the associated application.</span></span> <span data-ttu-id="c4469-160">C’est à l’application de décider comment la gérer.</span><span class="sxs-lookup"><span data-stu-id="c4469-160">It is up to the application to decide how to handle it.</span></span> <span data-ttu-id="c4469-161">Il peut s’agir de l’une des valeurs qui peuvent être spécifiées dans le paramètre *nCmdShow* pour la fonction [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="c4469-161">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="c4469-162">*lpfnCBWinExec*</span><span class="sxs-lookup"><span data-stu-id="c4469-162">*lpfnCBWinExec*</span></span> 
</dt> <dd>

<span data-ttu-id="c4469-163">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="c4469-163">Type: **void\***</span></span>

<span data-ttu-id="c4469-164">Fonction de rappel utilisée pour appeler [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) dans le noyau 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4469-164">Callback function used to call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in the 16-bit kernel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4469-165">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4469-165">Return value</span></span>

<span data-ttu-id="c4469-166">Type : **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="c4469-166">Type: **HINSTANCE**</span></span>

<span data-ttu-id="c4469-167">Retourne une valeur supérieure à 32 en cas de réussite, ou une valeur d’erreur inférieure ou égale à 32 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c4469-167">Returns a value greater than 32 if successful, or an error value that is less than or equal to 32 otherwise.</span></span> <span data-ttu-id="c4469-168">Le tableau suivant répertorie les valeurs d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c4469-168">The following table lists the error values.</span></span> <span data-ttu-id="c4469-169">La valeur de retour est castée en tant que HINSTANCE pour la compatibilité descendante avec les applications Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c4469-169">The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications.</span></span> <span data-ttu-id="c4469-170">Toutefois, ce n’est pas un véritable HINSTANCE.</span><span class="sxs-lookup"><span data-stu-id="c4469-170">It is not a true HINSTANCE, however.</span></span> <span data-ttu-id="c4469-171">La seule chose qui peut être effectuée avec le HINSTANCE retourné est de le convertir en **int** et de le comparer à la valeur 32 ou à l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c4469-171">The only thing that can be done with the returned HINSTANCE is to cast it to an **int** and compare it with the value 32 or one of the error codes below.</span></span>



| <span data-ttu-id="c4469-172">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c4469-172">Return code</span></span>                                                                                             | <span data-ttu-id="c4469-173">Description</span><span class="sxs-lookup"><span data-stu-id="c4469-173">Description</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4469-174"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-174"><dt>**0**</dt></span></span> </dl>                        | <span data-ttu-id="c4469-175">Le système d’exploitation ne dispose pas de suffisamment de mémoire ou de ressources.</span><span class="sxs-lookup"><span data-stu-id="c4469-175">The operating system is out of memory or resources.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="c4469-176"><dt>**\_fichier d' \_ erreur \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-176"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="c4469-177">Le fichier spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c4469-177">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="c4469-178"><dt>**\_chemin d' \_ erreur \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-178"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="c4469-179">Le chemin spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c4469-179">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="c4469-180"><dt>**\_format incorrect de l’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-180"><dt>**ERROR\_BAD\_FORMAT**</dt></span></span> </dl>       | <span data-ttu-id="c4469-181">Le fichier. exe n’est pas valide (non Win32. exe ou erreur dans l’image. exe).</span><span class="sxs-lookup"><span data-stu-id="c4469-181">The .exe file is invalid (non-Win32 .exe or error in .exe image).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="c4469-182"><dt>**SE \_ ACCESSDENIED d’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-182"><dt>**SE\_ERR\_ACCESSDENIED**</dt></span></span> </dl>    | <span data-ttu-id="c4469-183">Le système d’exploitation a refusé l’accès au fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c4469-183">The operating system denied access to the specified file.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="c4469-184"><dt>**SE \_ ASSOCINCOMPLETE d’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-184"><dt>**SE\_ERR\_ASSOCINCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="c4469-185">L’Association du nom de fichier est incomplète ou non valide.</span><span class="sxs-lookup"><span data-stu-id="c4469-185">The file name association is incomplete or invalid.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="c4469-186"><dt>**SE \_ DDEBUSY d’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-186"><dt>**SE\_ERR\_DDEBUSY**</dt></span></span> </dl>         | <span data-ttu-id="c4469-187">La transaction DDE n’a pas pu être effectuée, car d’autres transactions DDE étaient en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="c4469-187">The DDE transaction could not be completed because other DDE transactions were being processed.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="c4469-188"><dt>**SE \_ DDEFAIL d’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-188"><dt>**SE\_ERR\_DDEFAIL**</dt></span></span> </dl>         | <span data-ttu-id="c4469-189">Échec de la transaction DDE.</span><span class="sxs-lookup"><span data-stu-id="c4469-189">The DDE transaction failed.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="c4469-190"><dt>**SE \_ DDETIMEOUT d’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-190"><dt>**SE\_ERR\_DDETIMEOUT**</dt></span></span> </dl>      | <span data-ttu-id="c4469-191">La transaction DDE n’a pas pu aboutir car la demande a expiré.</span><span class="sxs-lookup"><span data-stu-id="c4469-191">The DDE transaction could not be completed because the request timed out.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="c4469-192"><dt>**SE \_ DLLNOTFOUND d’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-192"><dt>**SE\_ERR\_DLLNOTFOUND**</dt></span></span> </dl>     | <span data-ttu-id="c4469-193">La DLL spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c4469-193">The specified DLL was not found.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="c4469-194"><dt>**erreur SE- \_ \_ FNF**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-194"><dt>**SE\_ERR\_FNF**</dt></span></span> </dl>             | <span data-ttu-id="c4469-195">Le fichier spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c4469-195">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="c4469-196"><dt>**SE \_ Err \_ noassoc**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-196"><dt>**SE\_ERR\_NOASSOC**</dt></span></span> </dl>         | <span data-ttu-id="c4469-197">Aucune application n’est associée à l’extension de nom de fichier donnée.</span><span class="sxs-lookup"><span data-stu-id="c4469-197">There is no application associated with the given file name extension.</span></span> <span data-ttu-id="c4469-198">Cette erreur est également retournée si vous tentez d’imprimer un fichier qui n’est pas imprimable.</span><span class="sxs-lookup"><span data-stu-id="c4469-198">This error will also be returned if you attempt to print a file that is not printable.</span></span><br/> |
| <dl> <span data-ttu-id="c4469-199"><dt>**SE \_ insuffisance d’erreur \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-199"><dt>**SE\_ERR\_OOM**</dt></span></span> </dl>             | <span data-ttu-id="c4469-200">La mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="c4469-200">There was not enough memory to complete the operation.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="c4469-201"><dt>**SE \_ Err. \_ PNF**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-201"><dt>**SE\_ERR\_PNF**</dt></span></span> </dl>             | <span data-ttu-id="c4469-202">Le chemin spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c4469-202">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="c4469-203"><dt>**\_partage d’Err. se \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-203"><dt>**SE\_ERR\_SHARE**</dt></span></span> </dl>           | <span data-ttu-id="c4469-204">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c4469-204">A sharing violation occurred.</span></span><br/>                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c4469-205">Notes</span><span class="sxs-lookup"><span data-stu-id="c4469-205">Remarks</span></span>

<span data-ttu-id="c4469-206">**WOWShellExecute** n’est pas inclus dans un en-tête ou un fichier. lib.</span><span class="sxs-lookup"><span data-stu-id="c4469-206">**WOWShellExecute** is not included in a header or .lib file.</span></span> <span data-ttu-id="c4469-207">Elle est exportée à partir de Shell32.dll par son nom.</span><span class="sxs-lookup"><span data-stu-id="c4469-207">It is exported from Shell32.dll by name.</span></span>

<span data-ttu-id="c4469-208">Cette méthode vous permet d’exécuter des commandes dans le menu contextuel d’un dossier ou stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c4469-208">This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.</span></span>

<span data-ttu-id="c4469-209">Si *lpOperation* a la **valeur null**, la fonction ouvre le fichier spécifié par *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="c4469-209">If *lpOperation* is **NULL**, the function opens the file specified by *lpFile*.</span></span> <span data-ttu-id="c4469-210">Si *lpOperation* est « Open » ou « explore », la fonction tente d’ouvrir ou d’explorer le dossier.</span><span class="sxs-lookup"><span data-stu-id="c4469-210">If *lpOperation* is "open" or "explore", the function attempts to open or explore the folder.</span></span>

<span data-ttu-id="c4469-211">Pour obtenir des informations sur l’application qui est lancée suite à l’appel de **WOWShellExecute**, utilisez [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="c4469-211">To obtain information about the application that is launched as a result of calling **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

> [!Note]  
> <span data-ttu-id="c4469-212">Le paramètre **Démarrer le dossier Windows dans un processus distinct** dans les options des dossiers affecte **WOWShellExecute**.</span><span class="sxs-lookup"><span data-stu-id="c4469-212">The **Launch folder windows in a separate process** setting in Folder Options affects **WOWShellExecute**.</span></span> <span data-ttu-id="c4469-213">Si cette option est désactivée (paramètre par défaut), **WOWShellExecute** utilise une fenêtre d’Explorateur ouverte au lieu d’en lancer une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="c4469-213">If that option is disabled (the default setting), **WOWShellExecute** uses an open Explorer window rather than launch a new one.</span></span> <span data-ttu-id="c4469-214">Si aucune fenêtre d’explorateur n’est ouverte, **WOWShellExecute** en lance une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="c4469-214">If no Explorer window is open, **WOWShellExecute** launches a new one.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4469-215">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4469-215">Requirements</span></span>



| <span data-ttu-id="c4469-216">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4469-216">Requirement</span></span> | <span data-ttu-id="c4469-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4469-217">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4469-218">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4469-218">Minimum supported client</span></span><br/> | <span data-ttu-id="c4469-219">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4469-219">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c4469-220">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4469-220">Minimum supported server</span></span><br/> | <span data-ttu-id="c4469-221">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4469-221">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4469-222">DLL</span><span class="sxs-lookup"><span data-stu-id="c4469-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4469-223"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4469-223"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4469-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4469-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4469-225">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="c4469-225">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 

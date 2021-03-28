---
description: Affiche une fenêtre d’aide qui correspond au paramètre de langue de l’interface utilisateur actuel.
title: MLHtmlHelp fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991124"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="c2749-103">MLHtmlHelp fonction)</span><span class="sxs-lookup"><span data-stu-id="c2749-103">MLHtmlHelp function</span></span>

<span data-ttu-id="c2749-104">\[Cette fonction est disponible via Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c2749-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c2749-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2749-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c2749-106">Affiche une fenêtre d’aide qui correspond au paramètre de langue de l’interface utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c2749-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2749-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2749-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="c2749-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2749-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2749-109">*hwndCaller* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2749-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2749-110">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="c2749-110">Type: **HWND**</span></span>

<span data-ttu-id="c2749-111">Handle de la fenêtre parente qui appelle cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c2749-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="c2749-112">*pszFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2749-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2749-113">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c2749-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c2749-114">Pointeur vers une mémoire tampon qui contient le chemin d’accès complet d’un fichier d’aide compilé (. chm) ou un fichier de rubrique dans un fichier d’aide spécifié.</span><span class="sxs-lookup"><span data-stu-id="c2749-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="c2749-115">*uCommand* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2749-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2749-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="c2749-116">Type: **UINT**</span></span>

<span data-ttu-id="c2749-117">Commande à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c2749-117">The command to complete.</span></span> <span data-ttu-id="c2749-118">Cette fonction prend directement en charge uniquement la [ \_ \_ rubrique d’affichage HH](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) et le [ \_ \_ texte affiché \_ hh](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span><span class="sxs-lookup"><span data-stu-id="c2749-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="c2749-119">Dans le cas d’une autre commande, l’appel est transféré sans la valeur *dwCrossCodePage* à [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span><span class="sxs-lookup"><span data-stu-id="c2749-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="c2749-120">*dwData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2749-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2749-121">Type : **\_ ptr DWORD**</span><span class="sxs-lookup"><span data-stu-id="c2749-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="c2749-122">Toutes les données qui peuvent être requises, en fonction de la valeur du paramètre *uCommand* .</span><span class="sxs-lookup"><span data-stu-id="c2749-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c2749-123">*dwCrossCodePage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2749-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2749-124">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c2749-124">Type: **DWORD**</span></span>

<span data-ttu-id="c2749-125">Valeur **DWORD** indiquant la page de codes du paramètre de langue actuelle de l’interface utilisateur, par exemple CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="c2749-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2749-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2749-126">Return value</span></span>

<span data-ttu-id="c2749-127">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="c2749-127">Type: **HWND**</span></span>

<span data-ttu-id="c2749-128">Selon le *uCommand* spécifié et le résultat, **MLHtmlHelp** retourne l’un des éléments suivants, ou les deux :</span><span class="sxs-lookup"><span data-stu-id="c2749-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="c2749-129">Handle (HWND) de la fenêtre d’aide.</span><span class="sxs-lookup"><span data-stu-id="c2749-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="c2749-130">**Valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c2749-130">**NULL**.</span></span> <span data-ttu-id="c2749-131">Dans certains cas, **null** indique un échec ; dans d’autres cas, la **valeur null** indique que la fenêtre d’aide n’a pas encore été créée.</span><span class="sxs-lookup"><span data-stu-id="c2749-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2749-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c2749-132">Remarks</span></span>

<span data-ttu-id="c2749-133">Si un problème se produit avec le chemin d’accès du fichier d’aide pour la langue actuelle, l’appel est transféré à [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) pour la gestion standard.</span><span class="sxs-lookup"><span data-stu-id="c2749-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="c2749-134">Lorsque la fenêtre d’aide est fermée, le focus revient au propriétaire, sauf si le propriétaire est le bureau.</span><span class="sxs-lookup"><span data-stu-id="c2749-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="c2749-135">Si *hwndCaller* est le bureau, le système d’exploitation détermine où le focus est retourné.</span><span class="sxs-lookup"><span data-stu-id="c2749-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="c2749-136">En outre, si **MLHtmlHelp** envoie des messages de notification à partir de la fenêtre d’aide, les messages sont envoyés à *hwndCaller* tant que vous avez activé le suivi des [messages de notification](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) dans la définition de la fenêtre d’aide.</span><span class="sxs-lookup"><span data-stu-id="c2749-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="c2749-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="c2749-137">Examples</span></span>

<span data-ttu-id="c2749-138">L’exemple suivant appelle la commande [hh \_ Display \_ topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) pour ouvrir le fichier d’aide nommé Help. chm et afficher sa rubrique par défaut dans la fenêtre d’aide nommée `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="c2749-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="c2749-139">En règle générale, la fenêtre d’aide spécifiée dans cette commande est une [visionneuse d’aide HTML](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)standard.</span><span class="sxs-lookup"><span data-stu-id="c2749-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="c2749-140">Quand vous utilisez cette fonction, définissez la taille de la pile de l’exécutable d’hébergement sur au moins 100 000.</span><span class="sxs-lookup"><span data-stu-id="c2749-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="c2749-141">Si la taille de la pile définie est trop petite, le thread créé pour exécuter l’aide HTML est également créé avec cette taille de pile, et l’opération peut échouer.</span><span class="sxs-lookup"><span data-stu-id="c2749-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="c2749-142">Si vous le souhaitez, vous pouvez supprimer/STACK de la ligne de commande de liaison et supprimer tous les paramètres de pile dans le fichier DEF de l’exécutable (la taille de la pile par défaut est de 1 Mo dans le cas présent).</span><span class="sxs-lookup"><span data-stu-id="c2749-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="c2749-143">Vous pouvez également définir la taille de la pile à l’aide de la commande du compilateur/fnumber (le compilateur passera ce à l’éditeur de liens en tant que/STACK).</span><span class="sxs-lookup"><span data-stu-id="c2749-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2749-144">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c2749-144">Requirements</span></span>



| <span data-ttu-id="c2749-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2749-145">Requirement</span></span> | <span data-ttu-id="c2749-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2749-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2749-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2749-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c2749-148">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2749-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2749-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2749-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c2749-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2749-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c2749-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2749-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2749-152"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="c2749-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="c2749-153">DLL</span><span class="sxs-lookup"><span data-stu-id="c2749-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2749-154"><dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c2749-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="c2749-155">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c2749-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c2749-156">**MLHtmlHelpW** (Unicode) et **MLHtmlHelpA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c2749-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 

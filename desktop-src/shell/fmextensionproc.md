---
description: Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers pour communiquer avec une extension du gestionnaire de fichiers.
title: Fonction de rappel FMExtensionProc (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842240"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="38ca1-103">FMExtensionProc fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="38ca1-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="38ca1-104">Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers pour communiquer avec une extension du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="38ca1-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ca1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38ca1-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="38ca1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38ca1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ca1-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="38ca1-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="38ca1-108">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="38ca1-108">Type: **HWND**</span></span>

<span data-ttu-id="38ca1-109">Handle de fenêtre vers le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="38ca1-109">A window handle to File Manager.</span></span> <span data-ttu-id="38ca1-110">Une extension utilise ce handle pour spécifier la fenêtre parente pour une boîte de dialogue ou une boîte de message qu’elle doit afficher, et pour envoyer des messages de requête au gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="38ca1-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="38ca1-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="38ca1-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="38ca1-112">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="38ca1-112">Type: **WORD**</span></span>

<span data-ttu-id="38ca1-113">Un des messages du gestionnaire de fichiers suivants.</span><span class="sxs-lookup"><span data-stu-id="38ca1-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="38ca1-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 à 99**</span><span class="sxs-lookup"><span data-stu-id="38ca1-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-115">L’utilisateur a sélectionné un élément dans le menu fourni par l’extension.</span><span class="sxs-lookup"><span data-stu-id="38ca1-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="38ca1-116">La valeur est l’identificateur de l’élément de menu sélectionné.</span><span class="sxs-lookup"><span data-stu-id="38ca1-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="38ca1-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="38ca1-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-118">L’utilisateur a appuyé sur F1 tout en sélectionnant un menu d’extension ou un élément de commande de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="38ca1-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="38ca1-119">Indique que l’extension doit appeler **WinHelp** de manière appropriée pour l’élément de commande.</span><span class="sxs-lookup"><span data-stu-id="38ca1-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="38ca1-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**\_HELPSTRING FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="38ca1-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-121">L’utilisateur a sélectionné un menu d’extension ou un élément de commande de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="38ca1-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="38ca1-122">Indique que l’extension doit fournir une chaîne d’aide.</span><span class="sxs-lookup"><span data-stu-id="38ca1-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="38ca1-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="38ca1-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-124">L’utilisateur a sélectionné le menu de l’extension.</span><span class="sxs-lookup"><span data-stu-id="38ca1-124">User selected the extension's menu.</span></span> <span data-ttu-id="38ca1-125">L’extension doit initialiser des éléments dans le menu.</span><span class="sxs-lookup"><span data-stu-id="38ca1-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="38ca1-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**\_charge FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="38ca1-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-127">Le gestionnaire de fichiers charge la DLL d’extension et invite la DLL à fournir des informations sur le menu fourni par la DLL.</span><span class="sxs-lookup"><span data-stu-id="38ca1-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="38ca1-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ selChange**</span><span class="sxs-lookup"><span data-stu-id="38ca1-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-129">La sélection dans la fenêtre répertoire du **Gestionnaire de fichiers** ou dans la fenêtre des résultats de la **recherche** a changé.</span><span class="sxs-lookup"><span data-stu-id="38ca1-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="38ca1-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="38ca1-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-131">Le gestionnaire de fichiers crée la barre d’outils et demande à la DLL d’extension des informations sur les boutons que la DLL ajoute à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="38ca1-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="38ca1-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**\_déchargement FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="38ca1-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-133">Le gestionnaire de fichiers décharge la DLL d’extension.</span><span class="sxs-lookup"><span data-stu-id="38ca1-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="38ca1-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT l’actualisation de l' \_ utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="38ca1-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="38ca1-135">L’utilisateur a sélectionné la commande **Actualiser** dans le menu **fenêtre** .</span><span class="sxs-lookup"><span data-stu-id="38ca1-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="38ca1-136">L’extension doit mettre à jour les éléments dans le menu, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="38ca1-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="38ca1-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38ca1-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ca1-138">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="38ca1-138">Type: **LONG**</span></span>

<span data-ttu-id="38ca1-139">Valeur spécifique au message.</span><span class="sxs-lookup"><span data-stu-id="38ca1-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ca1-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38ca1-140">Return value</span></span>

<span data-ttu-id="38ca1-141">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="38ca1-141">Type: **LONG**</span></span>

<span data-ttu-id="38ca1-142">Retourne une valeur en fonction du message de paramètre *wMsg* .</span><span class="sxs-lookup"><span data-stu-id="38ca1-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ca1-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="38ca1-143">Requirements</span></span>



| <span data-ttu-id="38ca1-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38ca1-144">Requirement</span></span> | <span data-ttu-id="38ca1-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="38ca1-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38ca1-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38ca1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="38ca1-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38ca1-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="38ca1-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38ca1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="38ca1-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38ca1-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="38ca1-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="38ca1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="38ca1-151"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="38ca1-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="38ca1-152">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="38ca1-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="38ca1-153">**FMExtensionProcW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="38ca1-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 





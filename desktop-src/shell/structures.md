---
description: Cette section décrit les structures de l’interpréteur de commandes Windows.
title: Structures de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bbda4cd81c3db2dff664b9d16d2db60aa8f12f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973774"
---
# <a name="shell-structures"></a><span data-ttu-id="d2605-103">Structures de Shell</span><span class="sxs-lookup"><span data-stu-id="d2605-103">Shell Structures</span></span>

<span data-ttu-id="d2605-104">Cette section décrit les structures de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="d2605-104">This section describes the Windows Shell Structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d2605-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d2605-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2605-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d2605-106">Topic</span></span></th>
<th><span data-ttu-id="d2605-107">Description</span><span class="sxs-lookup"><span data-stu-id="d2605-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2605-108"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-108"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-109">Structure de taille variable qui contient des informations sur un nom de fichier de menu.</span><span class="sxs-lookup"><span data-stu-id="d2605-109">A variable-size structure that contains information about a menu file name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-110"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-110"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-111">Contient des informations sur un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="d2605-111">Contains information about a menu item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-112"><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-112"><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-113">Contient des informations sur un message appbar système.</span><span class="sxs-lookup"><span data-stu-id="d2605-113">Contains information about a system appbar message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-114"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-114"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-115">Fournit des informations sur la catégorie application pour ajouter/supprimer des programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d2605-115">Provides application category information to Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="d2605-116">La structure <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a> est utilisée pour créer une liste complète des catégories pour un éditeur d’application.</span><span class="sxs-lookup"><span data-stu-id="d2605-116">The <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a> structure is used create a complete list of categories for an application publisher.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-117"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-117"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-118">Fournit la liste des catégories d’applications prises en charge à partir d’un éditeur d’application pour ajouter/supprimer des programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d2605-118">Provides a list of supported application categories from an application publisher to Add/Remove Programs in Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-119"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-119"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-120">Fournit des informations sur une application publiée à l’utilitaire ajout/suppression de programmes du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d2605-120">Provides information about a published application to the Add/Remove Programs Control Panel utility.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-121"><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-121"><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-122">Définit les informations utilisées par <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> pour récupérer une interface <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> pour une association de fichier donnée.</span><span class="sxs-lookup"><span data-stu-id="d2605-122">Defines information used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> to retrieve an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> interface for a given file association.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-123"><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-123"><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-124">Contient des informations sur une bande de dossiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-124">Contains information about a folder band.</span></span> <span data-ttu-id="d2605-125">Cette structure est utilisée avec les méthodes <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand :: GetBandInfoSFB</strong></a> et <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand :: SetBandInfoSFB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-125">This structure is used with the <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand::GetBandInfoSFB</strong></a> and <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand::SetBandInfoSFB</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-126"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-126"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-127">Contient des informations sur un site de bande.</span><span class="sxs-lookup"><span data-stu-id="d2605-127">Contains information about a band site.</span></span> <span data-ttu-id="d2605-128">Cette structure est utilisée avec les méthodes <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite :: GetBandSiteInfo</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite :: SetBandSiteInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-128">This structure is used with the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite::GetBandSiteInfo</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite::SetBandSiteInfo</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-129"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-129"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-130">Contient des membres protégés de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="d2605-130">Contains protected members of the base class.</span></span> <span data-ttu-id="d2605-131"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> définit l’état du navigateur et est utilisé avec <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2 :: GetBaseBrowserData</strong></a> et <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2 ::P utbasebrowserdata</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-131"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> defines the browser state and is used with <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2::GetBaseBrowserData</strong></a> and <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2::PutBaseBrowserData</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-132"><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-132"><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-133">Définit les coordonnées des angles supérieur gauche et inférieur droit d’un rectangle de bordure.</span><span class="sxs-lookup"><span data-stu-id="d2605-133">Defines the coordinates of the upper-left and lower-right corners of a border rectangle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-134"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-134"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-135">Contient des paramètres pour la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a> et reçoit des informations sur le dossier sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2605-135">Contains parameters for the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a> function and receives information about the folder selected by the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-136"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-136"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-137">Contient des informations de catégorie.</span><span class="sxs-lookup"><span data-stu-id="d2605-137">Contains category information.</span></span> <span data-ttu-id="d2605-138">Une catégorie de composant est un groupe de classes COM (Component Object Model) liées de manière logique qui partagent un identificateur de catégorie (CATID) commun.</span><span class="sxs-lookup"><span data-stu-id="d2605-138">A component category is a group of logically-related Component Object Model (COM) classes that share a common category identifier (CATID).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-139"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>DESTINÉS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-139"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>CIDA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-140">Utilisé avec le format de presse-papiers <a href="clipboard.md">CFSTR_SHELLIDLIST</a> pour transférer le pointeur vers une liste d’identificateurs d’élément (PIDL) d’un ou plusieurs objets d’espace de noms de Shell.</span><span class="sxs-lookup"><span data-stu-id="d2605-140">Used with the <a href="clipboard.md">CFSTR_SHELLIDLIST</a> clipboard format to transfer the pointer to an item identifier list (PIDL) of one or more Shell namespace objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-141"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-141"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-142">Définit les informations de colonne.</span><span class="sxs-lookup"><span data-stu-id="d2605-142">Defines column information.</span></span> <span data-ttu-id="d2605-143">Utilisé par les membres de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-143">Used by members of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-144"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-144"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-145">Contient les informations nécessaires à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu :: commande InvokeCommand</strong></a> pour appeler une commande de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="d2605-145">Contains information needed by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> to invoke a shortcut menu command.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-146"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-146"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-147">Contient des informations étendues sur une commande de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="d2605-147">Contains extended information about a shortcut menu command.</span></span> <span data-ttu-id="d2605-148">Cette structure est une version étendue de <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> qui permet d’utiliser des valeurs Unicode.</span><span class="sxs-lookup"><span data-stu-id="d2605-148">This structure is an extended version of <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> that allows the use of Unicode values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-149"><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-149"><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-150">Utilisé de manière générique pour filtrer les éléments.</span><span class="sxs-lookup"><span data-stu-id="d2605-150">Used generically to filter elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-151"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>-</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-151"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>COMPONENT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-152">Utilisé par Windows 2000 pour conserver les informations relatives à un composant.</span><span class="sxs-lookup"><span data-stu-id="d2605-152">Used by Windows 2000 to hold information about a component.</span></span> <span data-ttu-id="d2605-153">Cette structure remplace la structure <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-153">This structure replaces the <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-154"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-154"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-155">Contient les options d’élément de bureau.</span><span class="sxs-lookup"><span data-stu-id="d2605-155">Contains the desktop item options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-156"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-156"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-157">Contient des informations sur la position et la taille d’un composant.</span><span class="sxs-lookup"><span data-stu-id="d2605-157">Holds information about a component's position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-158"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-158"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-159">Utilisé par Windows 2000 pour conserver les informations sur l’état d’un composant.</span><span class="sxs-lookup"><span data-stu-id="d2605-159">Used by Windows 2000 to hold information about a component's state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-160"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-160"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-161">Définit la structure de l’élément en conflit.</span><span class="sxs-lookup"><span data-stu-id="d2605-161">Defines conflict item structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-162"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-162"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-163">Définit la structure des informations sur les résultats des conflits.</span><span class="sxs-lookup"><span data-stu-id="d2605-163">Defines conflict result information structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-164"><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-164"><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-165">Contient des informations sur les ressources et une valeur définie par l’application pour une boîte de dialogue prise en charge par une application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d2605-165">Contains resource information and an application-defined value for a dialog box supported by a Control Panel application.</span></span> <span data-ttu-id="d2605-166">La fonction <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> de l’application du panneau de configuration retourne ces informations dans le panneau de configuration en réponse à un message de <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-166">The <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> function of the Control Panel application returns this information to the Control Panel in response to a <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-167"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-167"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-168">Contient des détails sur les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="d2605-168">Contains details about a credential.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-169"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-169"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-170">Décrit un champ unique dans les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="d2605-170">Describes a single field in a credential.</span></span> <span data-ttu-id="d2605-171">Par exemple, une chaîne ou une image utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2605-171">For example, a string or a user image.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-172"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-172"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-173">Utilisé avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-173">Used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-174"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-174"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-175">Sert d’en-tête pour certaines structures de données supplémentaires utilisées par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-175">Serves as the header for some of the extra data structures used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-176"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-176"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-177">Contient les informations de menu contextuel utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-177">Contains context menu information used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-178"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-178"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-179">Utilisé par les dossiers délégués à la place d’une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> standard.</span><span class="sxs-lookup"><span data-stu-id="d2605-179">Used by delegate folders in place of a standard <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-180"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-180"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-181">Contient des informations détaillées sur un élément de dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="d2605-181">Contains detail information for a Shell folder item.</span></span> <span data-ttu-id="d2605-182">Utilisé avec la notification de <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-182">Used with the <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-183"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-183"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-184">Contient des arguments supplémentaires utilisés par <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-184">Contains additional arguments used by <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-185"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-185"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-186">Reçoit des informations de version spécifiques à la DLL.</span><span class="sxs-lookup"><span data-stu-id="d2605-186">Receives DLL-specific version information.</span></span> <span data-ttu-id="d2605-187">Elle est utilisée avec la fonction <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-187">It is used with the <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> function.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2605-188">À la place de cette structure, vous pouvez utiliser la structure <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-188">In place of this structure, you can use the <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> structure.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-189"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-189"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-190">Reçoit des informations de version spécifiques à la DLL.</span><span class="sxs-lookup"><span data-stu-id="d2605-190">Receives DLL-specific version information.</span></span> <span data-ttu-id="d2605-191">Elle est utilisée avec la fonction <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-191">It is used with the <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-192"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-192"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-193">Décrit l’image et le texte d’accompagnement pour un objet Drop.</span><span class="sxs-lookup"><span data-stu-id="d2605-193">Describes the image and accompanying text for a drop object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-194"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-194"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-195">Définit le format du presse-papiers <a href="clipboard.md">CF_HDROP</a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-195">Defines the <a href="clipboard.md">CF_HDROP</a> clipboard format.</span></span> <span data-ttu-id="d2605-196">Les données suivantes sont une liste de noms de fichiers se terminant par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="d2605-196">The data that follows is a double null-terminated list of file names.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-197"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-197"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-198">Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-198">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d2605-199">Il contient l’ID de Windows Installer du lien.</span><span class="sxs-lookup"><span data-stu-id="d2605-199">It holds the link's Windows Installer ID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-200"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-200"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-201">Stocke les informations sur l’état du lien de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="d2605-201">Stores information about the Shell link state.</span></span> <span data-ttu-id="d2605-202">Cette structure est utilisée pour les sections de données supplémentaires qui sont marquées avec EXP_PROPERTYSTORAGE_SIG.</span><span class="sxs-lookup"><span data-stu-id="d2605-202">This structure is used for extra data sections that are tagged with EXP_PROPERTYSTORAGE_SIG.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-203"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-203"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-204">Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-204">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d2605-205">Elle contient des informations sur les dossiers spéciaux.</span><span class="sxs-lookup"><span data-stu-id="d2605-205">It holds special folder information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-206"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-206"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-207">Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-207">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d2605-208">Elle contient des chaînes d’environnement développables pour l’icône ou la cible.</span><span class="sxs-lookup"><span data-stu-id="d2605-208">It holds expandable environment strings for the icon or target.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-209"><a href="ext-button.md"><strong>EXT_BUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-209"><a href="ext-button.md"><strong>EXT_BUTTON</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-210">Contient des informations sur un bouton que la DLL d’extension du gestionnaire de fichiers ajoute à la barre d’outils du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-210">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-211"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-211"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-212">Utilisé par un objet énumérateur <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> pour retourner des informations sur les objets de recherche pris en charge par un objet de dossier de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="d2605-212">Used by an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> enumerator object to return information on the search objects supported by a Shell Folder object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-213"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-213"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-214">Contient la définition du format du presse-papiers pour CFSTR_FILE_ATTRIBUTES_ARRAY.</span><span class="sxs-lookup"><span data-stu-id="d2605-214">Contains the clipboard format definition for CFSTR_FILE_ATTRIBUTES_ARRAY.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-215"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-215"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-216">Décrit les propriétés d’un fichier copié par le biais du presse-papiers pendant une opération de <a href="dragdrop.md">glisser-déplacer</a> Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d2605-216">Describes the properties of a file that is being copied by means of the clipboard during a Microsoft ActiveX <a href="dragdrop.md">drag-and-drop</a> operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-217"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-217"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-218">Définit le format du presse-papiers CF_FILEGROUPDESCRIPTOR.</span><span class="sxs-lookup"><span data-stu-id="d2605-218">Defines the CF_FILEGROUPDESCRIPTOR clipboard format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-219"><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-219"><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-220">Contient des informations sur le lecteur sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre du répertoire ou la fenêtre des résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="d2605-220">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-221"><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-221"><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-222">Contient des informations sur un fichier sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre de répertoire ou la fenêtre des résultats de la recherche).</span><span class="sxs-lookup"><span data-stu-id="d2605-222">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-223"><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-223"><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-224">Contient des informations utilisées par le gestionnaire de fichiers pour ajouter une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d2605-224">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-225"><a href="fms-load.md"><strong>FMS_LOAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-225"><a href="fms-load.md"><strong>FMS_LOAD</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-226">Contient des informations utilisées par le gestionnaire de fichiers pour ajouter un menu personnalisé fourni par une DLL d’extension du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-226">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="d2605-227">La structure fournit également une valeur delta que la DLL d’extension peut utiliser pour manipuler le menu personnalisé après le chargement du menu par le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-227">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-228"><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-228"><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-229">Contient des informations sur les boutons personnalisés à ajouter à la barre d’outils du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-229">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="d2605-230">Les boutons sont fournis par une DLL d’extension du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-230">The buttons are provided by a File Manager extension DLL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-231"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-231"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-232">Contient des informations sur l’affichage des dossiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-232">Contains folder view information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-233"><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-233"><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-234">Contient des informations utilisées par la visionneuse de fichiers pour afficher un fichier.</span><span class="sxs-lookup"><span data-stu-id="d2605-234">Contains information that the file viewer uses to display a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-235"><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-235"><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-236">Contient des informations sur un élément pour lequel une aide contextuelle a été demandée.</span><span class="sxs-lookup"><span data-stu-id="d2605-236">Contains information about an item for which context-sensitive Help has been requested.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-237"><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-237"><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-238">Contient la taille et la position d’une fenêtre d’aide principale ou secondaire.</span><span class="sxs-lookup"><span data-stu-id="d2605-238">Contains the size and position of either a primary or secondary Help window.</span></span> <span data-ttu-id="d2605-239">Une application peut définir ces informations en appelant la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> avec la valeur HELP_SETWINPOS.</span><span class="sxs-lookup"><span data-stu-id="d2605-239">An application can set this information by calling the <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> function with the HELP_SETWINPOS value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-240"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-240"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-241">Utilisé par Microsoft Internet Explorer 4,0 et Microsoft Internet Explorer 4,01 pour stocker des informations sur un composant.</span><span class="sxs-lookup"><span data-stu-id="d2605-241">Used by Microsoft Internet Explorer 4.0 and Microsoft Internet Explorer 4.01 to hold information about a component.</span></span> <span data-ttu-id="d2605-242">Avec Windows 2000, il est remplacé par la structure du <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>composant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-242">With Windows 2000, it is replaced by the <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>COMPONENT</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-243"><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-243"><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-244">Contient une liste d’identificateurs d’élément.</span><span class="sxs-lookup"><span data-stu-id="d2605-244">Contains a list of item identifiers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-245"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-245"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-246">Stocke les dimensions des deux tailles possibles de l’espacement des icônes qui sont disponibles pour l’affichage : petite et grande.</span><span class="sxs-lookup"><span data-stu-id="d2605-246">Stores the dimensions of the two possible sizes of icon spacing that are available for display: small and large.</span></span> <span data-ttu-id="d2605-247">Utilisé par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView :: GetItemSpacing</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-247">Used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView::GetItemSpacing</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-248"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-248"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-249">Définit les caractéristiques d’un dossier connu.</span><span class="sxs-lookup"><span data-stu-id="d2605-249">Defines the specifics of a known folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-250"><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-250"><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-251">Définit les attributs d’une police.</span><span class="sxs-lookup"><span data-stu-id="d2605-251">Defines the attributes of a font.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-252"><a href="mruinfo.md"><strong>MRUINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-252"><a href="mruinfo.md"><strong>MRUINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-253">Contient des informations qui définissent une nouvelle liste des derniers fichiers utilisés (MRU).</span><span class="sxs-lookup"><span data-stu-id="d2605-253">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="d2605-254">Utilisé par <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-254">Used by <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-255"><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-255"><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-256">Spécifie un mot clé à rechercher et la table de mots clés dans laquelle l’aide Windows doit être recherchée.</span><span class="sxs-lookup"><span data-stu-id="d2605-256">Specifies a keyword to search for and the keyword table to be searched by Windows Help.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-257"><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-257"><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-258">Contient des informations qui décrivent une adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="d2605-258">Contains information that describes a network address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-259"><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-259"><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-260">Décrit une adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="d2605-260">Describes a network address.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-261"><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-261"><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-262">Contient des informations sur les ressources et une valeur définie par l’application pour une boîte de dialogue prise en charge par une application du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d2605-262">Contains resource information and an application-defined value for a dialog box supported by a Control Panel application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-263"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-263"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-264">Contient des informations dont le système a besoin pour afficher les notifications dans la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="d2605-264">Contains information that the system needs to display notifications in the notification area.</span></span> <span data-ttu-id="d2605-265">Utilisé par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-265">Used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-266"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-266"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-267">Contient des informations utilisées par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> pour identifier l’icône pour laquelle le rectangle englobant doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="d2605-267">Contains information used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> to identify the icon for which to retrieve the bounding rectangle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-268"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-268"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-269">Définit le format du presse-papiers CF_NETRESOURCE.</span><span class="sxs-lookup"><span data-stu-id="d2605-269">Defines the CF_NETRESOURCE clipboard format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-270"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-270"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-271">Structure de dessin personnalisée utilisée par les méthodes <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-271">Custom draw structure used by <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-272"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-272"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-273">Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-273">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d2605-274">Elle contient les propriétés de la console.</span><span class="sxs-lookup"><span data-stu-id="d2605-274">It holds console properties.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-275"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-275"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-276">Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-276">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d2605-277">Elle contient la page de codes de la console.</span><span class="sxs-lookup"><span data-stu-id="d2605-277">It holds the console's code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-278"><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-278"><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-279">Identifie une feuille de propriétés particulière dans les pages de propriétés d’une imprimante et indique si cette feuille de propriétés doit être modale.</span><span class="sxs-lookup"><span data-stu-id="d2605-279">Identifies a particular property sheet in a printer's property pages and whether that property sheet should be modal.</span></span> <span data-ttu-id="d2605-280">Éventuellement utilisé avec la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-280">Optionally used with the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-281"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-281"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-282">Stocke des informations pour la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-282">Stores information for the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-283"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>AVEC chevauchement</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-283"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>OVERLAPPED</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-284">Contient des informations utilisées dans les entrées/sorties (e/s) asynchrones (avec chevauchement).</span><span class="sxs-lookup"><span data-stu-id="d2605-284">Contains information used in asynchronous (overlapped) input/output (I/O).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-285"><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-285"><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-286">Utilisé par la fonction <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>ParseUrl</strong></a> pour retourner l’URL analysée.</span><span class="sxs-lookup"><span data-stu-id="d2605-286">Used by the <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>ParseURL</strong></a> function to return the parsed URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-287"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-287"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-288">Spécifie le dossier cible d’un raccourci de dossier et ses attributs.</span><span class="sxs-lookup"><span data-stu-id="d2605-288">Specifies a folder shortcut's target folder and its attributes.</span></span> <span data-ttu-id="d2605-289">Cette structure est utilisée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3 :: GetFolderTargetInfo</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3 :: InitializeEx</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-289">This structure is used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3::GetFolderTargetInfo</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3::InitializeEx</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-290"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-290"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-291">Structure de la table d’accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="d2605-291">Accelerator table structure.</span></span> <span data-ttu-id="d2605-292">Utilisé par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame :: GetWindowContext</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-292">Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame::GetWindowContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-293"><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-293"><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-294">Contient des informations utilisées lors du chargement ou du déchargement d’un profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2605-294">Contains information used when loading or unloading a user profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-295"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-295"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-296">Fournit des informations sur une application publiée à partir d’un éditeur d’application pour <strong>Ajouter/supprimer des programmes</strong> dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d2605-296">Provides information about a published application from an application publisher to <strong>Add/Remove Programs</strong> in Control Panel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-297"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-297"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-298">Contient des informations pour la fusion d’éléments de menu dans des menus de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="d2605-298">Contains information for merging menu items into Windows Explorer menus.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-299"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-299"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-300">Utilisé par la fonction <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> pour décrire une seule interface.</span><span class="sxs-lookup"><span data-stu-id="d2605-300">Used by the <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> function to describe a single interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-301"><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-301"><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-302">Plage de mémoire de type arbitraire qui représente une structure <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> sérialisée.</span><span class="sxs-lookup"><span data-stu-id="d2605-302">A range of memory of arbitrary type that represents a serialized <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> structure.</span></span> <span data-ttu-id="d2605-303">Les programmes ne doivent pas inspecter le contenu d’un <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>; au lieu de cela, ils doivent le manipuler avec les fonctions <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> et <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-303">Programs should not inspect the contents of a <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>; instead, they should manipulate it with the <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> and <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-304"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-304"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-305">Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-305">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-306"><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-306"><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-307">Stocke les informations de position d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d2605-307">Stores position information for an item.</span></span> <span data-ttu-id="d2605-308">Utilisé avec les <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>de message.</span><span class="sxs-lookup"><span data-stu-id="d2605-308">Used with message <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-309"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-309"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-310">Contient le nom d’un fichier d’aide HTML et une rubrique dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="d2605-310">Contains the name of an HTML Help file and a topic in that file.</span></span> <span data-ttu-id="d2605-311">Utilisé avec la notification de <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-311">Used with the <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> notification.</span></span> <span data-ttu-id="d2605-312">Cette structure requiert des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="d2605-312">This structure requires Unicode strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-313"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-313"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-314">Contient les détails d’une page à ajouter à la feuille de <strong>Propriétés</strong> d’un objet.</span><span class="sxs-lookup"><span data-stu-id="d2605-314">Contains the details of a page to be added to an object's <strong>Properties</strong> sheet.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-315"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-315"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-316">Contient les données utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> pour identifier un élément, dans ce cas comme un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, et le processus auquel il est associé.</span><span class="sxs-lookup"><span data-stu-id="d2605-316">Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> to identify both an item—in this case as an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>—and the process that it is associated with.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-317"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-317"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-318">Contient les données utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> pour identifier un élément (dans ce cas par un PIDL absolu) et le processus auquel il est associé.</span><span class="sxs-lookup"><span data-stu-id="d2605-318">Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> to identify both an item—in this case by an absolute PIDL—and the process that it is associated with.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-319"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-319"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-320">Contient des données utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> pour identifier un élément, dans ce cas par le biais d’un <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>, et le processus auquel il est associé.</span><span class="sxs-lookup"><span data-stu-id="d2605-320">Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> to identify both an item, in this case through an <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>, and the process that it is associated with.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-321"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-321"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-322">Contient et reçoit des informations pour les notifications de modification.</span><span class="sxs-lookup"><span data-stu-id="d2605-322">Contains and receives information for change notifications.</span></span> <span data-ttu-id="d2605-323">Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a> et la notification <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-323">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a> function and the <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-324"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-324"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-325">Contient des informations qui identifient un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="d2605-325">Contains information that identifies a particular file.</span></span> <span data-ttu-id="d2605-326">Elle est utilisée par <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider :: GetItemData</strong></a> lors de la demande de données pour un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="d2605-326">It is used by <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> when requesting data for a particular file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-327"><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-327"><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-328">Spécifie l’identificateur FMTID/PID d’une colonne qui sera affichée par l’affichage Détails de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="d2605-328">Specifies the FMTID/PID identifier of a column that will be displayed by the Windows Explorer Details view.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2605-329">À compter de Windows Vista, <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> est considéré comme une forme héritée et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="d2605-329">As of Windows Vista, <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> is considered a legacy form and should not be used.</span></span> <span data-ttu-id="d2605-330">À la place, utilisez la structure <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-330">In its place, use the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> structure.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-331"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-331"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-332">Contient des informations sur les propriétés d’une colonne.</span><span class="sxs-lookup"><span data-stu-id="d2605-332">Contains information about the properties of a column.</span></span> <span data-ttu-id="d2605-333">Elle est utilisée par <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider :: GetColumnInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-333">It is used by <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider::GetColumnInfo</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-334"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-334"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-335">Transmet les informations d’initialisation à <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider :: Initialize</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-335">Passes initialization information to <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider::Initialize</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-336"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-336"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-337">Reçoit des données d’élément en réponse à un appel à <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-337">Receives item data in response to a call to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-338"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-338"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-339">Contient les informations nécessaires pour créer une image de glissement.</span><span class="sxs-lookup"><span data-stu-id="d2605-339">Contains the information needed to create a drag image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-340"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-340"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-341">Définit la ressource d’élément d’environnement.</span><span class="sxs-lookup"><span data-stu-id="d2605-341">Defines Shell item resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-342"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-342"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-343">Fournit des informations détaillées sur un élément dans un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="d2605-343">Reports detailed information on an item in a Shell folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-344"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-344"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-345">Contient des informations utilisées par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-345">Contains information used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-346"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-346"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-347">Contient un jeu d’indicateurs qui indiquent les paramètres d’interpréteur de commandes actuels.</span><span class="sxs-lookup"><span data-stu-id="d2605-347">Contains a set of flags that indicate the current Shell settings.</span></span> <span data-ttu-id="d2605-348">Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-348">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-349"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-349"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-350">Contient les paramètres de l’état de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="d2605-350">Contains settings for the Shell's state.</span></span> <span data-ttu-id="d2605-351">Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-351">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-352"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-352"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-353">Contient des informations sur un objet de fichier.</span><span class="sxs-lookup"><span data-stu-id="d2605-353">Contains information about a file object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-354"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-354"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-355">Contient des informations que la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> utilise pour effectuer des opérations sur les fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-355">Contains information that the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> function uses to perform file operations.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2605-356">À compter de Windows Vista, l’utilisation de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> est recommandée par rapport à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d2605-356">As of Windows Vista, the use of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> interface is recommended over this function.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-357"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-357"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-358">Contient les paramètres des dossiers personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d2605-358">Holds custom folder settings.</span></span> <span data-ttu-id="d2605-359">Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-359">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-360"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-360"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-361">Définit un identificateur d’élément.</span><span class="sxs-lookup"><span data-stu-id="d2605-361">Defines an item identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-362"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-362"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-363">Contient l’ancien et le nouveau nom de chemin d’accès pour chaque fichier déplacé, copié ou renommé par la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-363">Contains the old and new path names for each file that was moved, copied, or renamed by the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-364"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-364"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-365">Contient les informations sur la taille et le nombre d’éléments récupérés par la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-365">Contains the size and item count information retrieved by the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-366"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-366"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-367">Reçoit les informations utilisées pour récupérer une icône d’interpréteur de commandes stock.</span><span class="sxs-lookup"><span data-stu-id="d2605-367">Receives information used to retrieve a stock Shell icon.</span></span> <span data-ttu-id="d2605-368">Cette structure est utilisée dans un appel <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-368">This structure is used in a call <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-369"><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-369"><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-370">Fournit des informations spécialisées sur l’application pour <strong>Ajouter/supprimer des programmes</strong> dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="d2605-370">Provides specialized application information to <strong>Add/Remove Programs</strong> in Control Panel.</span></span> <span data-ttu-id="d2605-371">Cette structure n’est pas applicable aux applications publiées.</span><span class="sxs-lookup"><span data-stu-id="d2605-371">This structure is not applicable to published applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-372"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-372"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-373">Contient des informations sur la notification de modification.</span><span class="sxs-lookup"><span data-stu-id="d2605-373">Contains information about change notification.</span></span> <span data-ttu-id="d2605-374">Elle est utilisée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback :: CallbackSM</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-374">It is used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback::CallbackSM</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-375"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-375"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-376">Contient des informations à partir d’une bande de menus.</span><span class="sxs-lookup"><span data-stu-id="d2605-376">Contains information from a menu band.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-377"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-377"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-378">Contient des informations sur un élément d’une bande de menu.</span><span class="sxs-lookup"><span data-stu-id="d2605-378">Contains information about an item from a menu band.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-379"><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-379"><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-380">Contient des informations sur une mise à jour logicielle.</span><span class="sxs-lookup"><span data-stu-id="d2605-380">Contains information about a software update.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-381"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-381"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-382">Stocke des informations sur la façon de trier une colonne qui est affichée dans l’affichage des dossiers.</span><span class="sxs-lookup"><span data-stu-id="d2605-382">Stores information about how to sort a column that is displayed in the folder view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-383"><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-383"><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-384">Contient des chaînes retournées par les méthodes de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-384">Contains strings returned from the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> interface methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-385"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-385"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-386">Contient les paramètres de la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2 :: CreateViewWindow2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-386">Holds the parameters for the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2::CreateViewWindow2</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-387"><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-387"><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-388">Définit un gestionnaire pour une synchronisation planifiée.</span><span class="sxs-lookup"><span data-stu-id="d2605-388">Defines a handler for a scheduled synchronization.</span></span> <span data-ttu-id="d2605-389">Utilisé avec <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule :: AddItem</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-389">Used with <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule::AddItem</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-390"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-390"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-391">Décrit la structure des informations d’ID de conflit.</span><span class="sxs-lookup"><span data-stu-id="d2605-391">Describes conflict ID information structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-392"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-392"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-393">Fournit des informations sur le gestionnaire à utiliser dans la méthode <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize :: GetHandlerInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-393">Provides information about the handler for use in the <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize::GetHandlerInfo</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-394"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-394"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-395">Fournit des informations sur les éléments qui sont énumérés par l’interface <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-395">Provides information about items being enumerated by the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-396"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-396"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-397">Fournit des informations d’erreur à utiliser dans la méthode <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback :: LogError</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-397">Provides error information for use in the <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback::LogError</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-398"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-398"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-399">Fournit des informations d’État pendant qu’une synchronisation est en cours.</span><span class="sxs-lookup"><span data-stu-id="d2605-399">Provides status information while a synchronization is in progress.</span></span> <span data-ttu-id="d2605-400">Cette structure est utilisée avec la méthode <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback ::P rogress</strong></a> et correspond à un élément de synchronisation unique.</span><span class="sxs-lookup"><span data-stu-id="d2605-400">This structure is used with the <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback::Progress</strong></a> method and corresponds to a single synchronization item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-401"><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-401"><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-402">Utilisé avec la notification de <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> pour spécifier le nombre de boutons à ajouter à la barre d’outils, ainsi que la façon dont ils sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="d2605-402">Used with the <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> notification to specify the number of buttons to add to the toolbar, as well as how they're added.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-403"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-403"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-404">Utilisé par les méthodes de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> pour définir les boutons utilisés dans une barre d’outils incorporée dans la représentation sous forme de miniature d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d2605-404">Used by methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> interface to define buttons used in a toolbar embedded in a window's thumbnail representation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-405"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-405"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-406">Contient les options d’affichage du papier peint.</span><span class="sxs-lookup"><span data-stu-id="d2605-406">Contains the wallpaper display options.</span></span> <span data-ttu-id="d2605-407">Utilisé avec les membres de l’interface <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d2605-407">Used with members of the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-408"><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-408"><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-409">Stocke les données de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d2605-409">Stores window data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-410"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-410"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-411">Spécifie le contexte d’une extraction de miniatures.</span><span class="sxs-lookup"><span data-stu-id="d2605-411">Specifies the context of a thumbnail extraction.</span></span> <span data-ttu-id="d2605-412">Utilisé par <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings :: SetContext</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d2605-412">Used by <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings::SetContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2605-413"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-413"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-414">Valeurs utilisées par <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache :: miniature</strong></a> pour spécifier les options d’extraction et d’affichage de l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="d2605-414">Values used by <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache::GetThumbnail</strong></a> to specify options for the extraction and display of the thumbnail image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2605-415"><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2605-415"><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d2605-416">Contient un identificateur unique pour une miniature dans le cache de miniatures système.</span><span class="sxs-lookup"><span data-stu-id="d2605-416">Contains a unique identifier for a thumbnail in the system thumbnail cache.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 

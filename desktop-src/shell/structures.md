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
# <a name="shell-structures"></a>Structures de Shell

Cette section décrit les structures de l’interpréteur de commandes Windows.

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a><br/></td>
<td>Structure de taille variable qui contient des informations sur un nom de fichier de menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a><br/></td>
<td>Contient des informations sur un élément de menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a><br/></td>
<td>Contient des informations sur un message appbar système.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a><br/></td>
<td>Fournit des informations sur la catégorie application pour ajouter/supprimer des programmes dans le panneau de configuration. La structure <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a> est utilisée pour créer une liste complète des catégories pour un éditeur d’application.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a><br/></td>
<td>Fournit la liste des catégories d’applications prises en charge à partir d’un éditeur d’application pour ajouter/supprimer des programmes dans le panneau de configuration. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a><br/></td>
<td>Fournit des informations sur une application publiée à l’utilitaire ajout/suppression de programmes du panneau de configuration.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a><br/></td>
<td>Définit les informations utilisées par <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> pour récupérer une interface <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> pour une association de fichier donnée.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a><br/></td>
<td>Contient des informations sur une bande de dossiers. Cette structure est utilisée avec les méthodes <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand :: GetBandInfoSFB</strong></a> et <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand :: SetBandInfoSFB</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a><br/></td>
<td>Contient des informations sur un site de bande. Cette structure est utilisée avec les méthodes <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite :: GetBandSiteInfo</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite :: SetBandSiteInfo</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a><br/></td>
<td>Contient des membres protégés de la classe de base. <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> définit l’état du navigateur et est utilisé avec <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2 :: GetBaseBrowserData</strong></a> et <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2 ::P utbasebrowserdata</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a><br/></td>
<td>Définit les coordonnées des angles supérieur gauche et inférieur droit d’un rectangle de bordure.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a><br/></td>
<td>Contient des paramètres pour la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a> et reçoit des informations sur le dossier sélectionné par l’utilisateur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a><br/></td>
<td>Contient des informations de catégorie. Une catégorie de composant est un groupe de classes COM (Component Object Model) liées de manière logique qui partagent un identificateur de catégorie (CATID) commun.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>DESTINÉS</strong></a><br/></td>
<td>Utilisé avec le format de presse-papiers <a href="clipboard.md">CFSTR_SHELLIDLIST</a> pour transférer le pointeur vers une liste d’identificateurs d’élément (PIDL) d’un ou plusieurs objets d’espace de noms de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a><br/></td>
<td>Définit les informations de colonne. Utilisé par les membres de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a><br/></td>
<td>Contient les informations nécessaires à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu :: commande InvokeCommand</strong></a> pour appeler une commande de menu contextuel.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a><br/></td>
<td>Contient des informations étendues sur une commande de menu contextuel. Cette structure est une version étendue de <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> qui permet d’utiliser des valeurs Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a><br/></td>
<td>Utilisé de manière générique pour filtrer les éléments.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>-</strong></a><br/></td>
<td>Utilisé par Windows 2000 pour conserver les informations relatives à un composant. Cette structure remplace la structure <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a><br/></td>
<td>Contient les options d’élément de bureau.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a><br/></td>
<td>Contient des informations sur la position et la taille d’un composant.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a><br/></td>
<td>Utilisé par Windows 2000 pour conserver les informations sur l’état d’un composant.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a><br/></td>
<td>Définit la structure de l’élément en conflit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a><br/></td>
<td>Définit la structure des informations sur les résultats des conflits.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a><br/></td>
<td>Contient des informations sur les ressources et une valeur définie par l’application pour une boîte de dialogue prise en charge par une application du panneau de configuration. La fonction <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> de l’application du panneau de configuration retourne ces informations dans le panneau de configuration en réponse à un message de <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a><br/></td>
<td>Contient des détails sur les informations d’identification.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a><br/></td>
<td>Décrit un champ unique dans les informations d’identification. Par exemple, une chaîne ou une image utilisateur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a><br/></td>
<td>Utilisé avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a><br/></td>
<td>Sert d’en-tête pour certaines structures de données supplémentaires utilisées par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a><br/></td>
<td>Contient les informations de menu contextuel utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a><br/></td>
<td>Utilisé par les dossiers délégués à la place d’une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> standard.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a><br/></td>
<td>Contient des informations détaillées sur un élément de dossier de Shell. Utilisé avec la notification de <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a><br/></td>
<td>Contient des arguments supplémentaires utilisés par <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a><br/></td>
<td>Reçoit des informations de version spécifiques à la DLL. Elle est utilisée avec la fonction <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> . <br/>
<blockquote>
[!Note]<br />
À la place de cette structure, vous pouvez utiliser la structure <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a><br/></td>
<td>Reçoit des informations de version spécifiques à la DLL. Elle est utilisée avec la fonction <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a><br/></td>
<td>Décrit l’image et le texte d’accompagnement pour un objet Drop.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a><br/></td>
<td>Définit le format du presse-papiers <a href="clipboard.md">CF_HDROP</a> . Les données suivantes sont une liste de noms de fichiers se terminant par un caractère null.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a><br/></td>
<td>Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Il contient l’ID de Windows Installer du lien.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a><br/></td>
<td>Stocke les informations sur l’état du lien de l’interpréteur de commandes. Cette structure est utilisée pour les sections de données supplémentaires qui sont marquées avec EXP_PROPERTYSTORAGE_SIG.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a><br/></td>
<td>Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Elle contient des informations sur les dossiers spéciaux.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a><br/></td>
<td>Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Elle contient des chaînes d’environnement développables pour l’icône ou la cible.<br/></td>
</tr>
<tr class="even">
<td><a href="ext-button.md"><strong>EXT_BUTTON</strong></a><br/></td>
<td>Contient des informations sur un bouton que la DLL d’extension du gestionnaire de fichiers ajoute à la barre d’outils du gestionnaire de fichiers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a><br/></td>
<td>Utilisé par un objet énumérateur <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> pour retourner des informations sur les objets de recherche pris en charge par un objet de dossier de l’interpréteur de commandes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a><br/></td>
<td>Contient la définition du format du presse-papiers pour CFSTR_FILE_ATTRIBUTES_ARRAY.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a><br/></td>
<td>Décrit les propriétés d’un fichier copié par le biais du presse-papiers pendant une opération de <a href="dragdrop.md">glisser-déplacer</a> Microsoft ActiveX.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a><br/></td>
<td>Définit le format du presse-papiers CF_FILEGROUPDESCRIPTOR.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a><br/></td>
<td>Contient des informations sur le lecteur sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre du répertoire ou la fenêtre des résultats de la recherche).<br/></td>
</tr>
<tr class="even">
<td><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a><br/></td>
<td>Contient des informations sur un fichier sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre de répertoire ou la fenêtre des résultats de la recherche).<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a><br/></td>
<td>Contient des informations utilisées par le gestionnaire de fichiers pour ajouter une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.<br/></td>
</tr>
<tr class="even">
<td><a href="fms-load.md"><strong>FMS_LOAD</strong></a><br/></td>
<td>Contient des informations utilisées par le gestionnaire de fichiers pour ajouter un menu personnalisé fourni par une DLL d’extension du gestionnaire de fichiers. La structure fournit également une valeur delta que la DLL d’extension peut utiliser pour manipuler le menu personnalisé après le chargement du menu par le gestionnaire de fichiers.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a><br/></td>
<td>Contient des informations sur les boutons personnalisés à ajouter à la barre d’outils du gestionnaire de fichiers. Les boutons sont fournis par une DLL d’extension du gestionnaire de fichiers.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a><br/></td>
<td>Contient des informations sur l’affichage des dossiers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a><br/></td>
<td>Contient des informations utilisées par la visionneuse de fichiers pour afficher un fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a><br/></td>
<td>Contient des informations sur un élément pour lequel une aide contextuelle a été demandée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a><br/></td>
<td>Contient la taille et la position d’une fenêtre d’aide principale ou secondaire. Une application peut définir ces informations en appelant la fonction <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> avec la valeur HELP_SETWINPOS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a><br/></td>
<td>Utilisé par Microsoft Internet Explorer 4,0 et Microsoft Internet Explorer 4,01 pour stocker des informations sur un composant. Avec Windows 2000, il est remplacé par la structure du <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>composant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a><br/></td>
<td>Contient une liste d’identificateurs d’élément.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a><br/></td>
<td>Stocke les dimensions des deux tailles possibles de l’espacement des icônes qui sont disponibles pour l’affichage : petite et grande. Utilisé par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView :: GetItemSpacing</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a><br/></td>
<td>Définit les caractéristiques d’un dossier connu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a><br/></td>
<td>Définit les attributs d’une police.<br/></td>
</tr>
<tr class="odd">
<td><a href="mruinfo.md"><strong>MRUINFO</strong></a><br/></td>
<td>Contient des informations qui définissent une nouvelle liste des derniers fichiers utilisés (MRU). Utilisé par <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a><br/></td>
<td>Spécifie un mot clé à rechercher et la table de mots clés dans laquelle l’aide Windows doit être recherchée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a><br/></td>
<td>Contient des informations qui décrivent une adresse réseau.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a><br/></td>
<td>Décrit une adresse réseau.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a><br/></td>
<td>Contient des informations sur les ressources et une valeur définie par l’application pour une boîte de dialogue prise en charge par une application du panneau de configuration.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a><br/></td>
<td>Contient des informations dont le système a besoin pour afficher les notifications dans la zone de notification. Utilisé par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a><br/></td>
<td>Contient des informations utilisées par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> pour identifier l’icône pour laquelle le rectangle englobant doit être récupéré.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a><br/></td>
<td>Définit le format du presse-papiers CF_NETRESOURCE.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a><br/></td>
<td>Structure de dessin personnalisée utilisée par les méthodes <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a><br/></td>
<td>Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Elle contient les propriétés de la console.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a><br/></td>
<td>Contient un bloc de données supplémentaire utilisé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Elle contient la page de codes de la console.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a><br/></td>
<td>Identifie une feuille de propriétés particulière dans les pages de propriétés d’une imprimante et indique si cette feuille de propriétés doit être modale. Éventuellement utilisé avec la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a><br/></td>
<td>Stocke des informations pour la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>AVEC chevauchement</strong></a><br/></td>
<td>Contient des informations utilisées dans les entrées/sorties (e/s) asynchrones (avec chevauchement).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a><br/></td>
<td>Utilisé par la fonction <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>ParseUrl</strong></a> pour retourner l’URL analysée.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a><br/></td>
<td>Spécifie le dossier cible d’un raccourci de dossier et ses attributs. Cette structure est utilisée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3 :: GetFolderTargetInfo</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3 :: InitializeEx</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a><br/></td>
<td>Structure de la table d’accélérateurs. Utilisé par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame :: GetWindowContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO</strong></a><br/></td>
<td>Contient des informations utilisées lors du chargement ou du déchargement d’un profil utilisateur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a><br/></td>
<td>Fournit des informations sur une application publiée à partir d’un éditeur d’application pour <strong>Ajouter/supprimer des programmes</strong> dans le panneau de configuration.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a><br/></td>
<td>Contient des informations pour la fusion d’éléments de menu dans des menus de l’Explorateur Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a><br/></td>
<td>Utilisé par la fonction <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> pour décrire une seule interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a><br/></td>
<td>Plage de mémoire de type arbitraire qui représente une structure <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> sérialisée. Les programmes ne doivent pas inspecter le contenu d’un <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>; au lieu de cela, ils doivent le manipuler avec les fonctions <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> et <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a><br/></td>
<td>Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a><br/></td>
<td>Stocke les informations de position d’un élément. Utilisé avec les <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>de message.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a><br/></td>
<td>Contient le nom d’un fichier d’aide HTML et une rubrique dans ce fichier. Utilisé avec la notification de <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> . Cette structure requiert des chaînes Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a><br/></td>
<td>Contient les détails d’une page à ajouter à la feuille de <strong>Propriétés</strong> d’un objet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a><br/></td>
<td>Contient les données utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> pour identifier un élément, dans ce cas comme un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, et le processus auquel il est associé.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a><br/></td>
<td>Contient les données utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> pour identifier un élément (dans ce cas par un PIDL absolu) et le processus auquel il est associé.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a><br/></td>
<td>Contient des données utilisées par <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> pour identifier un élément, dans ce cas par le biais d’un <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>, et le processus auquel il est associé.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a><br/></td>
<td>Contient et reçoit des informations pour les notifications de modification. Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a> et la notification <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a><br/></td>
<td>Contient des informations qui identifient un fichier particulier. Elle est utilisée par <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider :: GetItemData</strong></a> lors de la demande de données pour un fichier particulier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a><br/></td>
<td>Spécifie l’identificateur FMTID/PID d’une colonne qui sera affichée par l’affichage Détails de l’Explorateur Windows. <br/>
<blockquote>
[!Note]<br />
À compter de Windows Vista, <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> est considéré comme une forme héritée et ne doit pas être utilisé. À la place, utilisez la structure <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a><br/></td>
<td>Contient des informations sur les propriétés d’une colonne. Elle est utilisée par <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider :: GetColumnInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a><br/></td>
<td>Transmet les informations d’initialisation à <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider :: Initialize</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a><br/></td>
<td>Reçoit des données d’élément en réponse à un appel à <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a><br/></td>
<td>Contient les informations nécessaires pour créer une image de glissement.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a><br/></td>
<td>Définit la ressource d’élément d’environnement.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a><br/></td>
<td>Fournit des informations détaillées sur un élément dans un dossier de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a><br/></td>
<td>Contient des informations utilisées par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a><br/></td>
<td>Contient un jeu d’indicateurs qui indiquent les paramètres d’interpréteur de commandes actuels. Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a><br/></td>
<td>Contient les paramètres de l’état de l’interpréteur de commandes. Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a><br/></td>
<td>Contient des informations sur un objet de fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a><br/></td>
<td>Contient des informations que la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> utilise pour effectuer des opérations sur les fichiers. <br/>
<blockquote>
[!Note]<br />
À compter de Windows Vista, l’utilisation de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> est recommandée par rapport à cette fonction.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a><br/></td>
<td>Contient les paramètres des dossiers personnalisés. Cette structure est utilisée avec la fonction <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a><br/></td>
<td>Définit un identificateur d’élément.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a><br/></td>
<td>Contient l’ancien et le nouveau nom de chemin d’accès pour chaque fichier déplacé, copié ou renommé par la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a><br/></td>
<td>Contient les informations sur la taille et le nombre d’éléments récupérés par la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a><br/></td>
<td>Reçoit les informations utilisées pour récupérer une icône d’interpréteur de commandes stock. Cette structure est utilisée dans un appel <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a><br/></td>
<td>Fournit des informations spécialisées sur l’application pour <strong>Ajouter/supprimer des programmes</strong> dans le panneau de configuration. Cette structure n’est pas applicable aux applications publiées.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a><br/></td>
<td>Contient des informations sur la notification de modification. Elle est utilisée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback :: CallbackSM</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a><br/></td>
<td>Contient des informations à partir d’une bande de menus.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a><br/></td>
<td>Contient des informations sur un élément d’une bande de menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a><br/></td>
<td>Contient des informations sur une mise à jour logicielle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a><br/></td>
<td>Stocke des informations sur la façon de trier une colonne qui est affichée dans l’affichage des dossiers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a><br/></td>
<td>Contient des chaînes retournées par les méthodes de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a><br/></td>
<td>Contient les paramètres de la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2 :: CreateViewWindow2</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a><br/></td>
<td>Définit un gestionnaire pour une synchronisation planifiée. Utilisé avec <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule :: AddItem</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a><br/></td>
<td>Décrit la structure des informations d’ID de conflit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a><br/></td>
<td>Fournit des informations sur le gestionnaire à utiliser dans la méthode <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize :: GetHandlerInfo</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a><br/></td>
<td>Fournit des informations sur les éléments qui sont énumérés par l’interface <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a><br/></td>
<td>Fournit des informations d’erreur à utiliser dans la méthode <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback :: LogError</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a><br/></td>
<td>Fournit des informations d’État pendant qu’une synchronisation est en cours. Cette structure est utilisée avec la méthode <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback ::P rogress</strong></a> et correspond à un élément de synchronisation unique.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a><br/></td>
<td>Utilisé avec la notification de <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> pour spécifier le nombre de boutons à ajouter à la barre d’outils, ainsi que la façon dont ils sont ajoutés.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a><br/></td>
<td>Utilisé par les méthodes de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> pour définir les boutons utilisés dans une barre d’outils incorporée dans la représentation sous forme de miniature d’une fenêtre.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a><br/></td>
<td>Contient les options d’affichage du papier peint. Utilisé avec les membres de l’interface <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a><br/></td>
<td>Stocke les données de fenêtre.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a><br/></td>
<td>Spécifie le contexte d’une extraction de miniatures. Utilisé par <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings :: SetContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a><br/></td>
<td>Valeurs utilisées par <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache :: miniature</strong></a> pour spécifier les options d’extraction et d’affichage de l’image miniature.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a><br/></td>
<td>Contient un identificateur unique pour une miniature dans le cache de miniatures système.<br/></td>
</tr>
</tbody>
</table>



 

 

 

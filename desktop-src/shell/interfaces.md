---
description: cette section décrit les interfaces de l’interpréteur de commandes Windows.
title: Interfaces Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 05223970-14f5-44c2-937b-07826b8aecf9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8bf8a0669666ae45ba79fda014a8b3b92b57a974b6f72e06303c6c8a2e368bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032367"
---
# <a name="shell-interfaces"></a>Interfaces Shell

cette section décrit les interfaces de l’interpréteur de commandes Windows.

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
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iaccessibleobject"><strong>IAccessibleObject</strong></a><br/></td>
<td>Expose une méthode qui peut être utilisée par une application d’accessibilité.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)"><strong>IAccessibilityDockingService</strong></a><br/></td>
<td>Ancre une fenêtre d’application d’accessibilité unique au bas d’un écran.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh448547(v=vs.85)"><strong>IAccessibilityDockingServiceCallback</strong></a><br/></td>
<td>Informe une application d’accessibilité que sa fenêtre a été détachée.<br/></td>
</tr>
<tr class="even">
<td><a href="iaclcustommru.md"><strong>IACLCustomMRU</strong></a><br/></td>
<td>Expose les méthodes utilisées pour initialiser une liste des derniers fichiers utilisés pour un objet de saisie semi-automatique.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a><br/></td>
<td>Expose une méthode qui améliore l’efficacité de la <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>saisie semi-automatique</strong></a> lorsque les chaînes candidates sont organisées dans une hiérarchie.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2"><strong>IACList2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a> pour permettre aux clients d’un objet de saisie semi-automatique de récupérer et de définir des indicateurs d’option.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a><br/></td>
<td>Représente la classe de base abstraite à partir de laquelle les opérations pilotées par progression peuvent hériter.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogressdialog"><strong>IActionProgressDialog</strong></a><br/></td>
<td>Expose des méthodes qui initialisent et arrêtent une boîte de dialogue de progression.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager"><strong>IApplicationActivationManager</strong></a><br/></td>
<td>fournit des méthodes qui activent Windows les applications du windows Store pour les <a href="/previous-versions/windows/apps/hh464906(v=win.10)">extensions</a>de lancement, de fichier et de protocole. Normalement, vous utiliserez cette interface dans les débogueurs et les outils de conception.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a><br/></td>
<td>Expose des méthodes qui interrogent et définissent des applications par défaut pour un <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>type d’association</strong></a>de fichier spécifique et des protocoles à un <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>niveau d’association</strong></a>spécifique. <br/>
<blockquote>
[!Note]<br />
à partir de Windows 8, les seules fonctionnalités de cette interface prises en charge sont <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault"><strong>QueryCurrentDefault</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui"><strong>IApplicationAssociationRegistrationUI</strong></a><br/></td>
<td>Expose une méthode qui lance une boîte de dialogue Association avancée par le biais de laquelle l’utilisateur peut personnaliser ses associations.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings"><strong>IApplicationDesignModeSettings</strong></a><br/></td>
<td>permet aux applications de l’outil de développement d’usurper dynamiquement les états système et utilisateur, tels que la résolution d’affichage native, le facteur d’échelle de l’appareil et l’état d’affichage de l’application, dans le but de tester Windows applications du windows Store qui s’exécutent en mode création pour un large éventail de facteurs de forme sans avoir besoin du matériel réel. permet également de tester les modifications de l’état contrôlé par l’utilisateur normalement afin de tester les applications de Windows store dans un large éventail de scénarios.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2"><strong>IApplicationDesignModeSettings2</strong></a><br/></td>
<td>permet aux applications de l’outil de développement de contrôler de manière dynamique les états utilisateur et système, tels que la résolution d’affichage native, le facteur d’échelle de l’appareil et la disposition de la vue de l’application, signalés à Windows applications du windows store afin de Windows tester les applications du windows store qui s’exécutent en mode création pour un large éventail de facteurs de forme sans avoir besoin du matériel permet également de tester les modifications de l’état contrôlé par l’utilisateur normalement afin de tester les applications de Windows store dans un large éventail de scénarios.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations"><strong>IApplicationDestinations</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application de supprimer une ou toutes les destinations des catégories <strong>récentes</strong> ou <strong>fréquentes</strong> dans une liste de raccourcis.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists"><strong>IApplicationDocumentLists</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application de récupérer le contenu des catégories <strong>récentes</strong> ou <strong>fréquentes</strong> dans une liste de raccourcis.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher"><strong>IAppPublisher</strong></a><br/></td>
<td>Expose des méthodes pour la publication d’applications via <strong>Ajout/suppression de programmes</strong> dans le panneau de configuration. Il s’agit de l’interface principale implémentée à cet effet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility"><strong>IAppVisibility</strong></a><br/></td>
<td>fournit des fonctionnalités permettant de déterminer si l’affichage affiche des applications Windows store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents"><strong>IAppVisibilityEvents</strong></a><br/></td>
<td>Permet aux applications de recevoir des notifications de modifications d’État dans un affichage et de modifications de la visibilité de l’écran de démarrage.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a><br/></td>
<td>Expose des méthodes pour les opérations avec une boîte de dialogue ou un menu d’association de fichiers.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker"><strong>IAssocHandlerInvoker</strong></a><br/></td>
<td>Expose les méthodes qui appellent un gestionnaire d’application associé.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute"><strong>IAttachmentExecute</strong></a><br/></td>
<td>Expose des méthodes qui fonctionnent avec les applications clientes pour présenter un environnement utilisateur qui permet de télécharger et d’échanger des fichiers en toute sécurité via des pièces jointes de messagerie électronique et de messagerie.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a><br/></td>
<td>Exposé par l’objet de saisie semi-automatique (CLSID_AutoComplete). Cette interface permet aux applications d’initialiser, d’activer et de désactiver l’objet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete2"><strong>IAutoComplete2</strong></a><br/></td>
<td>Étend <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a>. Cette interface permet aux clients de l’objet de saisie semi-automatique de récupérer et de définir un certain nombre d’options qui contrôlent le fonctionnement de la saisie semi-automatique.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iautocompletedropdown"><strong>IAutoCompleteDropDown</strong></a><br/></td>
<td>Expose des méthodes qui permettent aux clients de réinitialiser ou d’interroger l’état d’affichage de la liste déroulante de saisie semi-automatique, qui contient les saisies semi-automatiques possibles dans une chaîne entrée par l’utilisateur dans un contrôle d’édition.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ibandhost"><strong>IBandHost</strong></a><br/></td>
<td>Expose des méthodes qui créent et détruisent des bandes et spécifient leur disponibilité.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite"><strong>IBandSite</strong></a><br/></td>
<td>Expose des méthodes qui contrôlent des objets de bande.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ibrowserframeoptions"><strong>IBrowserFrameOptions</strong></a><br/></td>
<td>Permet à un navigateur ou à un hôte de demander à <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> quel type de comportement d’affichage est pris en charge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategorizer"><strong>ICategorizer</strong></a><br/></td>
<td>Expose les méthodes utilisées pour obtenir des informations sur les listes d’identificateurs d’éléments.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategoryprovider"><strong>ICategoryProvider</strong></a><br/></td>
<td>Expose une liste de catégoriseurs inscrits sur un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburn"><strong>ICDBurn</strong></a><br/></td>
<td>Expose des méthodes qui déterminent si un système dispose d’un matériel pour écrire sur CD, la lettre de lecteur d’un graveur de CD et initier une session de gravure de CD par programmation. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a><br/></td>
<td>expose des méthodes qui activent l’inspection et la manipulation de colonnes dans l’affichage détails de l’explorateur de Windows. Chaque colonne est référencée par une structure <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> , qui nomme une propriété.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a><br/></td>
<td>Exposée par les boîtes de dialogue de fichier courantes à utiliser lorsqu’elles hébergent un navigateur d’interpréteur de commandes. S’il est pris en charge, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a> expose des méthodes qui permettent à une vue de Shell de gérer plusieurs cas qui requièrent un comportement différent dans une boîte de dialogue que dans une vue de Shell normale. Vous obtenez un pointeur d’interface <strong>ICommDlgBrowser</strong> en appelant <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> sur l’objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a><br/></td>
<td>Étend les fonctionnalités de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a>. Cette interface est exposée par les boîtes de dialogue de fichier courantes lorsqu’elles hébergent un navigateur d’interpréteur de commandes. Un pointeur vers <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a> peut être obtenu en appelant <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> sur l’objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icommdlgbrowser3"><strong>ICommDlgBrowser3</strong></a><br/></td>
<td>Étend les fonctionnalités de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>et utilisées par les boîtes de dialogue de fichier courantes lorsqu’elles hébergent un navigateur d’interpréteur de commandes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-icomputerinfochangenotify"><strong>IComputerInfoChangeNotify</strong></a><br/></td>
<td>Cette interface peut être absente dans les versions ultérieures de Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a><br/></td>
<td>Expose des méthodes pour la connexion et la déconnexion des objets <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>IContactManagerInterop</strong></a><br/></td>
<td>Permet d’accéder aux méthodes <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>ContactManager</strong></a> dans une application qui gère plusieurs fenêtres.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a><br/></td>
<td>Expose les méthodes qui créent ou fusionnent un menu contextuel associé à un objet Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a><br/></td>
<td>Expose des méthodes qui créent ou fusionnent un menu contextuel (contexte) associé à un objet Shell. Étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> en ajoutant une méthode qui permet aux objets clients de gérer des messages associés à des éléments de menu owner-drawn.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3"><strong>IContextMenu3</strong></a><br/></td>
<td>Expose les méthodes qui créent ou fusionnent un menu contextuel associé à un objet Shell. Permet aux objets clients de gérer des messages associés à des éléments de menu owner-drawn et étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a> en acceptant une valeur de retour de cette gestion des messages.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb"><strong>IContextMenuCB</strong></a><br/></td>
<td>Expose une méthode qui active le rappel d’un menu contextuel. Par exemple, pour ajouter une icône de bouclier à un <strong>MenuItem</strong> qui requiert une élévation.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb776063(v=vs.85)"><strong>IControlMarkup</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)"><strong>ICopyHook</strong></a><br/></td>
<td>Expose une méthode qui crée un <em>Gestionnaire de raccordement de copie</em>. Un gestionnaire de raccordement de copie est une extension de Shell qui détermine si un dossier shell ou un objet Printer peut être déplacé, copié, renommé ou supprimé. L’interpréteur de commandes appelle la méthode <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)"><strong>ICopyHook :: CopyCallback</strong></a> avant d’exécuter l’une de ces opérations.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a><br/></td>
<td>Expose une méthode qui crée un objet d’une classe spécifiée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a><br/></td>
<td>Utilisé par <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> pour permettre à l’appelant de modifier certains paramètres du processus en cours de création.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs"><strong>ICreateProcessInputs</strong></a><br/></td>
<td>Utilisé par l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a> pour modifier certains paramètres du processus en cours de création.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovider"><strong>ICredentialProvider</strong></a><br/></td>
<td>Expose les méthodes utilisées lors de l’installation et de la manipulation d’un fournisseur d’informations d’identification. Tous les fournisseurs d’informations d’identification doivent implémenter cette interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a><br/></td>
<td>Expose des méthodes qui permettent de gérer des informations d’identification.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredential2"><strong>ICredentialProviderCredential2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a> en ajoutant une méthode qui récupère l’identificateur de sécurité (SID) d’un utilisateur. Les informations d’identification sont associées à cet utilisateur et peuvent être regroupées sous la vignette de l’utilisateur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a><br/></td>
<td>Fournit un mécanisme de rappel asynchrone utilisé par les informations d’identification pour les notifier des événements de modification d’État ou de texte dans l’interface utilisateur d’ouverture de session ou l’interface utilisateur des informations d’identification.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialevents2"><strong>ICredentialProviderCredentialEvents2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a> en ajoutant des méthodes qui activent la mise à jour par lots des champs dans l’interface utilisateur theLogon ou l’interface utilisateur des informations d’identification.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions"><strong>ICredentialProviderCredentialWithFieldOptions</strong></a><br/></td>
<td>Fournit une méthode qui permet à l’infrastructure du fournisseur d’informations d’identification de déterminer si vous avez apporté une personnalisation à l’option d’un champ dans une connexion ou une interface utilisateur d’informations d’identification.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderevents"><strong>ICredentialProviderEvents</strong></a><br/></td>
<td>Fournit un mécanisme de rappel asynchrone utilisé par un fournisseur d’informations d’identification pour notifier les modifications apportées à la liste des informations d’identification ou à leurs champs.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderfilter"><strong>ICredentialProviderFilter</strong></a><br/></td>
<td>Utilisé pour filtrer dynamiquement les fournisseurs d’informations d’identification en fonction des informations disponibles au moment de l’exécution.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidersetuserarray"><strong>ICredentialProviderSetUserArray</strong></a><br/></td>
<td>Fournit une méthode qui permet à un fournisseur d’informations d’identification de recevoir l’ensemble des utilisateurs qui seront affichés dans l’interface utilisateur d’ouverture de session ou d’informations d’identification.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruser"><strong>ICredentialProviderUser</strong></a><br/></td>
<td>Fournit des méthodes utilisées pour récupérer certaines propriétés d’un utilisateur individuel incluses dans une connexion ou une interface utilisateur d’informations d’identification.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruserarray"><strong>ICredentialProviderUserArray</strong></a><br/></td>
<td>Représente l’ensemble des utilisateurs qui s’affichent dans l’interface utilisateur de connexion ou d’informations d’identification. Ces informations permettent au fournisseur d’informations d’identification d’énumérer le jeu pour récupérer les informations de propriété de chaque utilisateur afin de remplir les champs ou de filtrer le jeu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem"><strong>ICurrentItem</strong></a><br/></td>
<td>Obtenu en appelant <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> pour un élément. Si l’élément représente un instantané d’un élément à un moment antérieur, cette interface obtient la version actuelle de l’élément.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory"><strong>ICurrentWorkingDirectory</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un client de récupérer ou de définir le répertoire de travail actuel d’un objet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist"><strong>ICustomDestinationList</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application de fournir une liste de raccourcis personnalisée, y compris des destinations et des tâches, à afficher dans la barre des tâches.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability"><strong>IDataObjectAsyncCapability</strong></a><br/></td>
<td>Active les interfaces qui sont généralement synchrones pour fonctionner de façon asynchrone. <br/>
<blockquote>
[!Note]<br />
Cette interface est la version actuelle, renommée de <a href="/previous-versions//bb776309(v=vs.85)"><strong>IAsyncOperation</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider"><strong>IDataObjectProvider</strong></a><br/></td>
<td>Fournit des méthodes qui vous permettent de définir ou de récupérer l' <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>interface IDataObject</strong></a>d’un objet <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage?view=winrt-19041">DataPackage</a> , que DataPackage utilise pour prendre en charge l’interopérabilité. L’objet DataPackage est utilisé par une application pour fournir des données à une autre application.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop"><strong>IDataTransferManagerInterop</strong></a><br/></td>
<td>permet l’accès aux méthodes <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataTransferManager"><strong>DataTransferManager</strong></a> dans Windows une application du windows Store qui gère plusieurs fenêtres.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a><br/></td>
<td>Expose des méthodes pour définir des icônes par défaut associées à un objet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize"><strong>IDefaultFolderMenuInitialize</strong></a><br/></td>
<td>Fournit des méthodes utilisées pour récupérer et définir des informations de menu contextuel. Ces informations sont les mêmes que celles fournies à <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a> via la structure <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-idelayedpropertystorefactory"><strong>IDelayedPropertyStoreFactory</strong></a><br/></td>
<td>Expose une méthode pour créer un objet <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> spécifié dans les cas où l’accès à la propriété est potentiellement lent.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder"><strong>IDelegateFolder</strong></a><br/></td>
<td>Expose une méthode par le biais de laquelle un dossier délégué reçoit l’interface <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> requise pour allouer et libérer des ID d’élément.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegateitem"><strong>IDelegateItem</strong></a><br/></td>
<td>Permet d’obtenir la représentation sous-jacente immédiatement du chemin d’accès d’un élément.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idesktopgadget"><strong>IDesktopGadget</strong></a><br/></td>
<td>Expose une méthode qui permet l’ajout par programme d’un gadget installé sur le Bureau de l’utilisateur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper"><strong>IDesktopWallpaper</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory"><strong>IDestinationStreamFactory</strong></a><br/></td>
<td>Expose une méthode pour copier manuellement un flux ou un fichier avant d’appliquer les modifications apportées aux propriétés.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem"><strong>IDisplayItem</strong></a><br/></td>
<td>Expose des méthodes qui recherchent une version de l’élément actuel à utiliser pour obtenir des propriétés d’affichage, telles que le nom de l’élément, qui seront affichées dans l’interface utilisateur. Utilisé par les boîtes de dialogue du moteur de copie pour fournir à l’interface utilisateur un élément approprié à afficher. Si aucune autre version n’est trouvée, l’élément actuel est utilisé.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a><br/></td>
<td>Expose des méthodes qui notifient l’objet de fenêtre d’ancrage des modifications, notamment l’affichage, le masquage et la suppression imminente. cette interface est implémentée par les objets de fenêtre qui peuvent être ancrés dans l’espace de bordure d’une fenêtre de l’explorateur de Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe"><strong>IDockingWindowFrame</strong></a><br/></td>
<td>Expose des méthodes qui prennent en charge l’ajout d’objets <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> à un frame. Implémenté par le navigateur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite"><strong>IDockingWindowSite</strong></a><br/></td>
<td>Expose des méthodes qui gèrent l’espace de bordure pour un ou plusieurs objets <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> . Cette interface est implémentée par le navigateur et est semblable à l’interface <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow"><strong>IOleInPlaceUIWindow</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a><br/></td>
<td>Exposé par le Shell pour permettre à une application de spécifier l’image qui sera affichée pendant une opération de glisser-déplacer de l’interpréteur de commandes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idragsourcehelper2"><strong>IDragSourceHelper2</strong></a><br/></td>
<td>Expose une méthode qui ajoute des fonctionnalités à <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a>. Cette méthode définit les caractéristiques d’une opération de glisser-déplacer sur un objet <strong>IDragSourceHelper</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper"><strong>IDropTargetHelper</strong></a><br/></td>
<td>Expose des méthodes qui autorisent les cibles de dépôt à afficher une image de glissement pendant que l’image se trouve sur la fenêtre cible.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idynamichwhandler"><strong>IDynamicHWHandler</strong></a><br/></td>
<td>Appelée par l’exécution automatique. Expose des méthodes qui obtiennent des informations dynamiques concernant un gestionnaire inscrit avant de l’afficher à l’utilisateur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers"><strong>IEnumAssocHandlers</strong></a><br/></td>
<td>Expose une méthode qui autorise l’énumération d’une collection de gestionnaires associés à des extensions de nom de fichier particulières.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumerableview"><strong>IEnumerableView</strong></a><br/></td>
<td>Expose des méthodes qui énumèrent le contenu d’une vue et reçoivent une notification du rappel à la fin de l’énumération. Cette interface permet aux clients d’une vue de tenter de partager la liste de contenu des dossiers de la vue.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand"><strong>IEnumExplorerCommand</strong></a><br/></td>
<td>Fourni par un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a>. Cette interface contient l’énumération des commandes à placer dans la barre de commandes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a><br/></td>
<td>Énumérateur OLE standard utilisé par un client pour déterminer les objets de recherche disponibles pour un dossier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist"><strong>IEnumFullIDList</strong></a><br/></td>
<td>Expose un ensemble standard de méthodes qui énumèrent les pointeurs vers les listes d’identificateurs d’élément (PIDL) des éléments d’un dossier de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a><br/></td>
<td>Expose un ensemble standard de méthodes utilisées pour énumérer les PIDL des éléments dans un dossier de Shell. Quand la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder :: EnumObjects</strong></a> d’un dossier est appelée, elle crée un objet d’énumération et passe à l’application appelante un pointeur vers l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a> de l’objet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects"><strong>IEnumObjects</strong></a><br/></td>
<td>Expose des méthodes pour énumérer des objets inconnus.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps"><strong>IEnumPublishedApps</strong></a><br/></td>
<td>Expose des méthodes qui énumèrent les applications publiées dans Ajout/suppression de programmes dans le panneau de configuration. L’objet exposant cette interface est demandé via <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-iapppublisher-enumapps"><strong>IAppPublisher :: EnumApps</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumreadycallback"><strong>IEnumReadyCallback</strong></a><br/></td>
<td>Expose des méthodes qui permettent à la vue de notifier l’implémenteur lorsque l’énumération est terminée. La vue appelle cette méthode pour indiquer à l’implémenteur que l’énumération peut être récupérée via <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents"><strong>IEnumerableView :: CreateEnumIDListFromContents</strong></a>. Le rappel permet à l’implémenteur de partager l’énumération views.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources"><strong>IEnumResources</strong></a><br/></td>
<td>Expose des méthodes d’énumération des ressources.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a><br/></td>
<td>Expose l’énumération des interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> . Cette interface est généralement obtenue en appelant la méthode <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrconflict"><strong>IEnumSyncMgrConflict</strong></a><br/></td>
<td>Expose des méthodes d’énumération de conflits.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrevents"><strong>IEnumSyncMgrEvents</strong></a><br/></td>
<td>Expose les méthodes d’énumération des événements de synchronisation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems"><strong>IEnumSyncMgrSyncItems</strong></a><br/></td>
<td>Expose des méthodes qui énumèrent les objets d’élément de synchronisation managés par le gestionnaire.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a><br/></td>
<td>Expose des méthodes qui définissent un État ou un paramètre donné en rapport avec le verbe de commande, ainsi qu’une méthode pour appeler ce verbe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment"><strong>IExecuteCommandApplicationHostEnvironment</strong></a><br/></td>
<td>Fournit une méthode unique qui permet à une application de déterminer si son hôte est en mode de bureau ou en mode immersif.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost"><strong>IExecuteCommandHost</strong></a><br/></td>
<td>Fournit une méthode qui permet à un gestionnaire de verbes de Shell basé sur <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a>d’interroger le mode d’interface utilisateur du composant hôte à partir duquel l’application a été appelée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> est un objet de navigateur qui peut être parcouru ou qui peut héberger une vue d’un objet de données. En tant qu’objet de navigateur complet, il prend également en charge un journal de voyage automatique.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents"><strong>IExplorerBrowserEvents</strong></a><br/></td>
<td>Expose des méthodes pour la notification de navigation dans le navigateur de l’Explorateur et d’affichage des événements de création.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent l’apparence de la commande, énumérent des sous-commandes ou appellent la commande.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a><br/></td>
<td>Expose des méthodes pour créer des commandes et des énumérateurs de commandes de l’Explorateur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a><br/></td>
<td>Expose une méthode unique qui permet la récupération de l’état de la commande.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a><br/></td>
<td>utilisé dans Windows Explorer par une implémentation de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> pour fournir des suggestions sur les volets qui sont visibles. En outre, un hôte <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> peut utiliser cette interface pour fournir des informations sur la visibilité des volets. L’hôte doit implémenter <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> avec <strong>SID_ExplorerPaneVisibility</strong> comme ID de service. L’hôte doit se trouver dans la chaîne de sites. <br/> L’implémentation de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> est récupérée à partir du dossier shell. Le dossier shell, à son tour, est récupéré à partir de la vue. Une extension d’espace de noms peut choisir de fournir une vue personnalisée (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>) au lieu d’utiliser l’objet de vue de dossier système (DefView). Dans ce cas, l’implémentation de <strong>IShellView</strong> doit inclure une implémentation de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView :: GetFolder</strong></a> pour retourner l’objet <strong>IExplorerPaneVisibility</strong> .<br/> Une extension d’espace de noms peut fournir une vue personnalisée en implémentant <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> elle-même au lieu d’utiliser l’objet de vue de dossier système (DefView). Dans ce cas, l’implémentation de <strong>IShellView</strong> doit inclure une implémentation de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView :: GetFolder</strong></a> pour utiliser <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona"><strong>IExtractIcon</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un client de récupérer l’icône associée à l’un des objets dans un dossier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a><br/></td>
<td>Expose des méthodes qui demandent une image miniature d’un dossier shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2"><strong>IExtractImage2</strong></a><br/></td>
<td>Étend les fonctionnalités de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a><br/></td>
<td>Expose des méthodes qui initialisent, affichent et obtiennent des résultats de la boîte de dialogue de fichier commune.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialog2"><strong>IFileDialog2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> en fournissant des méthodes qui permettent à l’appelant de nommer un emplacement restreint spécifique qui peut être parcouru dans la boîte de dialogue de fichier commune et de spécifier un texte de remplacement à afficher en tant qu’étiquette sur le bouton <strong>Annuler</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents"><strong>IFileDialogControlEvents</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application d’être avertie des événements liés aux contrôles que l’application a ajoutés à une boîte de dialogue de fichier commune.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application d’ajouter des contrôles à une boîte de dialogue de fichier commune.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents"><strong>IFileDialogEvents</strong></a><br/></td>
<td>Expose des méthodes qui autorisent la notification d’événements dans une boîte de dialogue de fichier commune.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse"><strong>IFileIsInUse</strong></a><br/></td>
<td>Expose des méthodes qui peuvent être appelées pour obtenir des informations sur ou fermer un fichier en cours d’utilisation par une autre application. Lorsqu’une application tente d’accéder à un fichier et trouve que ce fichier est déjà utilisé, elle peut utiliser les méthodes de cette interface pour collecter des informations à présenter à l’utilisateur dans une boîte de dialogue.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog"><strong>IFileOpenDialog</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> en ajoutant des méthodes spécifiques à la boîte de dialogue Ouvrir.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a><br/></td>
<td>Expose des méthodes pour copier, déplacer, renommer, créer et supprimer des éléments de Shell, ainsi que des méthodes pour fournir des boîtes de dialogue de progression et d’erreur. Cette interface remplace la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink"><strong>IFileOperationProgressSink</strong></a><br/></td>
<td>Expose des méthodes qui fournissent un système de notification riche utilisé par les appelants d' <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> pour analyser les détails des opérations qu’ils effectuent via cette interface.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog"><strong>IFileSaveDialog</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> en ajoutant des méthodes spécifiques à la boîte de dialogue Enregistrer, qui incluent celles qui fournissent la prise en charge de la collection de métadonnées à rendre persistante avec le fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler"><strong>IFileSyncMergeHandler</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a><br/></td>
<td>Expose des méthodes qui stockent des informations de système de fichiers pour l’optimisation des appels à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a><br/></td>
<td>Étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a>, qui stocke les informations de système de fichiers pour l’optimisation des appels à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a>. Cette interface ajoute la capacité définie ou obtient l’ID de fichier ou l’identificateur de classe de jonction (CLSID).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/schema-library-iconreference"><strong>IFileViewer</strong></a><br/></td>
<td>Expose des méthodes qui désignent une interface qui permet à une visionneuse de fichiers inscrite d’être notifiée lorsqu’elle doit afficher ou imprimer un fichier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite"><strong>IFileViewerSite</strong></a><br/></td>
<td>Expose des méthodes qui désignent une interface qui permet à une visionneuse de fichiers d’extraire le handle de la fenêtre épinglée actuelle ou de définir une nouvelle fenêtre épinglée. La fenêtre épinglée est la fenêtre dans laquelle la visionneuse de fichiers active affiche un fichier. Lorsque l’utilisateur sélectionne un nouveau fichier à afficher, l’interpréteur de commandes demande à la visionneuse de fichiers d’afficher le nouveau fichier dans la fenêtre épinglée au lieu de créer une nouvelle fenêtre.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter"><strong>IFolderFilter</strong></a><br/></td>
<td>Exposé par un client pour spécifier comment filtrer l’énumération d’un dossier shell par une application serveur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite"><strong>IFolderFilterSite</strong></a><br/></td>
<td>Exporté par un hôte pour permettre aux clients de spécifier comment filtrer une énumération de dossiers de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a><br/></td>
<td>Expose des méthodes qui récupèrent des informations sur les options d’affichage d’un dossier, sélectionnent les éléments spécifiés dans ce dossier et définissent le mode d’affichage du dossier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a><br/></td>
<td>Expose des méthodes qui récupèrent des informations sur les options d’affichage d’un dossier, sélectionnent les éléments spécifiés dans ce dossier et définissent le mode d’affichage du dossier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewhost"><strong>IFolderViewHost</strong></a><br/></td>
<td>Expose une méthode qui héberge un objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a> dans une fenêtre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a><br/></td>
<td>expose des méthodes qui permettent le contrôle des options d’affichage des dossiers spécifiques aux affichages Windows 7 et versions ultérieures.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderviewsettings"><strong>IFolderViewSettings</strong></a><br/></td>
<td>Expose des méthodes pour obtenir des paramètres d’affichage des dossiers.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane"><strong>IFrameworkInputPane</strong></a><br/></td>
<td>Fournit des méthodes qui permettent aux applications d’être informées des modifications d’État et de l’emplacement du volet d’entrée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler"><strong>IFrameworkInputPaneHandler</strong></a><br/></td>
<td>Permet à une application d’être avertie lorsque le volet entrée (le clavier visuel ou le panneau écriture manuscrite) est affiché ou masqué. Cela permet à la fenêtre d’application d’ajuster son affichage afin qu’aucune zone d’entrée (telle qu’une zone de texte) ne soit obscurcie par le volet d’entrée.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo"><strong>IHandlerInfo</strong></a><br/></td>
<td>Fournit des méthodes qui fournissent des informations sur le gestionnaire aux méthodes de l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup"><strong>IHomeGroup</strong></a><br/></td>
<td>Expose des méthodes qui déterminent l’état d’appartenance du groupe résidentiel d’un ordinateur et affichent l’Assistant partage.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a><br/></td>
<td>Appelée par l’exécution automatique pour implémenter la gestion des types de média inscrits.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler2"><strong>IHWEventHandler2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a> pour résoudre l’élévation du contrôle de compte utilisateur (UAC) pour les gestionnaires d’appareils.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname"><strong>IIdentityName</strong></a><br/></td>
<td>Expose des méthodes pour comparer deux éléments afin de déterminer s’ils sont identiques.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iimagerecompress"><strong>IImageRecompress</strong></a><br/></td>
<td>Expose une méthode qui recompresse les images.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a><br/></td>
<td>Expose une méthode unique utilisée pour initialiser des objets qui implémentent <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> ou <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> avec le nom de commande spécifié par l’application et ses propriétés inscrites.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl/nn-shobjidl-iinitializenetworkfolder"><strong>IInitializeNetworkFolder</strong></a><br/></td>
<td>Expose une méthode qui initialise la source de données réseau CLSID_NetworkPlaces comme spécifié.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithbindctx"><strong>IInitializeWithBindCtx</strong></a><br/></td>
<td>Expose une méthode qui initialise un gestionnaire, tel qu’un gestionnaire de propriétés, un gestionnaire de miniatures ou un gestionnaire d’aperçus, avec un contexte de liaison.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile"><strong>IInitializeWithFile</strong></a><br/></td>
<td>Expose une méthode pour initialiser un gestionnaire, tel qu’un gestionnaire de propriétés, un gestionnaire de miniatures ou un gestionnaire d’aperçus, avec un chemin d’accès de fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem"><strong>IInitializeWithItem</strong></a><br/></td>
<td>Expose une méthode utilisée pour initialiser un gestionnaire, tel qu’un gestionnaire de propriétés, un gestionnaire de miniatures ou un gestionnaire d’aperçus, avec un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore"><strong>IInitializeWithPropertyStore</strong></a><br/></td>
<td>Expose une méthode qui initialise un gestionnaire, tel qu’un gestionnaire de propriétés, un gestionnaire de miniatures ou un gestionnaire d’aperçus, avec une banque de propriétés.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a><br/></td>
<td>Expose une méthode qui initialise un gestionnaire, tel qu’un gestionnaire de propriétés, un gestionnaire de miniatures ou un gestionnaire d’aperçus, avec un flux.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow"><strong>IInitializeWithWindow</strong></a><br/></td>
<td>expose une méthode par le biais de laquelle un client peut fournir une fenêtre propriétaire à un objet Windows Runtime utilisé dans une application de bureau.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a><br/></td>
<td>Expose des méthodes qui modifient l’activation de l’interface utilisateur et traitent les accélérateurs pour un objet d’entrée utilisateur contenu dans le shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject2"><strong>IInputObject2</strong></a><br/></td>
<td>Expose une méthode qui étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a> en gérant des accélérateurs globaux.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite"><strong>IInputObjectSite</strong></a><br/></td>
<td>Expose une méthode qui est utilisée pour communiquer les modifications de focus pour un objet d’entrée utilisateur contenu dans le shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration"><strong>IInputPanelConfiguration</strong></a><br/></td>
<td>fournit des fonctionnalités pour que les applications de bureau choisissent le mécanisme de suivi de focus utilisé dans les applications Windows store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration"><strong>IInputPanelInvocationConfiguration</strong></a><br/></td>
<td>permet à Windows applications du windows Store de refuser le comportement d’appel automatique.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iiocancelinformation"><strong>IIOCancelInformation</strong></a><br/></td>
<td>Expose des méthodes pour publier un message de fenêtre d’annulation dans le thread de processus à partir de la boîte de dialogue de progression. <br/> Cette interface permet à la boîte de dialogue de progression de poster un message de thread via <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> vers le thread de travail pour annuler ses opérations. Le thread de travail doit vérifier périodiquement la file d’attente de messages via <a href="/windows/desktop/api/winuser/nf-winuser-getmessage"><strong>GetMessage</strong></a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea"><strong>PeekMessage</strong></a> ou <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex"><strong>MsgWaitForMultipleObjectsEx</strong></a>.<br/> La méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation"><strong>IIOCancelInformation :: SetCancelInformation</strong></a> indique à la boîte de dialogue de progression l’ID de thread et le message à <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> lorsque l’utilisateur clique sur <strong>Annuler</strong>. Un ID de thread de &quot; zéro &quot; désactive l’opération d’envoi pour le message d’annulation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits"><strong>IItemNameLimits</strong></a><br/></td>
<td>Récupère une liste de caractères valides et non valides ou la longueur maximale d’un nom dans l’espace de noms. Utilisez cette interface pour l’analyse et la traduction de la validation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder"><strong>IKnownFolder</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application de récupérer des informations sur la catégorie, le type, le GUID, la valeur PIDL, les fonctionnalités de redirection et la définition d’un dossier connu. Il fournit une méthode pour le designer de l’objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> d’un dossier connu. Il fournit également des méthodes pour récupérer ou définir le chemin d’accès au dossier connu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a><br/></td>
<td>Expose des méthodes qui créent, énumèrent ou gèrent des dossiers connus existants.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid"><strong>ILaunchSourceAppUserModelId</strong></a><br/></td>
<td>Fournit une méthode pour récupérer un <a href="appids.md">AppUserModelId</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference</strong></a><br/></td>
<td>Fournit des méthodes pour récupérer des informations sur l’application source.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor"><strong>ILaunchTargetMonitor</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference"><strong>ILaunchTargetViewSizePreference</strong></a><br/></td>
<td>Fournit une méthode pour récupérer la taille de vue par défaut d’une nouvelle fenêtre d’application.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/shell-extensibility-bumper"><strong>IMarkupCallback</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a> peut être modifié ou non disponible.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow"><strong>IModalWindow</strong></a><br/></td>
<td>Expose une méthode qui représente une fenêtre modale. cette interface est utilisée dans l’assistant Passport Windows XP.<br/></td>
</tr>
<tr class="odd">
<td><a href="imultimonitordockingsite.md"><strong>IMultiMonitorDockingSite</strong></a><br/></td>
<td>Implémenté par le navigateur. expose des méthodes qui gèrent le moniteur qui contient la barre des tâches Windows sur un système à plusieurs écrans. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-inamedpropertybag"><strong>INamedPropertyBag</strong></a><br/></td>
<td>Expose des méthodes qui fournissent un objet avec un conteneur de propriétés spécifié dans lequel l’objet peut enregistrer ses propriétés.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-inamedpropertystore"><strong>INamedPropertyStore</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent et définissent des propriétés nommées.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreeaccessible"><strong>INameSpaceTreeAccessible</strong></a><br/></td>
<td>Expose des méthodes qui effectuent des actions d’accessibilité sur un élément de Shell à partir d’un contrôle d’arborescence d’espace de noms.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a><br/></td>
<td>Expose les méthodes utilisées pour afficher et manipuler des nœuds dans une arborescence d’éléments de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> en fournissant des méthodes qui obtiennent et définissent les styles d’affichage des contrôles TreeView à utiliser avec les éléments d’espace de noms de l’interpréteur de commandes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a><br/></td>
<td>Expose des méthodes qui permettent à l’utilisateur de dessiner un contrôle d’arborescence d’espace de noms personnalisé et ses éléments.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontroldrophandler"><strong>INameSpaceTreeControlDropHandler</strong></a><br/></td>
<td>Expose des méthodes de gestionnaire pour le glisser-déplacer. Utilisé par le contrôle d’arborescence d’espace de noms pour notifier au client toute opération de glisser-déplacer survenant dans le contrôle. Permet à un client d’intercepter une opération de déplacement et d’exécuter sa propre action, ou de retourner l’effet de dépôt souhaité.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolevents"><strong>INameSpaceTreeControlEvents</strong></a><br/></td>
<td>Expose des méthodes pour gérer les événements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a><br/></td>
<td>Expose une méthode unique qui récupère l’état de la prise en charge du filtrage <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System. IsPinnedToNameSpaceTree</a> d’un dossier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a><br/></td>
<td>Expose des méthodes qui parcourent un espace de noms à partir d’un nœud racine donné. La profondeur du parcours est spécifiée et un tableau facultatif est retourné, contenant les ID de tous les nœuds parcourus.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a><br/></td>
<td>Interface de rappel exposant les méthodes utilisées avec <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a>. Après avoir effectué un parcours avec <strong>INamespaceWalk</strong>, un objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> représentant les nœuds parcouru est passé aux méthodes <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> . Ce que font ces méthodes avec les informations dépend de l’objet qui les implémente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb2"><strong>INamespaceWalkCB2</strong></a><br/></td>
<td>Étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> avec une méthode qui est requise pour effectuer un parcours d’espace de noms. Cette méthode supprime les données collectées pendant le parcours. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewmenuclient"><strong>INewMenuClient</strong></a><br/></td>
<td>expose des méthodes qui permettent de manipuler des éléments dans un menu Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka"><strong>INewShortcutHook</strong></a><br/></td>
<td>Expose des méthodes pour créer un nouveau raccourci Internet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager"><strong>INewWindowManager</strong></a><br/></td>
<td>Expose une méthode qui détermine si une fenêtre qui est lancée par une autre fenêtre doit être affichée ou bloquée, ce qui permet de contrôler les fenêtres indépendantes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica"><strong>INotifyReplica</strong></a><br/></td>
<td>Expose une méthode qui fournit le créateur d’un objet avec le moyen de notifier à l’objet qu’il peut être soumis à un rapprochement ultérieur. Le réconciliateur de porte-documents est responsable de l’implémentation de cette interface.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a><br/></td>
<td>Expose des méthodes qui permettent aux clients d’accéder aux éléments d’une collection d’objets qui prennent en charge <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection"><strong>IObjectCollection</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a> en fournissant des méthodes qui permettent aux clients d’ajouter et de supprimer des objets qui prennent en charge <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> dans une collection.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider"><strong>IObjectProvider</strong></a><br/></td>
<td>Expose une méthode pour découvrir des objets nommés avec un <strong>GUID</strong> à partir d’un autre objet. Contrairement à <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> , cette interface ne déléguera pas ses fonctionnalités à d’autres objets.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid"><strong>IObjectWithAppUserModelID</strong></a><br/></td>
<td>Expose des méthodes qui permettent aux implémenteurs d’un objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a> personnalisé de fournir l’accès à son ID de modèle d’utilisateur d’application explicite (AppUserModelID). Ces informations sont utilisées pour déterminer si un type de fichier particulier peut être ajouté à la liste de raccourcis d’une application.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithbackreferences"><strong>IObjectWithBackReferences</strong></a><br/></td>
<td>Fournit une méthode pour interagir avec les références Back détenues par un objet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent"><strong>IObjectWithCancelEvent</strong></a><br/></td>
<td>Fournit à un appelant un événement qui est signalé par l’objet appelé pour dénoter l’annulation d’une tâche.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent et définissent les modes d’énumération d’un élément analysé.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid"><strong>IObjectWithProgID</strong></a><br/></td>
<td>Expose des méthodes qui fournissent l’accès au ProgID associé à un objet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iobjectwithpropertykey"><strong>IObjectWithPropertyKey</strong></a><br/></td>
<td>Expose des méthodes pour obtenir et définir la clé de propriété.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent ou définissent des éléments sélectionnés représentés par un tableau d’éléments d’interpréteur de commandes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr"><strong>IObjMgr</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un client d’ajouter ou de supprimer un objet d’une collection d’objets gérés par un objet serveur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel"><strong>IOpenControlPanel</strong></a><br/></td>
<td>Expose des méthodes qui récupèrent l’état d’affichage du panneau de configuration, le chemin d’accès des éléments du panneau de configuration individuels et qui ouvrent le panneau de configuration lui-même ou un élément du panneau de configuration individuel.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource"><strong>IOpenSearchSource</strong></a><br/></td>
<td>expose une méthode pour obtenir les résultats de la recherche d’une source de données OpenSearch côté client personnalisée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog"><strong>IOperationsProgressDialog</strong></a><br/></td>
<td>Expose des méthodes permettant d’obtenir, de définir et d’interroger une boîte de dialogue de progression.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ipackagedebugsettings"><strong>IPackageDebugSettings</strong></a><br/></td>
<td>permet aux développeurs de débogueur de contrôler le cycle de vie d’une application Windows Store, comme la suspension ou la reprise.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification"><strong>IPackageExecutionStateChangeNotification</strong></a><br/></td>
<td>active la réception des notifications de modification de l’état du package pendant le débogage de l’application Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a><br/></td>
<td>Expose les méthodes qui obtiennent et définissent le parent et l’ID enfant du parent. Bien que <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> soit généralement implémenté sur IShellItems, il n’est pas spécifique à <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem"><strong>IParseAndCreateItem</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a><br/></td>
<td>Expose une méthode qui initialise des objets de dossier de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent des informations à partir d’objets de dossier shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3"><strong>IPersistFolder3</strong></a><br/></td>
<td>Étend les interfaces <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a> en permettant à un objet Folder d’implémenter une gestion par défaut des raccourcis de dossiers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist"><strong>IPersistIDList</strong></a><br/></td>
<td>Expose les méthodes utilisées pour rendre persistantes des listes d’identificateurs d’éléments.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage"><strong>IPersistSerializedPropStorage</strong></a><br/></td>
<td>Expose des méthodes pour rendre persistantes les données de stockage des propriétés sérialisées pour une utilisation ultérieure et pour restaurer les données persistantes dans une nouvelle instance du magasin de propriétés.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage2"><strong>IPersistSerializedPropStorage2</strong></a><br/></td>
<td>Expose des méthodes pour rendre persistantes les données de stockage des propriétés sérialisées pour une utilisation ultérieure et pour restaurer les données persistantes dans une nouvelle instance du magasin de propriétés.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh707033(v=vs.85)"><strong>IPlaybackManager</strong></a><br/></td>
<td>fournit des méthodes qui permettent aux applications multimédias de communiquer avec le gestionnaire de lecture Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh707034(v=vs.85)"><strong>IPlaybackManagerEvents</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler"><strong>IPreviewHandler</strong></a><br/></td>
<td>Expose des méthodes pour l’affichage des aperçus enrichis.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe"><strong>IPreviewHandlerFrame</strong></a><br/></td>
<td>Permet aux gestionnaires d’aperçus de passer des raccourcis clavier à l’hôte. Cette interface récupère une liste de raccourcis clavier et indique à l’hôte de gérer un raccourci clavier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals"><strong>IPreviewHandlerVisuals</strong></a><br/></td>
<td>Expose des méthodes pour appliquer des informations de couleur et de police à des gestionnaires d’aperçu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewitem"><strong>IPreviewItem</strong></a><br/></td>
<td>Identifie un élément qui sera affiché dans le volet de visualisation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipreviousversionsinfo"><strong>IPreviousVersionsInfo</strong></a><br/></td>
<td>expose une méthode qui recherche les versions antérieures des fichiers ou dossiers du serveur, stockées pour l’objectif de la réversion par la technologie des <em>clichés instantanés</em> fournie avec Windows server 2003.<br/></td>
</tr>
<tr class="odd">
<td><a href="iprivateidentitymanager.md"><strong>IPrivateIdentityManager</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="iprivateidentitymanager2.md"><strong>IPrivateIdentityManager2</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice"><strong>IProfferService</strong></a><br/></td>
<td>Expose un mécanisme général permettant aux objets d’offrir des services à d’autres objets sur le même hôte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog"><strong>IProgressDialog</strong></a><br/></td>
<td>Expose des méthodes qui fournissent des options pour qu’une application affiche une boîte de dialogue de progression. Cette interface est exportée par l’objet de boîte de dialogue de progression (CLSID_ProgressDialog). Cet objet est une méthode générique pour montrer à un utilisateur comment une opération progresse. Elle est généralement utilisée lors de la suppression, du chargement, de la copie, du déplacement ou du téléchargement d’un grand nombre de fichiers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a><br/></td>
<td>Expose des méthodes qui représentent des applications pour ajouter/supprimer des programmes dans le panneau de configuration. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp2"><strong>IPublishedApp2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a> en fournissant une méthode d’installation supplémentaire.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a><br/></td>
<td>Expose des méthodes pour travailler avec l’Assistant impression en ligne, l’Assistant Publication Web et l’Assistant Ajouter un favori réseau. dans Windows Vista, <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a> ne prend plus en charge l’assistant publication de sites Web ou l’assistant impression en ligne.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a><br/></td>
<td>Expose des méthodes qui simplifient le processus de récupération des informations stockées dans le registre en association avec la définition d’un type de fichier ou d’un protocole et son association à une application.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>IQueryCancelAutoPlay</strong></a><br/></td>
<td>Expose une méthode qui remplace par programmation la <a href="autorun2k-intro.md">lecture automatique</a> ou l' <a href="autoplay.md">exécution automatique</a>. Cela vous permet de personnaliser l’emplacement et le type de contenu qui est lancé lorsque le média est inséré.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycodepage"><strong>IQueryCodePage</strong></a><br/></td>
<td>Obtient et définit la valeur numérique (identificateur de page de codes) de la page de codes ANSI.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a><br/></td>
<td>Expose une méthode qui fournit un mécanisme standard simple pour que les objets interrogent un client pour obtenir l’autorisation de poursuivre une opération. Les clients de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>, par exemple, doivent passer une implémentation de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a> à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show"><strong>IUserNotification :: Show</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iquerycontinuewithstatus"><strong>IQueryContinueWithStatus</strong></a><br/></td>
<td>Expose des méthodes qui fournissent un mécanisme standard pour les fournisseurs d’informations d’identification afin d’appeler <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue"><strong>QueryContinue</strong></a> lors d’une tentative de connexion au réseau pour déterminer s’ils doivent continuer à effectuer ces tentatives. Les fournisseurs d’informations d’identification peuvent également utiliser cette interface pour afficher des messages à l’utilisateur lors de la tentative d’établissement d’une connexion réseau.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo"><strong>IQueryInfo</strong></a><br/></td>
<td>Expose les méthodes que l’interpréteur de commandes utilise pour récupérer des indicateurs et des informations d’info-bulle pour un élément qui réside dans une implémentation de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . Les info-bulles sont généralement affichées à l’intérieur d’un contrôle <a href="/windows/desktop/Controls/tooltip-controls">ToolTip</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem"><strong>IRelatedItem</strong></a><br/></td>
<td>Expose des méthodes qui dérivent des éléments connexes avec des relations spécifiques.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer"><strong>IRemoteComputer</strong></a><br/></td>
<td>Expose une méthode qui énumère ou Initialise une extension d’espace de noms lorsqu’elle est appelée sur un objet distant. Cette interface est utilisée, par exemple, pour initialiser le dossier virtuel des imprimantes distantes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink"><strong>IResolveShellLink</strong></a><br/></td>
<td>Expose une méthode qui permet à une application de demander à un objet de dossier de Shell de résoudre un lien pour l’un de ses éléments.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a><br/></td>
<td>Expose des méthodes qui contiennent des éléments d’un objet de données.<br/> Un <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a> est un dossier qui peut contenir des éléments de tout sur l’espace de noms et les représenter à l’utilisateur dans un dossier unique.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask"><strong>IRunnableTask</strong></a><br/></td>
<td>Interface à thread libre qui peut être exposée par un objet pour permettre l’exécution d’opérations sur un thread d’arrière-plan. Par exemple, si la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation"><strong>IExtractImage :: GetLocation</strong></a> retourne E_PENDING, l’application appelante est autorisée à extraire l’image sur un thread d’arrière-plan.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-isearchboxinfo"><strong>ISearchBoxInfo</strong></a><br/></td>
<td>Expose des méthodes qui permettent à l’appelant de récupérer les informations entrées dans une zone de recherche.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext"><strong>ISearchContext</strong></a><br/></td>
<td>Expose des méthodes qui associent des informations de personnalisation aux raccordements de recherche.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory"><strong>ISearchFolderItemFactory</strong></a><br/></td>
<td>Expose des méthodes qui créent et modifient des dossiers de recherche. Les méthodes Set sont appelées en premier pour configurer les paramètres de la recherche. Lorsqu’il n’est pas appelé, les valeurs par défaut sont utilisées à la place. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist"><strong>ISearchFolderItemFactory :: GetIDList</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem"><strong>ISearchFolderItemFactory :: GetShellItem</strong></a> retournent les deux formes de la recherche spécifiée par ces paramètres. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-isharedbitmap"><strong>ISharedBitmap</strong></a><br/></td>
<td>Expose des méthodes économes en mémoire pour l’accès aux bitmaps. Cette interface est utilisée comme un wrapper léger autour des objets HBITMAP, ce qui permet à ces objets d’être décomptés et protégés de la modification de leurs données sous-jacentes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a><br/></td>
<td>Expose des méthodes qui définissent et récupèrent des informations sur les paramètres de partage par défaut d’un ordinateur pour le dossier <strong>Users</strong> ( <code>C:\Users</code> ) ou <strong>public</strong> ( <code>C:\Users\Public</code> ). Expose également un ensemble de méthodes qui permettent le contrôle du partage d’imprimantes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ishellapp"><strong>IShellApp</strong></a><br/></td>
<td>Expose des méthodes qui fournissent des informations générales sur une application à l’application Ajout/suppression de programmes. Vous ne pouvez pas l’utiliser en dehors de l’application Ajout/suppression de programmes. Les informations fournies par cette interface incluent une liste des actions de gestion prises en charge et indiquent si l’application est actuellement installée. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a><br/></td>
<td>Implémenté par des hôtes d’affichages de Shell (objets qui implémentent <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>). Expose des méthodes qui fournissent des services pour la vue qu’elle héberge et d’autres objets qui s’exécutent dans le contexte de la fenêtre de l’Explorateur. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellchangenotify"><strong>IShellChangeNotify</strong></a><br/></td>
<td>Expose une méthode qui notifie une extension d’espace de noms de Shell lorsque l’ID d’un élément a changé.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a><br/></td>
<td>Exposé par les dossiers Shell pour fournir des informations détaillées sur les éléments d’un dossier. il s’agit des mêmes informations que celles affichées par l’explorateur de Windows lorsque la vue du dossier est définie sur détails. pour les systèmes Windows 2000 et versions ultérieures, <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a> est remplacé par <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit"><strong>IShellExtInit</strong></a><br/></td>
<td>Expose une méthode qui initialise des extensions de Shell pour les feuilles de propriétés, les menus contextuels et les gestionnaires de glisser-déplacer (extensions qui ajoutent des éléments à des menus contextuels pendant des opérations de glisser-déplacer non par défaut).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a><br/></td>
<td>Exposée par tous les objets de dossier de l’espace de noms Shell, ses méthodes sont utilisées pour gérer des dossiers.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a><br/></td>
<td>Étend les fonctionnalités de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>. Ses méthodes fournissent diverses informations sur le contenu d’un dossier de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfoldersearchable.md"><strong>IShellFolderSearchable</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une extension de Shell de fournir un espace de noms pouvant faire l’objet d’une recherche.<br/></td>
</tr>
<tr class="even">
<td><a href="ishellfoldersearchablecallback.md"><strong>IShellFolderSearchableCallback</strong></a><br/></td>
<td>Expose des routines de rappel pour surveiller le processus de recherche.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>IShellFolderViewCB</strong></a><br/></td>
<td>expose une méthode qui permet la communication entre l’explorateur de Windows et une vue de dossier implémentée à l’aide de l’objet de vue de dossier système (objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> retourné via <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a>) afin que l’affichage des dossiers puisse être averti des événements et modifier sa vue en conséquence.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual"><strong>IShellFolderViewDual</strong></a><br/></td>
<td>Expose des méthodes qui modifient la vue et sélectionnent les éléments dans le dossier actif. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual2"><strong>IShellFolderViewDual2</strong></a><br/></td>
<td>Expose des méthodes qui modifient la vue et sélectionnent les éléments dans le dossier actif.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual3"><strong>IShellFolderViewDual3</strong></a><br/></td>
<td>Expose des méthodes qui modifient l’affichage des dossiers en cours.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfolderviewtype.md"><strong>IShellFolderViewType</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un dossier de Shell de prendre en charge différentes vues sur son contenu (différentes dispositions hiérarchiques de ses données).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellicon"><strong>IShellIcon</strong></a><br/></td>
<td>Expose une méthode qui obtient un index d’icône pour un objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay"><strong>IShellIconOverlay</strong></a><br/></td>
<td>Expose les méthodes utilisées par une extension d’espace de noms pour spécifier des superpositions d’icône pour les objets qu’elle contient.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier"><strong>IShellIconOverlayIdentifier</strong></a><br/></td>
<td>Expose des méthodes qui gèrent toutes les communications entre les gestionnaires de superposition d’icône et l’interpréteur de commandes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedataabort"><strong>IShellImageDataAbort</strong></a><br/></td>
<td>Expose une méthode unique utilisée pour abandonner les processus <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedatafactory"><strong>IShellImageDataFactory</strong></a><br/></td>
<td>Expose des méthodes qui créent des instances <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> basées sur diverses sources d’image.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a><br/></td>
<td>Expose des méthodes qui récupèrent des informations sur un élément de Shell. <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> sont les représentations préférées des éléments dans tout nouveau code.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a><br/></td>
<td>Étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> avec des méthodes qui récupèrent différentes valeurs de propriété de l’élément. <strong>IShellItem</strong> et <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> sont les représentations préférées des éléments dans tout nouveau code.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray"><strong>IShellItemArray</strong></a><br/></td>
<td>Expose des méthodes qui créent et manipulent des tableaux d' <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>éléments d’interpréteur</strong></a> de commandes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter"><strong>IShellItemFilter</strong></a><br/></td>
<td>Exposé par un client pour spécifier comment filtrer l’énumération d’un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>élément de Shell</strong></a> par une application serveur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory"><strong>IShellItemImageFactory</strong></a><br/></td>
<td>Expose une méthode pour retourner des icônes ou des miniatures pour les éléments de Shell. Si aucune miniature ou icône n’est disponible pour l’élément demandé, une icône par classe peut être fournie à partir de l’interpréteur de commandes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources"><strong>IShellItemResources</strong></a><br/></td>
<td>Expose des méthodes pour manipuler et interroger des ressources d’élément d’environnement.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary"><strong>IShellLibrary</strong></a><br/></td>
<td>Expose des méthodes pour créer et gérer des bibliothèques.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a><br/></td>
<td>Expose des méthodes qui créent, modifient et résolvent des liens de Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application d’attacher des blocs de données supplémentaires à un <a href="/windows/desktop/shell/links">lien de Shell</a>. Ces méthodes ajoutent, copient ou suppriment des blocs de données.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a><br/></td>
<td>Expose des méthodes qui interagissent avec les menus de l’interpréteur de commandes tels que le menu <strong>Démarrer</strong> et le menu <strong>favoris</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback"><strong>IShellMenuCallback</strong></a><br/></td>
<td>Interface de rappel qui expose une méthode qui reçoit des messages d’une bande de menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext"><strong>IShellPropSheetExt</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un gestionnaire de feuilles de propriétés d’ajouter ou de remplacer des pages dans la feuille de propriétés affichée pour un objet fichier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ishellrundll"><strong>IShellRunDll</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a><br/></td>
<td>expose des méthodes qui présentent une vue dans les fenêtres de Windows ou de l’explorateur de dossiers.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a><br/></td>
<td>Étend les fonctionnalités de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ishellview3"><strong>IShellView3</strong></a><br/></td>
<td>Étend les fonctionnalités de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> en fournissant une méthode pour remplacer <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2 :: CreateViewWindow2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a><br/></td>
<td>Permet d’accéder à la collection de fenêtres d’interpréteur de commandes ouvertes.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istartmenupinnedlist"><strong>IStartMenuPinnedList</strong></a><br/></td>
<td>Expose une méthode qui désépingle un raccourci de l’application à partir du menu <strong>Démarrer</strong> ou de la barre des tâches.<br/></td>
</tr>
<tr class="odd">
<td><a href="nn-shobjidl-istorageprovidercopyhook.md"><strong>IStorageProviderCopyHook</strong></a><br/></td>
<td>Expose une méthode qui détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler"><strong>IStorageProviderHandler</strong></a><br/></td>
<td>Récupère le <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a> associé à un fichier ou un dossier spécifique.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a><br/></td>
<td>Fournit une collection de propriétés associées à un fichier ou à un dossier.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamasync"><strong>IStreamAsync</strong></a><br/></td>
<td>Expose des méthodes pour gérer les entrées/emplacement (e/s) dans un flux asynchrone. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamunbufferedinfo"><strong>IStreamUnbufferedInfo</strong></a><br/></td>
<td>Expose une méthode qui détermine la taille du secteur comme une aide pour l’alignement des octets.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager"><strong>ISuspensionDependencyManager</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflict"><strong>ISyncMgrConflict</strong></a><br/></td>
<td>Expose des méthodes qui fournissent des informations sur un conflit récupéré à partir d’un magasin de conflits et permet de résoudre le conflit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a><br/></td>
<td>Expose une méthode qui obtient la liste d’ID de conflit pour un objet de conflit.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictitems"><strong>ISyncMgrConflictItems</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent les données d’élément de conflit et le nombre d’éléments.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a><br/></td>
<td>Expose une méthode qui présente un conflit à l’utilisateur.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems"><strong>ISyncMgrConflictResolutionItems</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent des informations sur les éléments et le nombre d’éléments.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo"><strong>ISyncMgrConflictResolveInfo</strong></a><br/></td>
<td>Expose des méthodes qui obtiennent et définissent des informations sur la résolution des conflits du gestionnaire de synchronisation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictstore"><strong>ISyncMgrConflictStore</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un gestionnaire de fournir des conflits qui apparaissent dans le dossier conflits.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application ou un gestionnaire de démarrer ou d’arrêter une synchronisation, de notifier le centre de synchronisation des modifications à l’ensemble de gestionnaires ou d’éléments, ou de notifier les modifications apportées aux valeurs de propriété.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a><br/></td>
<td>Expose des méthodes qui énumèrent un tableau de structures <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> . Chacune de ces structures fournit des informations sur un élément qui peut être synchronisé. <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> a les mêmes méthodes que toutes les interfaces d’énumérateur standard : Next, Skip, Reset et clone.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrevent"><strong>ISyncMgrEvent</strong></a><br/></td>
<td>Expose des méthodes qui récupèrent des données à partir d’un magasin d’événements. Un magasin d’événements permet au centre de synchronisation d’obtenir un énumérateur de tous les événements dans le magasin, ainsi que de récupérer des événements individuels.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventlinkuioperation"><strong>ISyncMgrEventLinkUIOperation</strong></a><br/></td>
<td>Fournit une méthode qui est appelée lorsque l’utilisateur clique sur les liens d’événements dans le dossier des résultats de synchronisation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventstore"><strong>ISyncMgrEventStore</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un gestionnaire de fournir son propre magasin d’événements et de gérer ses propres événements de synchronisation, au lieu d’utiliser le magasin d’événements du centre de synchronisation par défaut. Ces événements sont affichés dans le dossier de résultats de la synchronisation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler"><strong>ISyncMgrHandler</strong></a><br/></td>
<td>Expose des méthodes qui composent l’interface principale implémentée par un gestionnaire de synchronisation. Le centre de synchronisation crée une instance du gestionnaire via cette interface pour récupérer des propriétés, énumérer les éléments de synchronisation et modifier l’État. Le centre de synchronisation crée une instance distincte du gestionnaire sur un thread distinct pour effectuer une opération de synchronisation ou d’interface utilisateur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlercollection"><strong>ISyncMgrHandlerCollection</strong></a><br/></td>
<td>Expose des méthodes qui fournissent un énumérateur des ID de gestionnaire de synchronisation et instancient ces gestionnaires de synchronisation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo"><strong>ISyncMgrHandlerInfo</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un gestionnaire de fournir des informations de propriété et d’État au centre de synchronisation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a><br/></td>
<td>Expose des méthodes pour qu’une application puisse s’inscrire auprès du gestionnaire de synchronisation. Vous pouvez le faire par le biais de l’interface <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> ou en vous inscrivant directement dans le registre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a><br/></td>
<td>Expose des méthodes qui gèrent les conflits de synchronisation. Implémentez cette interface pour construire un gestionnaire de conflits de synchronisation. L’interface utilisateur de résolution des conflits appellera cette interface pour résoudre le conflit présenté à l’utilisateur. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation"><strong>ISyncMgrScheduleWizardUIOperation</strong></a><br/></td>
<td>Expose une méthode qui permet à un gestionnaire d’afficher l’Assistant Planification de la synchronisation pour le gestionnaire.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsessioncreator"><strong>ISyncMgrSessionCreator</strong></a><br/></td>
<td>Expose une méthode unique par le biais de laquelle un gestionnaire ou une application externe peut notifier le centre de synchronisation que la synchronisation a commencé, ainsi que signaler la progression et les événements.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynccallback"><strong>ISyncMgrSyncCallback</strong></a><br/></td>
<td>Expose des méthodes qui permettent à un processus de synchronisation de signaler la progression et les événements au centre de synchronisation, ou d’interroger si le processus a été annulé.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize"><strong>ISyncMgrSynchronize</strong></a><br/></td>
<td>Expose des méthodes qui permettent à l’application ou au service inscrit de recevoir des notifications du gestionnaire de synchronisation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback"><strong>ISyncMgrSynchronizeCallback</strong></a><br/></td>
<td>Expose des méthodes qui gèrent le processus de synchronisation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke"><strong>ISyncMgrSynchronizeInvoke</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application inscrite d’appeler le gestionnaire de synchronisation pour mettre à jour des éléments.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem"><strong>ISyncMgrSyncItem</strong></a><br/></td>
<td>Expose des méthodes qui agissent sur et récupèrent des informations à partir d’un seul élément de synchronisation, ce qui permet aux gestionnaires de gérer des éléments de synchronisation en tant qu’objets indépendants.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer"><strong>ISyncMgrSyncItemContainer</strong></a><br/></td>
<td>Expose des méthodes qui fournissent des informations aux gestionnaires sur les éléments qu’ils contiennent.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo"><strong>ISyncMgrSyncItemInfo</strong></a><br/></td>
<td>Expose des méthodes qui fournissent des informations de propriété et d’État pour un élément de synchronisation unique.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncresult"><strong>ISyncMgrSyncResult</strong></a><br/></td>
<td>Expose une méthode que les applications qui appellent <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> peuvent utiliser pour obtenir le résultat d’un appel <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl :: StartHandlerSync</strong></a> ou <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl :: StartItemSync</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgruioperation"><strong>ISyncMgrUIOperation</strong></a><br/></td>
<td>Expose une méthode par le biais de laquelle un gestionnaire de synchronisation ou un élément de synchronisation peut afficher un objet d’interface utilisateur lorsqu’il y est invité par le centre de synchronisation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a><br/></td>
<td>Expose des méthodes qui contrôlent la barre des tâches. Elle vous permet d’ajouter, de supprimer et d’activer dynamiquement des éléments dans la barre des tâches.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a> en exposant une méthode pour marquer une fenêtre en tant qu’affichage plein écran.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a><br/></td>
<td>étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a> en exposant des méthodes qui prennent en charge la fonctionnalité de bouton de lancement et de basculement unifiée de la barre des tâches ajoutée dans Windows 7. Cette fonctionnalité comprend des représentations de miniatures et des cibles de commutateur basées sur des onglets individuels dans une application avec onglets, des barres d’outils miniatures, des superpositions de notifications et d’États et des indicateurs de progression.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4"><strong>ITaskbarList4</strong></a><br/></td>
<td>Étend <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> en fournissant une méthode qui permet à l’appelant de contrôler deux valeurs de propriété pour la miniature d’onglet et la fonctionnalité d’aperçu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailcache"><strong>IThumbnailCache</strong></a><br/></td>
<td>Expose des méthodes pour un cache de miniatures système partagé entre les applications.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcacheprimer"><strong>IThumbnailCachePrimer</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ithumbnailhandlerfactory"><strong>IThumbnailHandlerFactory</strong></a><br/></td>
<td>Expose une méthode pour récupérer le gestionnaire de miniatures d’un élément. Implémentez cette interface si vous souhaitez spécifier l’extracteur utilisé pour un IDList enfant.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider"><strong>IThumbnailProvider</strong></a><br/></td>
<td>Expose une méthode pour obtenir une image miniature et est destinée à être implémentée pour les gestionnaires de miniatures. L’objet qui implémente cette interface doit également implémenter <a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailsettings"><strong>IThumbnailSettings</strong></a><br/></td>
<td>Fournit une méthode qui permet à un fournisseur de miniatures de déterminer le contexte utilisateur d’une demande de miniature.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a><br/></td>
<td>Obtient ou définit le flux de miniatures. Cette interface est destinée à un usage interne uniquement et ne peut être appelée que par l’application photos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itrackshellmenu"><strong>ITrackShellMenu</strong></a><br/></td>
<td>Expose des méthodes qui étendent l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a> en offrant la possibilité de coordonner les boutons de la barre d’outils avec un menu et d’afficher un menu contextuel.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Imagetranscode/nn-imagetranscode-itranscodeimage"><strong>ITranscodeImage</strong></a><br/></td>
<td>Expose une méthode qui permet de convertir des formats d’image JPEG ou bitmap (BMP) à partir de n’importe quel type d’image pris en charge par Windows. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink"><strong>ITransferAdviseSink</strong></a><br/></td>
<td>Expose les méthodes qui prennent en charge la collecte d’État et les informations d’échec.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a><br/></td>
<td>Expose des méthodes qui créent un élément de Shell de destination pour une opération de copie ou de déplacement. Cette interface est fournie pour permettre davantage de contrôle sur les opérations de fichier en fournissant une méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise"><strong>ITransferDestination :: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem"><strong>ITransferMediumItem</strong></a><br/></td>
<td>Utilisé par un moteur de copie pour obtenir l’élément sur lequel appeler <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> pour retourner un pointeur vers l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> ou l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a>. Ces interfaces peuvent être interrogées et énumérées pour les opérations de copie, de déplacement ou de suppression.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a><br/></td>
<td>Expose des méthodes pour manipuler des <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, y compris la copie, le déplacement, le recyclage et d’autres. Cette interface est proposée pour fournir davantage de contrôle sur les opérations de fichier en fournissant une méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise"><strong>ITransferSource :: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-itraydeskband"><strong>ITrayDeskBand</strong></a><br/></td>
<td>Expose des méthodes qui affichent, masquent et interrogent des deskbands.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist"><strong>IUpdateIDList</strong></a><br/></td>
<td>Fournit une méthode pour mettre à jour le <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> de l’enfant d’un objet Folder.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook"><strong>IURLSearchHook</strong></a><br/></td>
<td>Expose une méthode utilisée par le navigateur pour traduire l’adresse d’un protocole d’URL inconnu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook2"><strong>IURLSearchHook2</strong></a><br/></td>
<td>Expose une méthode utilisée par le navigateur pour traduire l’adresse d’un protocole d’URL inconnu à l’aide d’un objet de contexte de recherche.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iuseraccountchangecallback"><strong>IUserAccountChangeCallback</strong></a><br/></td>
<td>Expose une méthode qui est appelée lorsque l’image qui représente un compte d’utilisateur est modifiée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a><br/></td>
<td>Expose des méthodes qui définissent des informations de notification, puis affichent cette notification à l’utilisateur dans une bulle qui s’affiche conjointement avec la zone de notification de la barre des tâches. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> diffère de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a> uniquement dans sa méthode <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> , qui ajoute un paramètre supplémentaire pour une interface de rappel pour communiquer avec la notification. Dans le cas contraire, les deux interfaces sont identiques au format et à la fonction. CLSID_UserNotification implémente les deux versions de <strong>Show</strong> comme une surcharge.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a><br/></td>
<td>Expose des méthodes qui définissent des informations de notification, puis affichent cette notification à l’utilisateur dans une bulle qui s’affiche conjointement avec la zone de notification de la barre des tâches. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> n’hérite pas de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>. <strong>IUserNotification2</strong> diffère de <strong>IUserNotification</strong> uniquement dans sa méthode <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>Show</strong></a> , qui ajoute un paramètre supplémentaire pour une interface de rappel pour communiquer avec la notification. Dans le cas contraire, les deux interfaces sont identiques au format et à la fonction. CLSID_UserNotification implémente les deux versions de <strong>Show</strong> comme une surcharge.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotificationcallback"><strong>IUserNotificationCallback</strong></a><br/></td>
<td>Expose une méthode pour la gestion d’un clic de souris ou d’un menu contextuel accessible dans une bulle de notification. Utilisé avec <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>IUserNotification2 :: Show</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusetobrowseitem"><strong>IUseToBrowseItem</strong></a><br/></td>
<td>Recherche l’élément qui doit être utilisé lors de l’exploration de cet élément.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iviewstateidentityitem"><strong>IViewStateIdentityItem</strong></a><br/></td>
<td>Fournit un élément de persistance canonique, un élément pour lequel les personnalisations d’affichage seront mémorisées.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager"><strong>IVirtualDesktopManager</strong></a><br/></td>
<td>Expose des méthodes qui permettent à une application d’interagir avec des groupes de fenêtres qui forment des espaces de travail virtuels.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a><br/></td>
<td>Expose des méthodes qui définissent et obtiennent des propriétés visuelles.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwebwizardextension"><strong>IWebWizardExtension</strong></a><br/></td>
<td>Étend l’interface <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a> en exposant des méthodes pour définir l’URL initiale de l’extension de l’Assistant et une URL spécifique en cas d’erreur.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a><br/></td>
<td>Utilisé par les assistants, tels que l’Assistant Publication de sites Web et l’Assistant commande d’impression en ligne, qui hébergent des pages de contenu côté serveur. Cette interface expose des méthodes pour spécifier des pages d’extension prises en charge et pour naviguer vers et à partir de ces pages.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardsite"><strong>IWizardSite</strong></a><br/></td>
<td>Expose les méthodes utilisées par une extension d’Assistant pour parcourir les bordures entre elles et le reste de l’Assistant.<br/></td>
</tr>
<tr class="odd">
<td><a href="taskcompletionclient.md"><strong>TaskCompletionClient</strong></a><br/></td>
<td>Active l’achèvement des tâches. <br/></td>
</tr>
</tbody>
</table>



 

 

 
---
description: 'Ensemble de clés de chaîne utilisées avec la méthode IBindCtx :: RegisterObjectParam pour spécifier un contexte de liaison.'
title: Clés de chaîne de contexte de liaison (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78743f18f9dc10b9c20b7e911224f1cd4e53e3f536f23686936a8f021605bf9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452046"
---
# <a name="bind-context-string-keys"></a>Clés de chaîne de contexte de liaison

Ensemble de clés de chaîne utilisées avec la méthode [**IBindCtx :: RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) pour spécifier un contexte de liaison.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP SP2</strong>. Spécifiez ce contexte de liaison pour permettre aux clients de la source de données de remplacer la stratégie de lettre de lecteur masquée et d’activer l’accès aux objets de vue pour les sources de données sur les lecteurs qui sont bloqués.<br/> Utilisé avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem :: BindToHandler</strong></a>.<br/> le système prend en charge les stratégies contrôlées par l’administrateur qui masquent les lettres de lecteur spécifiées pour empêcher les utilisateurs d’accéder à ces lecteurs par le biais de l’explorateur de Windows. Lorsque cette stratégie est active, le résultat est que les objets de vue et les autres gestionnaires créés avec la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder :: CreateViewObject</strong></a> échouent lorsqu’ils sont appelés sur des lecteurs qui sont bloqués par la stratégie.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour que la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> utilise l’objet spécifié par le paramètre <em>PBC</em> pour créer l’objet cible. dans ce cas, l’objet spécifié par le paramètre <em>punk</em> dans l’appel <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx :: RegisterObjectParam</strong></a> doit implémenter l’interface <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a> . <br/> Utilisé avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem :: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows 7</strong>. Passé à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> avec une valeur <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> pour contrôler le mode d’énumération de l’élément analysé. La valeur <strong>FOLDER_ENUM_MODE</strong> est passée dans le contexte de liaison via un objet qui implémente <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a>. <br/> Les éléments avec différents modes d’énumération sont comparés de façon canonique (SHCIDS_CANONICALONLY) différemment, car ils énumèrent différents ensembles d’éléments.<br/> Si un élément ne prend pas en charge le mode d’énumération (parce qu’il ne s’agit pas d’un dossier ou qu’il ne fournit pas le mode d’énumération), il est créé en mode d’énumération par défaut.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows 7</strong>. Passé à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> , ainsi que <strong>STR_FILE_SYS_BIND_DATA</strong>. Cela permet d’effectuer une analyse simple tout en recherchant des fichiers Desktop.inis sur le chemin d’accès à partir duquel obtenir une chaîne de nom localisée. Cela évite la détection de dossiers sur le chemin d’accès, qui, dans le cas d’un dossier qui représente un serveur ou un partage, peut prendre beaucoup de temps et de ressources. Les fichiers de Desktop.ini sont mis en cache dans certains emplacements. il est donc au moins aussi efficace que la détection des attributs de dossiers, puis la détection du Desktop.ini si ce dossier doit transformer l’unité d’organisation en lecture seule.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP SP2</strong>. Spécifiez ce contexte de liaison pour forcer un raccourci de dossier à résoudre le lien qui pointe vers sa cible. <br/> Un raccourci de dossier est un élément de dossier qui pointe vers un autre élément de dossier dans le même espace de noms, à l’aide d’un lien (raccourci) qui contiendra le IDList de la cible. Le lien est résolu pour effectuer le suivi de la cible au cas où elle serait déplacée ou renommée. par exemple, le dossier favoris <strong>réseau</strong> Windows XP et le dossier <strong>ordinateur</strong> Windows Vista peuvent contenir des raccourcis de dossiers créés à l’aide de l’assistant ajout d’un <strong>emplacement réseau</strong> . Pour améliorer les performances, la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> ne résout pas les liens vers un dossier réseau par défaut.<br/> Utilisé avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem :: BindToHandler</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP</strong>. Spécifiez ce contexte de liaison pour empêcher un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> sur le dossier <strong>Desktop</strong> de traiter les chemins d’accès relatifs par rapport au bureau. dans ce cas, l’analyse échoue lorsque ce contexte de liaison est spécifié.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour indiquer à un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> de ne pas résoudre la cible de lien obtenue lors de l’utilisation du GUID <strong>BHID_LinkTargetItem</strong> dans <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem :: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP</strong>. Spécifiez ce contexte de liaison pour fournir des métadonnées de fichier à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> , qui est utilisée au lieu de tenter de récupérer les métadonnées de fichier réelles. L’objet associé doit implémenter <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a> et peut éventuellement implémenter <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a>. Par défaut, la méthode <strong>IShellFolder ::P arsedisplayname</strong> vérifie que le fichier existe et utilise les métadonnées réelles du fichier pour remplir la liste d’ID.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduite dans Windows 8.1</strong>. spécifiez ce contexte de liaison pour indiquer que les données fournies dans le contexte de liaison <strong>STR_FILE_SYS_FIND_DATA</strong> doivent être utilisées pour créer une liste ItemID au format Windows 7.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows 7</strong>. Spécifiez ce contexte de liaison lorsque le gestionnaire est récupéré sur le même thread que l’interface utilisateur. Toutes les activités gourmandes en mémoire, telles que celles qui impliquent l’accès au disque ou au réseau, doivent être évitées.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison lors de la demande d’un gestionnaire <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Cette valeur est utilisée avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a>. Pour plus d’informations, consultez l’indicateur <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison lors de la demande d’un gestionnaire <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Cette valeur est utilisée avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a>. Pour plus d’informations, consultez l’indicateur <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison lors de la demande d’un gestionnaire <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Cette valeur est utilisée avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a>. Pour plus d’informations, consultez l’indicateur <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison lors de la demande d’un gestionnaire <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Cette valeur est utilisée avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a>. Pour plus d’informations, consultez l’indicateur <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows 7</strong>. Spécifiez ce contexte de liaison lors de la demande d’un gestionnaire <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Cette valeur est utilisée avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a>. Pour plus d’informations, consultez l’indicateur <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison lors de la demande d’un gestionnaire <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> ou <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Cette valeur est utilisée avec <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a>. Pour plus d’informations, consultez l’indicateur <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Vista uniquement.</strong> Spécifiez ce contexte de liaison pour déclencher un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> qui demande à l’interface <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> d’un objet de système de fichiers de retourner un filtre de texte si aucun autre filtre n’est disponible. cette valeur n’est pas définie à partir de Windows 7.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Vista uniquement.</strong> Spécifiez ce contexte de liaison pour déclencher un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> qui demande à l’interface <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> d’un objet de système de fichiers de ne pas retourner de filtre de secours si aucun filtre inscrit n’a été trouvé.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour activer le chargement de l’historique à partir d’un flux pour une navigation interne lorsque la méthode <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory :: LoadHistory</strong></a> est appelée. Une navigation interne est une navigation dans la même vue.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows 7</strong>. Spécifiez ce contexte de liaison avec STR_PARSE_PREFER_FOLDER_BROWSING lorsque le client souhaite que les gestionnaires de dossiers Internet Shell génèrent un IDList pour n’importe quelle URL valide si un dossier de type DAV ne peut pas être créé pour cette URL. L’URL n’est pas vérifiée pour exister. seule sa syntaxe est vérifiée et possède un gestionnaire de protocole inscrit.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows 7</strong>. Spécifiez ce contexte de liaison pour indiquer aux implémentations de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3 :: InitializeEx</strong></a> de mettre en cache les objets d’assistance nécessitant beaucoup de mémoire qui peuvent exister entre les instanciations d’éléments de Shell au lieu de recréer ces objets chaque fois qu’un élément de Shell est créé. L’objet associé est un autre objet de contexte de liaison, initialement vide. Cela doit aboutir à un objet de contexte de liaison distinct, accessible via <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx :: GetObjectParam</strong></a> ou <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx :: Register. ObjectParam</strong></a>. <br/> Un appelant doit accepter ce comportement en fournissant ce paramètre de contexte de liaison lors de l’appel de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. En procédant ainsi, vous optimisez le comportement de liaison à plusieurs noms d’analyse successifs. La durée de vie de l’objet de contexte de liaison doit s’étendre sur plusieurs instances d’éléments de Shell et leurs contextes de liaison individuels.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour autoriser l’affichage des caractères de nom de fichier non valides dans les noms de fichiers. Par défaut, un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> rejette les caractères non conformes dans les noms de fichiers. Ce contexte de liaison est significatif uniquement en association avec le contexte de liaison STR_FILE_SYS_FIND_DATA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour activer un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> sur le dossier <strong>Desktop</strong> pour analyser des URL. Si ce contexte de liaison est spécifié, il remplace <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows 7</strong>. Spécifiez ce contexte de liaison pour indiquer à l’implémentation d’une source de données <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> pour optimiser le comportement de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. <br/> Normalement, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a> effectue deux opérations de liaison sur le nom à analyser : une par une et une à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> et une pour créer l’élément de Shell. Lorsque le contexte de liaison <strong>STR_PARSE_AND_CREATE_ITEM</strong> est pris en charge, la deuxième liaison est évitée en créant l’élément de Shell pendant le <strong>IShellFolder ::P arsedisplayname</strong> la liaison et le stockage de l’élément de Shell par le biais de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem :: SetItem</strong></a>. <strong>SHCreateItemFromParsingName</strong> utilise ensuite l’élément de Shell stocké au lieu d’en créer un.<br/> Ce paramètre s’applique au dernier élément du nom analysé. Par exemple, dans le nom &quot;C:\Folder1\File.txt, les données s’appliquent à File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Vista uniquement.</strong> Spécifie que, lors de l’analyse d’une URL, ce contexte de liaison ne doit pas exiger que l’URL existe avant de générer un IDList pour celle-ci. Spécifiez ce contexte de liaison avec <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> lorsque le client souhaite que les gestionnaires de dossiers <strong>Internet Shell</strong> génèrent un IDList pour l’URL si un dossier DAV ne peut pas être créé pour l’URL donnée.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour passer l’élément d’origine qui est à nouveau analysé lorsque cet élément est stocké en tant qu’objet <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> qui implémente également l’interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> . avant le Windows 7, cette valeur n’était pas définie dans un fichier d’en-tête. Il peut être défini par l’appelant ou passé comme valeur de chaîne de <strong>L &quot; ParseOriginalItem &quot; </strong>. à partir de Windows 7, la valeur est définie dans Shlobj. h. Notez qu’il s’agit d’un autre en-tête que les autres constantes STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP</strong>. Spécifiez ce contexte de liaison pour activer un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> sur le dossier <strong>Desktop</strong> pour analyser les URL comme s’il s’agissait de dossiers. Utilisez ce contexte de liaison pour établir une liaison à un serveur WebDAV.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour empêcher un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> sur le dossier du <strong>Bureau</strong> formulaire d’analyse des URL. Ce contexte de liaison peut être substitué par <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour remplacer la Banque de propriétés par défaut utilisée par la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> et utilisez la Banque de propriétés spécifiée comme paramètre de liaison à la place. S’applique aux dossiers délégués.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP SP2</strong>. Spécifiez ce contexte de liaison pour activer un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> sur le dossier <strong>Desktop</strong> pour utiliser la &quot; &quot; notation de préfixe Shell : pour accéder aux fichiers.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour déclencher un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> pour afficher la boîte de dialogue Diagnostics du réseau si l’analyse d’un chemin d’accès réseau échoue.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows Vista</strong>. Spécifiez ce contexte de liaison pour déclencher un appel à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> pour ignorer la vérification du cache des partages réseau et contacter directement le serveur réseau. Les informations sur les partages réseau sont mises en cache pour améliorer les performances, et <strong>IShellFolder ::P arsedisplayname</strong> vérifie par défaut ce cache.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP</strong>. Spécifiez ce contexte de liaison pour passer les propriétés analysées à la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> pour un espace de noms délégué. L’espace de noms peut utiliser les propriétés transmises au lieu d’essayer d’analyser le nom lui-même.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Vista uniquement.</strong> Un contexte de liaison d’analyse qui est utilisé pour passer un ensemble de propriétés et le nom de l’élément lors de l’appel de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a>. L’objet dans le contexte de liaison implémente <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> et est récupéré en appelant <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx :: GetObjectParam</strong></a>.<br/> DBFolder est une source de données Shell qui représente des éléments dans les résultats de recherche et les vues basées sur des requêtes. DBFolder récupère ces éléments en interrogeant le système de recherche de Windows. Les éléments des résultats de la recherche sont identifiés par un schéma de protocole, par exemple &quot; fichier : &quot; ou &quot; MAPI : &quot; . DBFolder fournit le comportement de ces éléments en déléguant aux sources de données Shell créées pour ces protocoles. Pour plus d’informations, consultez <a href="/previous-versions/bb233544(v=msdn.10)">développement de compléments de gestionnaires de protocole</a> .<br/> quand DBFolder délègue son opération d’analyse aux sources de données de l’interpréteur de commandes qui prennent en charge Windows les protocoles de recherche, ce contexte de liaison fournit l’accès aux valeurs qui ont été retournées dans le résultat de la requête pour cet élément. Notamment :<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System. ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System. ParsingPath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System. ItemPathDisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System. ItemNameDisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Ce contexte de liaison peut également être utilisé pour analyser un élément DBFolder si un client possède un ensemble de propriétés qui définissent l’élément. Dans ce cas, un nom vide doit être passé à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a>.<br/> avant le Windows 7, cette valeur n’était pas définie dans un fichier d’en-tête. Il peut être défini par l’appelant ou passé comme valeur de chaîne : <code>L&quot;ParseWithProperties&quot;</code> . à partir de Windows 7, la valeur est définie dans Shlobj. h. Notez qu’il s’agit d’un en-tête différent de celui dans lequel les autres constantes STR sont définies.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introduite dans Windows 8</strong>. Spécifiez ce contexte de liaison pour indiquer que le paramètre de contexte de liaison est un conteneur de propriétés (<a href="/windows/win32/api/oaidl/nn-oaidl-ipropertybag"><strong>IPropertyBag</strong></a>) utilisé pour passer des valeurs de type Variant dans le contexte de liaison. Pour plus d’informations, consultez la section Notes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>introduite dans Windows XP</strong>. Spécifiez ce contexte de liaison pour faire en sorte que les appels aux méthodes <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder ::P arsedisplayname</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> ignorent une extension d’espace de noms de Shell particulière lors de l’analyse ou de la liaison. Le CLSID de l’espace de noms à ignorer est fourni par la méthode <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist :: GetClassID</strong></a> du paramètre de liaison. <br/>
<blockquote>
[!Note]<br />
introduite dans Windows SP3 2000, cette valeur a été définie dans Shlobj. h jusqu’à Windows XP, lorsqu’elle a été déplacée vers Shobjidl. h.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">Non utilisé.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarques

Les contextes de liaison sont utilisés pour passer des paramètres facultatifs à des fonctions qui ont un \* paramètre IBindCtx. Ces paramètres sont exprimés en tant qu’objets COM et peuvent implémenter des interfaces qui sont utilisées pour modéliser les données de paramètre. Certains contextes de liaison représentent une valeur booléenne, où **true** indique qu’un objet qui implémente uniquement [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et false indique qu’aucun objet n’est présent.

[**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname), [**IShellFolder :: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) et [**IShellItem :: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) prennent un contexte de liaison et vous pouvez leur transmettre des paramètres via ce contexte de liaison.

Certains contextes de liaison sont spécifiques à certaines implémentations de source de données ou types de gestionnaires.

Les paramètres de contexte de liaison sont définis pour être utilisés avec une fonction ou une méthode spécifique.

Lors de la demande d’un magasin de propriétés via [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), vous pouvez spécifier l’équivalent de [**GPS par \_ défaut**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) en passant un paramètre [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) null. Vous pouvez également spécifier l’équivalent de GPS \_ ReadWrite en passant un mode de STGM \_ ReadWrite \| STGM \_ exclusif dans le contexte de liaison.

Le jeu de propriétés spécifié par l’objet de contexte de liaison **Str \_ PROPERTYBAG \_ param** contient des valeurs supplémentaires auxquelles vous pouvez accéder avec les méthodes [**IPropertyBag :: Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) et [**IPropertyBag :: Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85)) .



| Nom de la propriété                                 | Type     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_indicateurs d’éléments d’énumération Str \_ \_                       | VT \_ UI4  | **Introduite dans Windows 8**. Spécifie une valeur [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) à passer à [**IShellFolder :: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) lorsque vous appelez [**IShellItem :: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) avec **BHID \_ EnumItems**.                                                                                                                                                                                                                         |
| STR- \_ analyser l' \_ \_ Association explicite \_ avec succès | VT \_ bool | **introduite dans Windows 7**. La méthode [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) définit cette propriété pour indiquer à l’appelant que le IDList retourné a été lié au [ProgID](fa-progids.md) spécifié avec l' **\_ analyse Str avec un \_ \_ \_ ProgID explicite** ou l’application spécifiée avec l' **\_ analyse Str \_ avec \_ \_ ASSOCAPP explicite**. Lorsque la réussite de l' **\_ \_ \_ Association \_ explicite de Str** est absente, le ProgID ou l’application n’a pas été lié à IDList. |
| CHAÎNE \_ Parse \_ avec \_ \_ ASSOCAPP explicite          | VT \_ BSTR | **introduite dans Windows 7**. Spécifiez cette propriété pour déclencher un appel à la méthode [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) pour retourner un IDList lié au gestionnaire d’association de types de fichiers pour l’application.                                                                                                                                                                                                                                          |
| CHAÎNE \_ Parse \_ avec \_ \_ ProgID explicite            | VT \_ BSTR | **introduite dans Windows 7**. Spécifiez cette propriété pour déclencher un appel à la méthode [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) pour retourner un IDList lié au gestionnaire d’association de fichiers du [ProgID](fa-progids.md)fourni.                                                                                                                                                                                                                          |



 

Consultez l' [exemple analyse avec des paramètres](samples-parsingwithparameters.md) pour obtenir un exemple d’utilisation des valeurs de contexte de liaison.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 

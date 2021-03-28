---
description: Attributs qui peuvent être récupérés sur un élément (fichier ou dossier) ou sur un ensemble d’éléments.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: SFGAO (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f01691c3dbb1e5b76d93739b4893ffaf7c69e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757725"
---
# <a name="sfgao"></a>SFGAO

Attributs qui peuvent être récupérés sur un élément (fichier ou dossier) ou sur un ensemble d’éléments.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valeur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl> <dt><strong>SFGAO_CANCOPY</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés peuvent être copiés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl> <dt><strong>SFGAO_CANMOVE</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés peuvent être déplacés.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl> <dt><strong>SFGAO_CANLINK</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Des raccourcis peuvent être créés pour les éléments spécifiés. Cet attribut a la même valeur que <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br/> Si une extension d’espace de noms retourne cet attribut, une entrée de <strong>raccourci créer</strong> avec un gestionnaire par défaut est ajoutée au menu contextuel qui s’affiche pendant les opérations de glisser-déplacer. L’extension peut également implémenter son propre gestionnaire pour le verbe <em>Link</em> à la place de la valeur par défaut. Si l’extension le fait, il est responsable de la création du raccourci.<br/> Un élément de <strong>raccourci créer</strong> est également ajouté au menu <strong>fichier</strong> de l’Explorateur Windows et aux menus contextuels normaux.<br/> Si l’élément est sélectionné, la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu :: commande InvokeCommand</strong></a> de votre application est appelée avec le <strong>membre lpVerb</strong> de la structure <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> défini sur <em>Link</em>. Votre application est chargée de créer le lien.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl> <dt><strong>SFGAO_STORAGE</strong></dt> <dt>0x00000008</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés peuvent être liés à un objet <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a> par le biais de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a>. Pour plus d’informations sur les fonctionnalités de manipulation d’espace de noms, consultez <strong>IStorage</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl> <dt><strong>SFGAO_CANRENAME</strong></dt> <dt>0x00000010</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés peuvent être renommés. Notez que cette valeur est essentiellement une suggestion ; tous les clients d’espace de noms n’autorisent pas le changement de nom des éléments. Toutefois, ceux qui doivent avoir cet attribut doivent être définis.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl> <dt><strong>SFGAO_CANDELETE</strong></dt> <dt>0x00000020</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés peuvent être supprimés.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl> <dt><strong>SFGAO_HASPROPSHEET</strong></dt> <dt>0x00000040</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés ont des feuilles de propriétés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl> <dt><strong>SFGAO_DROPTARGET</strong></dt> <dt>0x00000100</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés sont des cibles de dépôt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl> <dt><strong>SFGAO_CAPABILITYMASK</strong></dt> <dt>0x00000177</dt> </dl></td>
<td style="text-align: left;">Cet indicateur est un masque pour les attributs de fonctionnalité : SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET et SFGAO_DROPTARGET. Normalement, les appelants n’utilisent pas cette valeur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl> <dt><strong>SFGAO_SYSTEM</strong></dt> <dt>0x00001000</dt> </dl></td>
<td style="text-align: left;"><strong>Windows 7 et versions ultérieures</strong>. Les éléments spécifiés sont des éléments système.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl> <dt><strong>SFGAO_ENCRYPTED</strong></dt> <dt>0x00002000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés sont chiffrés et peuvent nécessiter une présentation spéciale.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl> <dt><strong>SFGAO_ISSLOW</strong></dt> <dt>0x00004000</dt> </dl></td>
<td style="text-align: left;">L’accès à l’élément (via <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> ou d’autres interfaces de stockage) est supposé être une opération lente. Les applications doivent éviter d’accéder aux éléments signalés par SFGAO_ISSLOW. <br/>
<blockquote>
[!Note]<br />
L’ouverture d’un flux pour un élément est généralement une opération lente à tout moment. SFGAO_ISSLOW indique qu’il est supposé être particulièrement lent, par exemple dans le cas de connexions réseau lentes ou de fichiers hors connexion (FILE_ATTRIBUTE_OFFLINE). Toutefois, l’interrogation de SFGAO_ISSLOW est une opération lente. Les applications doivent interroger SFGAO_ISSLOW uniquement sur un thread d’arrière-plan. Une autre méthode, telle que la récupération de la propriété <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> et le test de FILE_ATTRIBUTE_OFFLINE, peut être utilisée à la place d’un appel de méthode qui implique SFGAO_ISSLOW.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl> <dt><strong>SFGAO_GHOSTED</strong></dt> <dt>0x00008000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés apparaissent grisés et non disponibles pour l’utilisateur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl> <dt><strong>SFGAO_LINK</strong></dt> <dt>0x00010000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés sont des raccourcis.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl> <dt><strong>SFGAO_SHARE</strong></dt> <dt>0x00020000</dt> </dl></td>
<td style="text-align: left;">Les objets spécifiés sont partagés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl> <dt><strong>SFGAO_READONLY</strong></dt> <dt>0x00040000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés sont en lecture seule. Dans le cas de dossiers, cela signifie que les nouveaux éléments ne peuvent pas être créés dans ces dossiers. Cela ne doit pas être confondu avec le comportement spécifié par l’indicateur FILE_ATTRIBUTE_READONLY récupéré par <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider :: GetItemData</strong></a> dans une structure <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a> . FILE_ATTRIBUTE_READONLY n’a aucune signification pour les dossiers du système de fichiers Win32.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl> <dt><strong>SFGAO_HIDDEN</strong></dt> <dt>0x00080000</dt> </dl></td>
<td style="text-align: left;">L’élément est masqué et ne doit pas être affiché, sauf si l’option <strong>afficher les fichiers et les dossiers masqués</strong> est activée dans les <strong>paramètres du dossier</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl> <dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt> <dt>0x000FC000</dt> </dl></td>
<td style="text-align: left;">Ne pas utiliser.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl> <dt><strong>SFGAO_NONENUMERATED</strong></dt> <dt>0x00100000</dt> </dl></td>
<td style="text-align: left;">Les éléments sont des éléments non énumérés et doivent être masqués. Ils ne sont pas retournés via un énumérateur tel que celui créé par la méthode <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder :: EnumObjects</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl> <dt><strong>SFGAO_NEWCONTENT</strong></dt> <dt>0x00200000</dt> </dl></td>
<td style="text-align: left;">Les éléments contiennent un nouveau contenu, tel que défini par l’application en question.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl> <dt><strong>SFGAO_CANMONIKER</strong></dt> </dl></td>
<td style="text-align: left;">Non pris en charge.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl> <dt><strong>SFGAO_HASSTORAGE</strong></dt> </dl></td>
<td style="text-align: left;">Non pris en charge.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl> <dt><strong>SFGAO_STREAM</strong></dt> <dt>0x00400000</dt> </dl></td>
<td style="text-align: left;">Indique que l’élément est associé à un flux. Ce flux est accessible via un appel à <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder :: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem :: BindToHandler</strong></a> avec IID_IStream dans le paramètre <em>riid</em> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl> <dt><strong>SFGAO_STORAGEANCESTOR</strong></dt> <dt>0x00800000</dt> </dl></td>
<td style="text-align: left;">Les enfants de cet élément sont accessibles via <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> ou <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>. Ces enfants sont marqués avec SFGAO_STORAGE ou SFGAO_STREAM.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl> <dt><strong>SFGAO_VALIDATE</strong></dt> <dt>0x01000000</dt> </dl></td>
<td style="text-align: left;">Lorsqu’il est spécifié en tant qu’entrée, SFGAO_VALIDATE indique au dossier de valider que les éléments contenus dans un dossier ou un tableau d’éléments d’interpréteur de commandes existent. Si un ou plusieurs de ces éléments n’existent pas, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder :: GetAttributesOf</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray :: GetAttributes</strong></a> retournent un code d’échec. Cet indicateur n’est jamais retourné en tant que valeur [out].<br/> En cas d’utilisation avec le dossier du système de fichiers, SFGAO_VALIDATE indique au dossier de supprimer les propriétés mises en cache récupérées par les clients de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2 :: GetDetailsEx</strong></a> qui ont pu être accumulés pour les éléments spécifiés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl> <dt><strong>SFGAO_REMOVABLE</strong></dt> <dt>0x02000000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés se trouvent sur un support amovible ou sont eux-mêmes des périphériques amovibles.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl> <dt><strong>SFGAO_COMPRESSED</strong></dt> <dt>0x04000000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés sont compressés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl> <dt><strong>SFGAO_BROWSABLE</strong></dt> <dt>0x08000000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés peuvent être hébergés à l’intérieur d’un navigateur Web ou d’un frame de l’Explorateur Windows.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl> <dt><strong>SFGAO_FILESYSANCESTOR</strong></dt> <dt>0x10000000</dt> </dl></td>
<td style="text-align: left;">Les dossiers spécifiés sont des dossiers du système de fichiers ou contiennent au moins un descendant (enfant, petit-enfant ou version ultérieure) qui est un dossier du système de fichiers (SFGAO_FILESYSTEM).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl> <dt><strong>SFGAO_FOLDER</strong></dt> <dt>0x20000000</dt> </dl></td>
<td style="text-align: left;">Les éléments spécifiés sont des dossiers. Certains éléments peuvent être marqués avec SFGAO_STREAM et SFGAO_FOLDER, par exemple un fichier compressé avec une extension de nom de fichier. zip. Certaines applications peuvent inclure cet indicateur lors du test des éléments qui sont à la fois des fichiers et des conteneurs.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl> <dt><strong>SFGAO_FILESYSTEM</strong></dt> <dt>0x40000000</dt> </dl></td>
<td style="text-align: left;">Les dossiers ou fichiers spécifiés font partie du système de fichiers (c’est-à-dire qu’il s’agit de fichiers, de répertoires ou de répertoires racine). Les noms analysés des éléments peuvent être supposés être des chemins d’accès de système de fichiers Win32 valides. Il peut s’agir d’un chemin d’accès UNC ou d’une lettre de lecteur.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl> <dt><strong>SFGAO_STORAGECAPMASK</strong></dt> <dt>0x70C50008</dt> </dl></td>
<td style="text-align: left;">Cet indicateur est un masque pour les attributs de capacité de stockage : SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER et SFGAO_FILESYSTEM. Normalement, les appelants n’utilisent pas cette valeur.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl> <dt><strong>SFGAO_HASSUBFOLDER</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">Les dossiers spécifiés comportent des sous-dossiers. L’attribut SFGAO_HASSUBFOLDER est uniquement consultatif et peut être retourné par les implémentations de dossiers Shell même s’ils ne contiennent pas de sous-dossiers. Notez, toutefois, que l’inverse, qui ne retourne pas SFGAO_HASSUBFOLDER, indique définitivement que les objets de dossier n’ont pas de sous-dossiers.<br/> Le retour de SFGAO_HASSUBFOLDER est recommandé chaque fois qu’un certain temps est nécessaire pour déterminer si des sous-dossiers existent. Par exemple, le shell retourne toujours SFGAO_HASSUBFOLDER lorsqu’un dossier se trouve sur un lecteur réseau.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl> <dt><strong>SFGAO_CONTENTSMASK</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">Cet indicateur est un masque pour les attributs de contenu, à l’heure actuelle uniquement SFGAO_HASSUBFOLDER. Normalement, les appelants n’utilisent pas cette valeur.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl> <dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt> <dt>0x81044000</dt> </dl></td>
<td style="text-align: left;">Masque utilisé par la propriété <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a> pour déterminer les attributs qui sont considérés comme provoquant des calculs lents ou qui manquent de contexte : SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER et SFGAO_VALIDATE. Normalement, les appelants n’utilisent pas cette valeur.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder ::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**IShellItemArray :: GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 

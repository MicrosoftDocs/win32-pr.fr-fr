---
title: Message CB_DIR (winuser. h)
description: Ajoute des noms à la liste affichée par la zone de liste déroulante. Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier. \_Le répertoire CB peut également ajouter des lettres de lecteur mappées à la liste.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: defa19ffdebfb448e1a89c141da0b275c1df1bffdcfa9e3914293400d706b7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577119"
---
# <a name="cb_dir-message"></a>\_Message du répertoire CB

Ajoute des noms à la liste affichée par la zone de liste déroulante. Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier. **CB \_ DIR** peut également ajouter des lettres de lecteur mappées à la liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Attributs des fichiers ou répertoires à ajouter à la zone de liste déroulante. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_Archive DDL**</dt> </dl>       | Comprend les fichiers archivés.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_répertoire DDL**</dt> </dl> | Comprend les sous-répertoires, qui sont placés entre crochets ( \[ \] ).<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_lecteurs DDL**</dt> </dl>          | Tous les lecteurs mappés sont ajoutés à la liste. Les lecteurs sont répertoriés sous la forme \[ - *x* - \] , où *x* est la lettre de lecteur.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DLL en \_ mode exclusif**</dt> </dl> | Comprend uniquement les fichiers avec les attributs spécifiés. Par défaut, les fichiers en lecture/écriture sont répertoriés même si DDL \_ ReadWrite n’est pas spécifié.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ masqué**</dt> </dl>          | Comprend les fichiers masqués.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ ReadOnly**</dt> </dl>    | Comprend des fichiers en lecture seule.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**lecture/ \_ écriture DDL**</dt> </dl> | Comprend des fichiers en lecture/écriture sans attributs supplémentaires. Il s’agit de la valeur par défaut.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_système DDL**</dt> </dl>          | Comprend des fichiers système.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur **LPCTSTR** vers une chaîne se terminant par un caractère null qui spécifie un chemin d’accès absolu, un chemin d’accès relatif ou un nom de fichier. Un chemin d’accès absolu peut commencer par une lettre de lecteur (par exemple, d : \) ou un nom UNC (par exemple, \\ \\ *MachineName* \\ *Nom_Partage*). Si la chaîne spécifie un nom de fichier ou un répertoire qui a les attributs spécifiés par le paramètre *wParam* , le nom de fichier ou le répertoire est ajouté à la liste. Si le nom de fichier ou le nom de répertoire contient des caractères génériques ( ? ou \* ), tous les fichiers ou répertoires qui correspondent à l’expression générique et dont les attributs sont spécifiés par le paramètre *wParam* sont ajoutés à la liste affichée dans la zone de liste déroulante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est l’index de base zéro du dernier nom ajouté à la liste.

Si une erreur se produit, la valeur de retour est CB \_ Err. Si l’espace est insuffisant pour stocker les nouvelles chaînes, la valeur de retour est CB \_ ERRSPACE.

## <a name="remarks"></a>Remarques

Si *wParam* inclut l' \_ indicateur de répertoire DDL et que *lParam* spécifie tous les sous-répertoires d’un répertoire de premier niveau, par exemple C : \\ temp \\ \* , la zone de liste inclura toujours une entrée « .. » pour le répertoire racine. Cela est vrai même si le répertoire racine contient des attributs système ou masqués et que les \_ indicateurs système DDL et DDL ne \_ sont pas spécifiés. Le répertoire racine d’un volume NTFS a des attributs système et masqués.

La liste affiche les noms de fichiers longs, le cas échéant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**$ \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_INSERTSTRING CB**](cb-insertstring.md)
</dt> <dt>

[**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 






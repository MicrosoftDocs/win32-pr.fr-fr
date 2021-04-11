---
title: Message LB_DIR (winuser. h)
description: Ajoute des noms à la liste affichée par une zone de liste. Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier. LB \_ dir peut également ajouter des lettres de lecteur mappées à la zone de liste.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106000"
---
# <a name="lb_dir-message"></a>Message du répertoire du LB \_

Ajoute des noms à la liste affichée par une zone de liste. Le message ajoute les noms des répertoires et des fichiers qui correspondent à une chaîne spécifiée et un ensemble d’attributs de fichier. **Lb \_ DIR** peut également ajouter des lettres de lecteur mappées à la zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Attributs des fichiers ou répertoires à ajouter à la zone de liste. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_Archive DDL**</dt> </dl>       | Comprend les fichiers archivés.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_répertoire DDL**</dt> </dl> | Comprend des sous-répertoires. Les noms de sous-répertoires sont placés entre crochets ( \[ \] ).<br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_lecteurs DDL**</dt> </dl>          | Tous les lecteurs mappés sont ajoutés à la liste. Les lecteurs sont répertoriés sous la forme \[ - *x* - \] , où *x* est la lettre de lecteur.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DLL en \_ mode exclusif**</dt> </dl> | Comprend uniquement les fichiers avec les attributs spécifiés. Par défaut, les fichiers en lecture/écriture sont répertoriés même si DDL \_ ReadWrite n’est pas spécifié.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ masqué**</dt> </dl>          | Comprend les fichiers masqués.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ ReadOnly**</dt> </dl>    | Comprend des fichiers en lecture seule.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**lecture/ \_ écriture DDL**</dt> </dl> | Comprend des fichiers en lecture/écriture sans attributs supplémentaires. Il s'agit du paramètre par défaut.<br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_système DDL**</dt> </dl>          | Comprend des fichiers système.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui spécifie un chemin d’accès absolu, un chemin d’accès relatif ou un nom de fichier. Un chemin d’accès absolu peut commencer par une lettre de lecteur (par exemple, d : \) ou un nom UNC (par exemple, \\ \\ *MachineName* \\ *Nom_Partage*).

Si la chaîne spécifie un nom de fichier ou un répertoire qui a les attributs spécifiés par le paramètre *wParam* , le nom de fichier ou le répertoire est ajouté à la liste. Si le nom de fichier ou de répertoire contient des caractères génériques ( ? ou \* ), tous les fichiers ou répertoires qui correspondent à l’expression générique et dont les attributs sont spécifiés par le paramètre *wParam* sont ajoutés à la liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est l’index de base zéro du dernier nom ajouté à la liste.

Si une erreur se produit, la valeur de retour est LB \_ Err. Si l’espace est insuffisant pour stocker les nouvelles chaînes, la valeur de retour est LB \_ ERRSPACE.

## <a name="remarks"></a>Notes

Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100). Il réserve la quantité de mémoire spécifiée afin que les messages de **\_ Répertoire de livres** suivants prennent le plus de temps possible. Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* . Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.

Si *wParam* inclut l' \_ indicateur de répertoire DDL et que *lParam* spécifie tous les sous-répertoires d’un répertoire de premier niveau, par exemple C : \\ temp \\ \* , la zone de liste inclura toujours une entrée « .. » pour le répertoire racine. Cela est vrai même si le répertoire racine contient des attributs système ou masqués et que les \_ indicateurs système DDL et DDL ne \_ sont pas spécifiés. Le répertoire racine d’un volume NTFS a des attributs système et masqués.

La liste affiche les noms de fichiers longs, le cas échéant.

Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de CP \_ ACP. Cela peut entraîner des problèmes. Par exemple, les caractères romains accentués dans une zone de liste non Unicode dans les fenêtres japonaises sont tronqués. Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 






---
title: Types de ressources (winuser. h)
description: Les types de ressources prédéfinis sont les suivants.
ms.assetid: 8d27f79a-8165-4565-a975-f25b2344efdc
topic_type:
- apiref
api_name:
- RT_ACCELERATOR
- RT_ANICURSOR
- RT_ANIICON
- RT_BITMAP
- RT_CURSOR
- RT_DIALOG
- RT_DLGINCLUDE
- RT_FONT
- RT_FONTDIR
- RT_GROUP_CURSOR
- RT_GROUP_ICON
- RT_HTML
- RT_ICON
- RT_MANIFEST
- RT_MENU
- RT_MESSAGETABLE
- RT_PLUGPLAY
- RT_RCDATA
- RT_STRING
- RT_VERSION
- RT_VXD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595f1d459f645d26014a644d0e2b7cb608f4c6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529992"
---
# <a name="resource-types"></a>Types de ressources

Les types de ressources prédéfinis sont les suivants.



| Constante/valeur                                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RT_ACCELERATOR"></span><span id="rt_accelerator"></span><dl> <dt>**RT \_ ACCÉLÉRATEUR**</dt> <dt>MAKEINTRESOURCE (9)</dt> </dl>                                 | Table d’accélérateurs.<br/>                                                                                                                                                                                                                                                                    |
| <span id="RT_ANICURSOR"></span><span id="rt_anicursor"></span><dl> <dt>**RT \_ ANICURSOR**</dt> <dt>MAKEINTRESOURCE (21)</dt> </dl>                                      | Curseur animé.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_ANIICON"></span><span id="rt_aniicon"></span><dl> <dt>**RT \_ ANIICON**</dt> <dt>MAKEINTRESOURCE (22)</dt> </dl>                                            | Icône animée.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_BITMAP"></span><span id="rt_bitmap"></span><dl> <dt>**RT \_ MAKEINTRESOURCE BITMAP**</dt> <dt>(2)</dt> </dl>                                                | Ressource bitmap.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_CURSOR"></span><span id="rt_cursor"></span><dl> <dt>**RT \_ CURSEUR**</dt> <dt>MAKEINTRESOURCE (1)</dt> </dl>                                                | Ressource de curseur dépendante du matériel.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_DIALOG"></span><span id="rt_dialog"></span><dl> <dt>**RT \_ Boîte de dialogue**</dt> <dt>MAKEINTRESOURCE (5)</dt> </dl>                                                | Boîte de dialogue.<br/>                                                                                                                                                                                                                                                                           |
| <span id="RT_DLGINCLUDE"></span><span id="rt_dlginclude"></span><dl> <dt>**RT \_ DLGINCLUDE**</dt> <dt>MAKEINTRESOURCE (17)</dt> </dl>                                   | Permet à un outil d’édition de ressources d’associer une chaîne à un fichier. rc. En règle générale, la chaîne est le nom du fichier d’en-tête qui fournit des noms symboliques. Le compilateur de ressources analyse la chaîne, mais ignore la valeur. Par exemple, <br/> `1 DLGINCLUDE "MyFile.h"`<br/> |
| <span id="RT_FONT"></span><span id="rt_font"></span><dl> <dt>**RT \_**</dt> <dt>MAKEINTRESOURCE de police (8)</dt> </dl>                                                      | Ressource de police.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_FONTDIR"></span><span id="rt_fontdir"></span><dl> <dt>**RT \_ FONTDIR**</dt> <dt>MAKEINTRESOURCE (7)</dt> </dl>                                             | Ressource du répertoire de polices.<br/>                                                                                                                                                                                                                                                              |
| <span id="RT_GROUP_CURSOR"></span><span id="rt_group_cursor"></span><dl> <dt>**RT \_ \_**</dt> <dt>MAKEINTRESOURCE de curseur de groupe ((ULONG \_ PTR) (RT \_ Cursor) + 11)</dt> </dl> | Ressource de curseur indépendante du matériel.<br/>                                                                                                                                                                                                                                                 |
| <span id="RT_GROUP_ICON"></span><span id="rt_group_icon"></span><dl> <dt>**RT \_ \_Icône de groupe**</dt> <dt>MAKEINTRESOURCE ((ULONG \_ PTR) ( \_ icône RT) + 11)</dt> </dl>         | Ressource icône indépendante du matériel.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_HTML"></span><span id="rt_html"></span><dl> <dt>**RT \_ MAKEINTRESOURCE HTML**</dt> <dt>(23)</dt> </dl>                                                     | Ressource HTML.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_ICON"></span><span id="rt_icon"></span><dl> <dt>**RT \_ ICÔNE**</dt> <dt>MAKEINTRESOURCE (3)</dt> </dl>                                                      | Ressource icône dépendante du matériel.<br/>                                                                                                                                                                                                                                                     |
| <span id="RT_MANIFEST"></span><span id="rt_manifest"></span><dl> <dt>**RT \_ MANIFESTE**</dt> <dt>MAKEINTRESOURCE (24)</dt> </dl>                                         | Manifeste d’assembly côte à côte.<br/>                                                                                                                                                                                                                                                       |
| <span id="RT_MENU"></span><span id="rt_menu"></span><dl> <dt>**RT \_ MENU**</dt> <dt>MAKEINTRESOURCE (4)</dt> </dl>                                                      | Ressource de menu.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_MESSAGETABLE"></span><span id="rt_messagetable"></span><dl> <dt>**RT \_ MESSAGETABLE**</dt> <dt>MAKEINTRESOURCE (11)</dt> </dl>                             | Entrée de table de messages.<br/>                                                                                                                                                                                                                                                                  |
| <span id="RT_PLUGPLAY"></span><span id="rt_plugplay"></span><dl> <dt>**RT \_ PLUGPLAY**</dt> <dt>MAKEINTRESOURCE (19)</dt> </dl>                                         | Ressource Plug-and-Play.<br/>                                                                                                                                                                                                                                                               |
| <span id="RT_RCDATA"></span><span id="rt_rcdata"></span><dl> <dt>**RT \_ MAKEINTRESOURCE RCDATA**</dt> <dt>(10)</dt> </dl>                                               | Ressource définie par l’application (données brutes).<br/>                                                                                                                                                                                                                                              |
| <span id="RT_STRING"></span><span id="rt_string"></span><dl> <dt>**RT \_ CHAÎNE**</dt> <dt>MAKEINTRESOURCE (6)</dt> </dl>                                                | Entrée de table de chaînes.<br/>                                                                                                                                                                                                                                                                   |
| <span id="RT_VERSION"></span><span id="rt_version"></span><dl> <dt>**RT \_ VERSION**</dt> <dt>MAKEINTRESOURCE (16)</dt> </dl>                                            | Ressource de version.<br/>                                                                                                                                                                                                                                                                     |
| <span id="RT_VXD"></span><span id="rt_vxd"></span><dl> <dt>**RT \_ VXD**</dt> <dt>MAKEINTRESOURCE (20)</dt> </dl>                                                        | Pilote.<br/>                                                                                                                                                                                                                                                                                  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

 






---
description: Représente une collection des fenêtres ouvertes qui appartiennent au shell. Les méthodes associées à ces objets peuvent contrôler et exécuter des commandes dans l’interpréteur de commandes, et obtenir d’autres objets liés à l’interpréteur de commandes.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Objet ShellWindows (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235140"
---
# <a name="shellwindows-object"></a>Objet ShellWindows

Représente une collection des fenêtres ouvertes qui appartiennent au shell. Les méthodes associées à ces objets peuvent contrôler et exécuter des commandes dans l’interpréteur de commandes, et obtenir d’autres objets liés à l’interpréteur de commandes.

## <a name="members"></a>Membres

L’objet **ShellWindows** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **ShellWindows** a ces méthodes.



| Méthode                                                 | Description                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](shellwindows--newenum-method-7ral.md) | Crée et retourne un nouvel objet **ShellWindows** qui est une copie de cet objet **ShellWindows** .<br/>        |
| [**Élément**](shellwindows-item.md)                      | Récupère un objet [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) qui représente la fenêtre de l’interpréteur de commandes.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **ShellWindows** a ces propriétés.



| Propriété                                       | Type d’accès          | Description                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Count**](shellwindows-count.md)<br/> | Lecture seule<br/> | Contient le nombre d’éléments de la collection.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 

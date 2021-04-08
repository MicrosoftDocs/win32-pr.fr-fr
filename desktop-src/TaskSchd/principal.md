---
title: Objet principal
description: Objet de script qui fournit les informations d’identification de sécurité pour un principal.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Planificateur de tâches de l’objet principal
- Planificateur de tâches de l’objet principal, Description
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843325"
---
# <a name="principal-object"></a>Objet principal

Objet de script qui fournit les informations d’identification de sécurité pour un principal. Ces informations d’identification de sécurité définissent le contexte de sécurité pour les tâches associées au principal.

## <a name="members"></a>Membres

L’objet **principal** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **principal** possède ces propriétés.



| Propriété                                                | Type d’accès           | Description                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NomComplet**](principal-displayname.md)<br/> | Lecture/écriture<br/> | Obtient ou définit le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.<br/>                                                                |
| [**GroupId**](principal-groupid.md)<br/>         | Lecture/écriture<br/> | Obtient ou définit l’identificateur du groupe d’utilisateurs qui est requis pour exécuter les tâches associées au principal.<br/>                           |
| [**Identifi**](principal-id.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit l'identificateur unique du principal.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Lecture/écriture<br/> | Obtient ou définit la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.<br/>                                  |
| [**RunLevel**](principal-runlevel.md)<br/>       | Lecture/écriture<br/> | Obtient ou définit l’identificateur qui est utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches associées au principal.<br/> |
| [**IDutilisateur**](principal-userid.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’identificateur de l’utilisateur qui est requis pour exécuter les tâches associées au principal.<br/>                                        |



 

## <a name="remarks"></a>Notes

Lorsque vous spécifiez un compte, n’oubliez pas d’utiliser correctement la double barre oblique inverse dans le code pour spécifier le domaine et le nom d’utilisateur. Par exemple, utilisez domaine \\ \\ nom d’utilisateur pour spécifier une valeur pour la propriété [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, les informations d’identification de sécurité d’un principal sont spécifiées dans l’élément [**principal**](taskschedulerschema-principal-principaltype-element.md) du schéma planificateur de tâches.

Si une tâche est inscrite à l’aide de l’outil de ligne de commande at.exe, et que cet objet est utilisé pour extraire des informations sur la tâche, la propriété [**LogonType**](principal-logontype.md) retourne 0, la propriété [**runlevel**](principal-runlevel.md) retourne 0 et la propriété [**userid**](principal-userid.md) retourne la valeur Nothing.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






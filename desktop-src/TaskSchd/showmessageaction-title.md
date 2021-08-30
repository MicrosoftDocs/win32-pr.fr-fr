---
title: ShowMessageAction. title, propriété
description: Pour les scripts, obtient ou définit le titre de la boîte de message.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Propriété Title Planificateur de tâches
- Propriété Title Planificateur de tâches, objet ShowMessageAction
- Objet ShowMessageAction Planificateur de tâches, propriété Title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4297bf3d845495e1783d3d8c65f64fc5df85a555b58d9afeb4a80c0fe96b517
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072609"
---
# <a name="showmessageactiontitle-property"></a>ShowMessageAction. title, propriété

\[Cet objet n’est plus pris en charge. vous pouvez utiliser IExecAction avec la fonction Windows scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) pour afficher un message dans la session utilisateur.\]

Pour les scripts, obtient ou définit le titre de la boîte de message.

## <a name="syntax"></a>Syntaxe


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a>Valeur de la propriété

Titre du message.

## <a name="remarks"></a>Remarques

Les chaînes paramétrables peuvent être utilisées dans le texte du titre de la boîte de message. Pour plus d’informations, consultez la section exemples dans [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’une ressource .dll fichier. Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources. Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier .dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource. Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                    |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                       |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 


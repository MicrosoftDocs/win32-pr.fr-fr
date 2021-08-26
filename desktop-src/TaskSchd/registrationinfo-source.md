---
title: RegistrationInfo. source, propriété
description: Pour les scripts, obtient ou définit l’origine de la tâche. Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Planificateur de tâches de la propriété source
- Planificateur de tâches de propriété source, objet RegistrationInfo
- Planificateur de tâches de l’objet RegistrationInfo, propriété source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97320d63823599e52327533afdba62f795622263e57878515ddd7ade9c98070b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126029"
---
# <a name="registrationinfosource-property"></a>RegistrationInfo. source, propriété

Pour les scripts, obtient ou définit l’origine de la tâche. Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.

## <a name="syntax"></a>Syntaxe


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Valeur de la propriété

Origine de la tâche. Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, les informations sur la source de la tâche sont spécifiées à l’aide de l’élément [**source**](taskschedulerschema-source-registrationinfotype-element.md) du schéma planificateur de tâches.

Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’une ressource .dll fichier. Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources. Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier .dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource. Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 






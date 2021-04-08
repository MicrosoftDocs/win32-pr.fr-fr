---
title: Propriété principal. DisplayName
description: Pour les scripts, obtient ou définit le nom du principal..
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- DisplayName, propriété Planificateur de tâches
- DisplayName Property Planificateur de tâches, objet principal
- Objet principal Planificateur de tâches, propriété DisplayName
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741876"
---
# <a name="principaldisplayname-property"></a>Propriété principal. DisplayName

Pour les scripts, obtient ou définit le nom du principal..

## <a name="syntax"></a>Syntaxe


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a>Valeur de la propriété

Nom du principal.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, le nom complet d’un principal est spécifié dans l’élément [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) du schéma planificateur de tâches.

Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll. Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources. Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource. Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**Directeur**](principal.md)
</dt> </dl>

 

 






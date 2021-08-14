---
description: L’objet UIPreview est utilisé pour afficher les boîtes de dialogue et les panneaux de l’interface utilisateur lors de la création. Cet objet est créé par la méthode EnableUIPreview de l’objet de base de données.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Objet UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 82436f21cc3920c2e1f635f8d1612118831e7d29f3fb1202105511f2e61f7a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623498"
---
# <a name="uipreview-object"></a>Objet UIPreview

L’objet **UIPreview** est utilisé pour afficher les boîtes de dialogue et les panneaux de l’interface utilisateur lors de la création. Cet objet est créé par la méthode [**EnableUIPreview**](database-enableuipreview.md) de l’objet [**de base de données**](database-object.md) .

## <a name="members"></a>Membres

L’objet **UIPreview** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **UIPreview** a ces méthodes.



| Méthode                                           | Description                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Affiche un panneau d’affichage créé à l’aide du contrôle hôte dans la boîte de dialogue actuellement affichée.<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | Affiche une boîte de dialogue d’interface utilisateur créée, stockée dans la base de données active.<br/>                           |



 

### <a name="properties"></a>Propriétés

L’objet **UIPreview** a ces propriétés.



| Propriété                                          | Type d’accès           | Description                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriété**](uipreview-property.md)<br/> | Lecture/écriture<br/> | Représente la valeur de chaîne d’une propriété de programme d’installation nommée ou, si elle est précédée d’un signe de pourcentage (%), de la valeur d’une variable d’environnement système pour le processus en cours.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview est défini en tant que 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





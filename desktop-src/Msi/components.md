---
description: L’objet Component représente une instance unique d’un composant qui est disponible pour l’énumération.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Objet composant
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092078"
---
# <a name="component-object"></a>Objet composant

L’objet Component représente une instance unique d’un composant qui est disponible pour l’énumération.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cet objet est disponible à partir de Windows Installer 5,0.

## <a name="members"></a>Membres

L’objet **Component** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **Component** possède ces propriétés.



| Propriété                                                    | Description                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ComponentCode**](component-componentcode.md)<br/> | Code du composant en question.<br/>                               |
| [**Context**](component-context.md)<br/>             | Contexte déterminé pour être applicable au composant en question.<br/> |
| [**UserSID**](component-usersid.md)<br/>             | SID de l’utilisateur pour le composant énuméré.<br/>                                     |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Programme d’installation 5,0 ou version ultérieure.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponent est défini en tant que 000C1097-0000-0000-C000-000000000046<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’interface d’automatisation](using-the-automation-interface.md)
</dt> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





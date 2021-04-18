---
description: L’objet ComponentInfo représente des détails supplémentaires sur un composant qui peut être obtenu via un appel de MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Objet ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533063"
---
# <a name="componentinfo-object"></a>Objet ComponentInfo

L’objet ComponentInfo représente des détails supplémentaires sur un composant qui peut être obtenu via un appel de MsiGetComponentPathEx.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. Cet objet est disponible à partir de Windows Installer 5,0.

## <a name="members"></a>Membres

L’objet **ComponentInfo** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ComponentInfo** a ces propriétés.



| Propriété                                                        | Description                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | Code du composant en question.<br/> |
| [**D**](componentinfo-componentcode.md)<br/>          | Chemin d’accès du composant.<br/>                       |
| [**State**](componentinfo-state.md)<br/>                 | État du composant.<br/>                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 ou version ultérieure.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponentInfo est défini en tant que 000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’interface d’automatisation](using-the-automation-interface.md)
</dt> <dt>

[Exemples de scripts Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





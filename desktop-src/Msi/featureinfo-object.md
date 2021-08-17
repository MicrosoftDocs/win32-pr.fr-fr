---
description: L’objet FeatureInfo contient des informations sur la fonctionnalité ciblée et est créée à partir de l’objet session à l’aide de la méthode FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Objet FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 136bc160ea81367f8f55ad81cfc06f5e2e272cafae9d7b8f444a65d34e85d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328369"
---
# <a name="featureinfo-object"></a>Objet FeatureInfo

L’objet **FeatureInfo** contient des informations sur la fonctionnalité ciblée et est créée à partir de l’objet [**session**](session-object.md) à l’aide de la méthode [**FeatureInfo**](session-featureinfo.md) .

## <a name="members"></a>Membres

L’objet **FeatureInfo** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **FeatureInfo** a ces propriétés.



| Propriété                                                  | Type d’accès           | Description                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Attributs**](featureinfo-attributes.md)<br/>   | Lecture/écriture<br/> | Retourne la valeur de la fonctionnalité dans la colonne attributs du tableau des fonctionnalités.<br/> |
| [**Description**](featureinfo-description.md)<br/> |                       | Retourne la description de la fonctionnalité.<br/>                                          |
| [**Titre**](featureinfo-title.md)<br/>             | Lecture seule<br/>  | Retourne le titre de la fonctionnalité.<br/>                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo est défini en tant que 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





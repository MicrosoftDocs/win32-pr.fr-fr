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
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535231"
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
| [**Intitulé**](featureinfo-title.md)<br/>             | Lecture seule<br/>  | Retourne le titre de la fonctionnalité.<br/>                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo est défini en tant que 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemples de scripts Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 





---
description: L’objet ConfigurableItem représente une ligne unique de la table ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Objet ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542754"
---
# <a name="configurableitem-object"></a>Objet ConfigurableItem

L' **objet ConfigurableItem** représente une ligne unique de la [table ModuleConfiguration](moduleconfiguration-table.md). Il s’agit d’un « attribut » configurable unique du module. L’interface se compose de propriétés en lecture seule, une pour chaque colonne de la table ModuleConfiguration. La définition de l’interface est la suivante.

## <a name="members"></a>Membres

L’objet **ConfigurableItem** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ConfigurableItem** a ces propriétés.



| Propriété                                                         | Description                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attributs**](configurableitem-attributes.md)<br/>     | Retourne la valeur dans le champ attributs de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                            |
| [**Context**](configurableitem-context.md)<br/>           | Retourne la valeur dans le champ de contexte de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                               |
| [**DefaultValue**](configurableitem-defaultvalue.md)<br/> | Retourne la valeur dans le champ DefaultValue de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                          |
| [**Description**](configurableitem-description.md)<br/>   | Retourne la valeur dans le champ Description de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                           |
| [**NomComplet**](configurableitem-displayname.md)<br/>   | Retourne la valeur dans le champ DisplayName de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                           |
| [**Format**](configurableitem-format.md)<br/>             | Retourne la valeur dans le champ format de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                                |
| [**HelpKeyword**](configurableitem-helpkeyword.md)<br/>   | Retourne la valeur dans le champ HelpKeyword de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | Retourne la valeur dans le champ HelpLocation de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                          |
| [**Nom**](configurableitem-name.md)<br/>                 | Retourne la valeur dans le champ nom de l’enregistrement de cet objet dans la [table ModuleConfiguration](moduleconfiguration-table.md).<br/> |
| [**Entrer**](configurableitem-type.md)<br/>                 | Retourne la valeur dans le champ type de l’enregistrement de cet objet dans la table ModuleConfiguration.<br/>                                  |



 

## <a name="c"></a>C++

interface **IMsmConfigurableItem : IDispatch**

## <a name="interface-id"></a>ID d’interface



| Constante                      | Valeur                                  |
|-------------------------------|----------------------------------------|
| **IID \_ IMsmConfigurableItem** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 





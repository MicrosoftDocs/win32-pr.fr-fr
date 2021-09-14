---
description: Vous pouvez utiliser les propriétés de l’objet SWbemMethod pour inspecter une définition de méthode unique d’un objet WMI. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Objet SWbemMethod (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918783"
---
# <a name="swbemmethod-object"></a>Objet SWbemMethod

Vous pouvez utiliser les propriétés de l’objet **SWbemMethod** pour inspecter une définition de méthode unique d’un objet WMI. Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .

Cet objet peut être utilisé pour inspecter les définitions des méthodes. Pour appeler les méthodes, vous devez utiliser l’accès direct (consultez [manipulation d’informations sur la classe et l’instance](manipulating-class-and-instance-information.md)) sur un objet [**SWbemObject**](swbemobject.md) (mécanisme recommandé) ou sur l’appel [**SWbemServices. ExecMethod**](swbemservices-execmethod.md) .

> [!Note]  
> Dans cette version de l’API, l’accès en écriture aux informations de méthode n’est pas pris en charge. Si vous souhaitez définir des méthodes ou modifier des définitions de méthode existantes, vous pouvez définir les modifications de méthode dans un fichier MOF et soumettre les modifications à l’aide du [compilateur MOF](compiling-mof-files.md). Vous pouvez également utiliser l' [API com pour WMI](com-api-for-wmi.md).

 

## <a name="members"></a>Membres

L’objet **SWbemMethod** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **SWbemMethod** a ces propriétés.



| Propriété                                                      | Type d’accès          | Description                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Inparamètres**](swbemmethod-inparameters.md)<br/>   | Lecture seule<br/> | Objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres d’entrée pour cette méthode.<br/>              |
| [**Nom**](swbemmethod-name.md)<br/>                   | Lecture seule<br/> | Nom de la méthode.<br/>                                                                                                     |
| [**Origine**](swbemmethod-origin.md)<br/>               | Lecture seule<br/> | Classe d’origine de la méthode.<br/>                                                                                        |
| [**Paramètres de paramètres**](swbemmethod-outparameters.md)<br/> | Lecture seule<br/> | Objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres de sortie et le type de retour de cette méthode.<br/> |
| [**Qualificateurs\_**](swbemmethod-qualifiers-.md)<br/>    | Lecture seule<br/> | Objet [**SWbemQualifierSet**](swbemqualifierset.md) qui contient les qualificateurs de cette méthode.<br/>                  |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 





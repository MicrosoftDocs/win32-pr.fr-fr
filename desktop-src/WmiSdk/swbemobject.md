---
description: Vous pouvez utiliser les méthodes et propriétés de l’objet SWbemObject pour représenter une définition de classe ou une instance d’objet Windows Management Instrumentation (WMI).
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: SWbemObject, objet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518393"
---
# <a name="swbemobject-object"></a>SWbemObject, objet

Vous pouvez utiliser les méthodes et propriétés de l’objet **SWbemObject** pour représenter une définition de classe ou une instance d’objet Windows Management Instrumentation (WMI). Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

Cet objet prend en charge deux types de propriétés et de méthodes. Ceux qui sont définis dans cette section sont des propriétés et des méthodes génériques qui s’appliquent à tous les objets WMI. En outre, cet objet expose les propriétés et les méthodes de l’objet sous-jacent sous forme de propriétés Automation dynamiques et de méthodes de **SWbemObject**. Les noms et les types de ces propriétés et méthodes dépendent de l’objet WMI sous-jacent. Pour plus d’informations sur la façon dont ces propriétés et méthodes dynamiques sont exposées, consultez [manipulation des informations relatives aux classes et aux instances](manipulating-class-and-instance-information.md).

Du point de vue du client WMI, cet objet est toujours in-process. Les opérations d’écriture affectent uniquement la copie locale de l’objet, et les opérations de lecture récupèrent toujours les valeurs à partir de la copie locale. Les mises à jour de WMI sont effectuées uniquement lorsque des objets entiers sont écrits à l’aide d’un appel à la méthode [**SWbemObject. put \_**](swbemobject-put-.md) . Si vous modifiez les propriétés ou les méthodes dans un objet **SWbemObject** , vos modifications ne sont pas écrites dans WMI tant que vous n’avez pas appelé **SWbemObject. put \_**.

La méthode générique et les noms de propriété définis dans cette section se terminent toujours par un trait de soulignement (« \_ ») de fin pour les différencier des méthodes et des propriétés WMI dynamiques de l’objet sous-jacent.

Notez que **SWbemObject** ne peut pas être créé à l’aide de la méthode VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Si vous souhaitez créer une nouvelle classe vide, utilisez [**SWbemServices. obtenir**](swbemservices-get.md) avec un paramètre de chemin d’accès vide. Cet appel retourne un objet **SWbemObject** vide qui peut devenir une classe. Vous pouvez ensuite fournir un nom de classe pour la propriété de [**classe**](swbemobjectpath-class.md) de l’objet [**SWbemObjectPath**](swbemobjectpath.md) retourné par l’appel de [**chemin \_**](swbemobject-path-.md) . Ajoutez des propriétés à la nouvelle classe par la méthode [**Properties \_**](swbemobject-properties-.md) . Pour créer une instance, appelez **GetObject** sur la nouvelle classe.

L’exemple de code suivant montre comment obtenir une nouvelle classe et lui ajouter une propriété. L’objet **SWbemObject** qui représente la classe doit être réécrit dans le référentiel WMI par un appel à [**put \_**](swbemobject-put-.md).


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



Vous pouvez examiner le référentiel à l’aide d’un outil d’affichage tel que [CIM Studio](further-information.md) pour vérifier que la nouvelle classe et l’instance s’affichent. Pour obtenir un exemple de suppression d’une classe et d’une instance du référentiel, consultez [**SWbemServices. Delete**](swbemservices-delete.md) ou [**SWbemObject. \_ Delete**](swbemobject-delete-.md).

## <a name="members"></a>Membres

L’objet **SWbemObject** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemObject** possède ces méthodes.



| Méthode                                                        | Description                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Associateurs\_**](swbemobject-associators-.md)             | Récupère les associateurs de l’objet.<br/>                                                     |
| [**AssociatorsAsync\_**](swbemobject-associatorsasync-.md)   | Récupère de manière asynchrone les associateurs de l’objet.<br/>                                      |
| [**Répliqué\_**](swbemobject-clone-.md)                         | Effectue une copie de l’objet en cours.<br/>                                                          |
| [**CompareTo\_**](swbemobject-compareto-.md)                 | Teste si deux objets sont égaux.<br/>                                                              |
| [**Supprimer\_**](swbemobject-delete-.md)                       | Supprime l’objet de WMI.<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | Supprime de façon asynchrone l’objet de WMI.<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | Exécute une méthode exportée par un fournisseur de méthode.<br/>                                             |
| [**ExecMethodAsync\_**](swbemobject-execmethodasync-.md)     | Exécute de façon asynchrone une méthode exportée par un fournisseur de méthode.<br/>                              |
| [**GetObjectText\_**](swbemobject-getobjecttext-.md)         | Récupère la représentation textuelle de l’objet (syntaxe MOF).<br/>                             |
| [**Fois\_**](swbemobject-instances-.md)                 | Retourne une collection d’instances de l’objet (qui doit être une classe WMI).<br/>                 |
| [**InstancesAsync\_**](swbemobject-instancesasync-.md)       | Retourne de façon asynchrone une collection d’instances de l’objet (qui doit être une classe WMI).<br/>  |
| [**Posé\_**](swbemobject-put-.md)                             | Crée ou met à jour l’objet dans WMI.<br/>                                                        |
| [**PutAsync\_**](swbemobject-putasync-.md)                   | Crée ou met à jour de façon asynchrone l’objet dans WMI.<br/>                                         |
| [**Références\_**](swbemobject-references-.md)               | Retourne des références à l’objet.<br/>                                                            |
| [**ReferencesAsync\_**](swbemobject-referencesasync-.md)     | Retourne de façon asynchrone des références à l’objet.<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | Crée une classe dérivée à partir de l’objet actuel (qui doit être une classe WMI).<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | Crée une nouvelle instance de à partir de l’objet en cours.<br/>                                              |
| [**Sous-classes\_**](swbemobject-subclasses-.md)               | Retourne une collection de sous-classes de l’objet (qui doit être une classe WMI).<br/>                |
| [**SubclassesAsync\_**](swbemobject-subclassesasync-.md)     | Retourne de façon asynchrone une collection de sous-classes de l’objet (qui doit être une classe WMI).<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemObject** possède les propriétés suivantes.



| Propriété                                                   | Type d’accès          | Description                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dérivation\_**](swbemobject-derivation-.md)<br/> | Lecture seule<br/> | Contient un tableau de chaînes qui décrit la hiérarchie de dérivation pour la classe.<br/>                                             |
| [**Méthodes\_**](swbemobject-methods-.md)<br/>       | Lecture seule<br/> | Objet [**SWbemMethodSet**](swbemmethodset.md) qui est la collection de méthodes pour cet objet.<br/>                           |
| [**D\_**](swbemobject-path-.md)<br/>             | Lecture seule<br/> | Contient un objet [**SWbemObjectPath**](swbemobjectpath.md) qui représente le chemin d’accès de l’objet de la classe ou de l’instance actuelle.<br/> |
| [**Propriétés\_**](swbemobject-properties-.md)<br/> | Lecture seule<br/> | Objet [**SWbemPropertySet**](swbempropertyset.md) qui est la collection de propriétés pour cet objet.<br/>                    |
| [**Qualificateurs\_**](swbemobject-qualifiers-.md)<br/> | Lecture seule<br/> | Objet [**SWbemQualifierSet**](swbemqualifierset.md) qui est la collection de qualificateurs pour cet objet.<br/>                  |
| [**Sécurité\_**](swbemobject-security-.md)<br/>     | Lecture seule<br/> | Contient un objet [**SWbemSecurity**](swbemsecurity.md) utilisé pour lire ou modifier les paramètres de sécurité.<br/>                         |



 

## <a name="examples"></a>Exemples

La [liste de toutes les propriétés et méthodes pour un](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) exemple de code VBScript de classe WMI dans la Galerie TechNet utilise SWbemObject pour répertorier toutes les méthodes et propriétés d’une classe WMI spécifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 


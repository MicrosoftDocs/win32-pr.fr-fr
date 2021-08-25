---
description: La \_ méthode Delete de l’objet SWbemObject supprime la classe en cours ou l’instance actuelle.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: Méthode SWbemObject.Delete_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: db8df81e56db9967db46b88c0587af9b82a6281e7e732b8647059e8bf4f5457a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857379"
---
# <a name="swbemobjectdelete_-method"></a>SWbemObject. Delete, \_ méthode

La **méthode \_ Delete** de l’objet [**SWbemObject**](swbemobject.md) supprime la classe en cours ou l’instance actuelle. Si un fournisseur dynamique fournit la classe ou l’instance, il est parfois impossible de supprimer cet objet, sauf si le fournisseur prend en charge la suppression de classe ou d’instance. Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Réservé et doit avoir la valeur 0 (zéro) si elle est spécifiée.

</dd> <dt>

*objwbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre n’est généralement pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **Delete \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Le contexte actuel ne dispose pas des droits de sécurité adéquats pour supprimer l’objet.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La classe spécifiée n’existe pas.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

Impossible de supprimer l’objet.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L’objet n’existait pas.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Remarques

La **méthode \_ Delete** échoue si une nouvelle instance de [**SWbemObject**](swbemobject.md) est créée, mais aucune valeur n’est fournie pour la propriété Key. Windows WMI (Management Instrumentation) génère automatiquement une valeur d’identificateur global unique (GUID), mais une valeur GUID n’est pas acceptée par **SWbemObject. Delete \_**. Dans ce cas, [**SWbemServices. Delete**](swbemservices-delete.md), qui utilise le chemin d’accès de l’objet, fonctionne. Notez qu’un objet [**SWbemObjectPath**](swbemobjectpath.md) est retourné par la méthode [**SWbemObject. \_ put**](swbemobject-put-.md) après qu’un objet a été validé dans WMI.

## <a name="examples"></a>Exemples

L’exemple suivant crée une nouvelle classe. Ajoute une propriété de clé ; écrit la nouvelle classe dans le référentiel ; et affiche le chemin d’accès du nouvel objet de classe. Le script génère ensuite une instance de la nouvelle classe ; l’écrit ; et affiche le chemin d’accès. Notez que le script supprime la classe et ses instances du référentiel en supprimant simplement la classe.


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



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



 

 





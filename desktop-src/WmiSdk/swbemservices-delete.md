---
description: Supprime la classe ou l’instance spécifiée dans le chemin d’accès de l’objet. Vous pouvez uniquement supprimer des objets dans l’espace de noms actuel.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: SWbemServices. Delete, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403469"
---
# <a name="swbemservicesdelete-method"></a>SWbemServices. Delete, méthode

La méthode **Delete** de l’objet [**SWbemServices**](swbemservices.md) supprime la classe ou l’instance spécifiée dans le chemin d’accès de l’objet. Vous pouvez uniquement supprimer des objets dans l’espace de noms actuel.

Si un fournisseur dynamique fournit la classe ou l’instance, vous ne pouvez pas supprimer cet objet, sauf si le fournisseur prend en charge la suppression de classe ou d’instance.

Cette méthode est appelée en mode synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatoire. Chaîne qui contient le chemin d’accès à l’objet que vous souhaitez supprimer. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Réservé. Cette valeur doit être zéro.

</dd> <dt>

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **Delete** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

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

L’objet n’existe pas.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Remarques

La méthode **SWbemServices. Delete** peut être utilisée lorsque la propriété de clé pour l’objet n’a pas de valeur, car cette méthode requiert uniquement un chemin d’accès d’objet comme entrée. Cette méthode peut être utilisée dans les situations où [**SWbemObject. \_ Delete**](swbemobject-delete-.md) échoue pour une valeur de clé manquante. Si l’objet est validé dans WMI via [**SWbemObject. put \_**](swbemobject-put-.md), un objet [**SWbemObjectPath**](swbemobjectpath.md) a été obtenu par le biais de l’appel.

## <a name="examples"></a>Exemples

L’exemple suivant crée une nouvelle classe, ajoute une propriété qui n’est pas une clé, écrit la nouvelle classe dans le référentiel et affiche le chemin d’accès du nouvel objet de classe. Le script génère ensuite une instance de la nouvelle classe, écrit l’instance et affiche le chemin d’accès. Notez que le script supprime la classe et ses instances du référentiel en supprimant la classe. Pour plus d’informations sur les classes et les instances WMI, consultez [manipulation d’informations sur les classes et les](manipulating-class-and-instance-information.md) instances et [Common Information Model](common-information-model.md).


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
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
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**M**](swbemservices.md)
</dt> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 

 





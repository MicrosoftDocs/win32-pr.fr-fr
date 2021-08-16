---
description: Récupère un objet, qui est soit une définition de classe, soit une instance, en fonction du chemin d’accès de l’objet.
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.tgt_platform: multiple
title: SWbemServices. obten, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Get
- ISWbemServices.Get
- ISWbemServices.Get
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d448d92cddf24e98f05cf023116e7087ad8cc3dcd310b7ccd3657571ee7650ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312658"
---
# <a name="swbemservicesget-method"></a>SWbemServices. obten, méthode

La **méthode d’extraction de** l’objet [**SWbemServices**](swbemservices.md) récupère un objet, qui est soit une définition de classe, soit une instance, en fonction du chemin d’accès de l’objet. Cette méthode récupère uniquement les objets de l’espace de noms associé à l’objet **SWbemServices** actif.

La méthode est appelée en mode synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObject = .Get( _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strObjectPath* \[ facultatif\]
</dt> <dd>

Chaîne qui contient le chemin d’accès de l’objet à récupérer. Si cette valeur est vide, l’objet vide retourné peut devenir une nouvelle classe. Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Entier qui détermine le comportement de la requête. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base. Pour plus d’informations sur les qualificateurs modifiés, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette méthode retourne un objet [**SWbemObject**](swbemobject.md) qui représente l’objet demandé.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode d' **extraction** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’a pas l’autorisation d’accéder à l’objet.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> <dt>

**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)
</dt> <dd>

Le chemin d’accès spécifié n’est pas valide.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L’objet demandé est introuvable.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Remarques

Contrairement aux méthodes [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) et [**InstancesOf**](swbemservices-instancesof.md) , la méthode obtenir retourne toujours un [**SWbemObject**](swbemobject.md) représentant une instance spécifique d’une ressource managée par WMI. Pour obtenir une instance spécifique d’une ressource managée WMI à l’aide de la méthode obtenir, vous devez indiquer à l’instance de récupérer l’instance en passant la méthode au chemin d’accès de l’objet, comme indiqué dans le script suivant.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " & objSWbemObject.Name        & vbCrLf & _
             "Display Name: " & objSWbemObject.DisplayName & vbCrLf & _
             "Start Mode:   " & objSWbemObject.StartMode   & vbCrLf & _
             "State:        " & objSWbemObject.State
```



Vous pouvez utiliser cette méthode pour obtenir des objets [*Singleton*](gloss-s.md) , tels que [**\_ \_ CIMOMIdentification**](--cimomidentification.md), qui contient des informations de version sur l’installation WMI en cours d’exécution.

Vous pouvez examiner le référentiel à l’aide d’un outil d’affichage tel que [CIM Studio](further-information.md) pour vérifier que la nouvelle classe et l’instance s’affichent. Pour obtenir un exemple de suppression d’une classe et d’une instance du référentiel, consultez [**SWbemServices. Delete**](swbemservices-delete.md) ou [**SWbemObject. \_ Delete**](swbemobject-delete-.md).

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

[**M**](swbemobject.md)
</dt> </dl>

 

 





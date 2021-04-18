---
description: Exécute une requête pour récupérer des objets.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cQuery (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2f3a894681bafc71de34ae7722b985494ef80b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522707"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.Exeméthode cQuery

La méthode **ExecQuery** de l’objet [**SWbemServices**](swbemservices.md) exécute une requête pour récupérer des objets. Ces objets sont disponibles par le biais de la collection [**SWbemObjectSet**](swbemobjectset.md) retournée.

Cette méthode est appelée en mode semi-synchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strQuery* 
</dt> <dd>

Obligatoire. Chaîne qui contient le texte de la requête. Ce paramètre ne peut pas être vide. Pour plus d’informations sur la création de chaînes de requête WMI, consultez [interrogation avec WQL](querying-with-wql.md) et la référence [WQL](wql-sql-for-wmi.md) .

</dd> <dt>

*strQueryLanguage* \[ facultatif\]
</dt> <dd>

Chaîne qui contient le langage de requête à utiliser. S’il est spécifié, cette valeur doit être « WQL ».

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Entier qui détermine le comportement de la requête et détermine si cet appel est retourné immédiatement. La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**. Ce paramètre peut accepter les valeurs suivantes.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Entraîne le retour d’un énumérateur avant uniquement. Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * * (0 (0x0))


</dt> <dd>

Fait en sorte que WMI conserve les pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Provoque le retour immédiat de l’appel.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Entraîne le blocage de cet appel jusqu’à ce que la requête soit terminée. Cet indicateur appelle la méthode en mode synchrone.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype * * * * (2 (0X2))


</dt> <dd>

Utilisé pour le prototypage. Cet indicateur empêche la requête de se produire et retourne un objet qui ressemble à un objet de résultat standard.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base. Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si aucune erreur ne se produit, cette méthode retourne un objet [**SWbemObjectSet**](swbemobjectset.md) . Il s’agit d’une collection d’objets qui contient le jeu de résultats de la requête. L’appelant peut examiner la collection à l’aide de l’implémentation des collections pour le langage de programmation que vous utilisez. Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **ExecQuery** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L’utilisateur actuel n’a pas l’autorisation d’afficher le jeu de résultats.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un paramètre non valide a été spécifié.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

La syntaxe de la requête n’est pas valide.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Le langage de requête demandé n’est pas pris en charge.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Mémoire insuffisante pour terminer l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

**ExecQuery** est l’un des appels les plus couramment utilisés pour récupérer des informations WMI. Un appel standard à **ExecQuery** ressemble à ce qui suit :


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



Notez que vous créez l’objet [**SWbemServices**](swbemservices.md) avec un moniker qui représente l’espace de noms et la sécurité appropriés, puis effectuez l’appel **ExecQuery** par le biais du service. Pour une description plus complète, consultez [création d’un script WMI](creating-a-wmi-script.md) et [énumération de WMI](enumerating-wmi.md).

À l’instar de la méthode [**InstancesOf**](swbemservices-instancesof.md) , la méthode **ExecQuery** retourne toujours une collection [**SWbemObjectSet**](swbemobjectset.md) . Par conséquent, votre script WMI doit énumérer la collection ExecQuery retourne afin d’accéder à chaque instance de ressource gérée dans la collection, comme illustré ici :


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Les autres méthodes [**SWbemServices**](swbemservices.md) qui retournent une [**SWbemObjectSet**](swbemobjectset.md) incluent [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md)et [**SubclassesOf**](swbemservices-subclassesof.md).

La requête ne peut pas retourner un jeu de résultats vide. La méthode **ExecQuery** retourne des propriétés de clé, que la propriété de clé soit demandée ou non dans l’argument *strQuery* . Si une erreur se produit lors de l’exécution de cette méthode et que vous n’utilisez pas l’indicateur **wbemFlagReturnImmediately** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) n’est pas défini tant que vous n’avez pas essayé d’accéder au jeu d’objets retourné. Toutefois, si vous utilisez l’indicateur **wbemFlagReturnWhenComplete** , l’objet Err est défini lorsque la méthode **ExecQuery** est appelée.

Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL. Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de **\_ \_ \_ violation de quota E WBEM** en tant que valeur **HRESULT** . La limite des mots clés WQL dépend de la complexité de la requête.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant localise tous les lecteurs de disque sur l’ordinateur local et affiche l’ID de l’appareil et le type du lecteur de disque.


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
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

[**SWbemServices.**](swbemservices-get.md)
</dt> <dt>

[Interrogation avec WQL](querying-with-wql.md)
</dt> <dt>

[Création d’un script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Énumération de WMI](enumerating-wmi.md)
</dt> </dl>

 


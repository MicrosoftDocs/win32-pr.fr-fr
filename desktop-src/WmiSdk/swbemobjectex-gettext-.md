---
description: Retourne une représentation XML d’un objet ou d’une instance. Le fichier texte est mis en forme au format XML spécifié comme indiqué dans WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Méthode SWbemObjectEx.GetText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2f5772429fa0cd7f2f45009ff1867141a845088b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885490"
---
# <a name="swbemobjectexgettext_-method"></a>SWbemObjectEx. GetText, \_ méthode

La **méthode \_ gettext** de l’objet [**SWBEMOBJECTEX**](swbemobjectex.md) retourne une représentation XML d’un objet ou d’une instance. Le fichier texte est mis en forme au format XML spécifié comme indiqué dans [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iTextFormat* \[ dans\]
</dt> <dd>

Obligatoire. Valeur de [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) qui spécifie le format XML obtenu.

</dd> <dt>

*IFlags* \[ dans, facultatif\]
</dt> <dd>

Indicateurs d’opération réservée. La valeur par défaut est 0 (zéro).

</dd> <dt>

*objWbemNamedValueSet* \[ dans, facultatif\]
</dt> <dd>

Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui définit le contexte de l’opération. La valeur par défaut est null. Pour plus d’informations sur les paires nom/valeur autorisées, consultez la section Notes ci-dessous.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode n’a pas de valeur de retour.

## <a name="error-codes"></a>Codes d’erreur

Une fois la méthode **gettext \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

Le format demandé est introuvable.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un des paramètres de l'appel n'est pas correct.

</dd> <dt>

**wbemErrCriticalError** -2147749898 (0x8004100A)
</dt> <dd>

Une erreur interne, critique et inattendue est survenue. Signalez cette erreur au Support technique Microsoft.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lors de la construction de votre [**SWbemNamedValueSet**](swbemnamedvalueset.md), seules les paires nom/valeur suivantes sont autorisées.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Valeur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LocalOnly</td>
<td><strong>VT_BOOL</strong><br/> Si la <strong>valeur est true</strong>, seules les propriétés et les méthodes définies localement sont présentes dans le XML résultant. La valeur par défaut est <strong>false</strong>.<br/></td>
</tr>
<tr class="even">
<td>IncludeQualifiers</td>
<td><strong>VT_BOOL</strong><br/> Si la <strong>valeur est true</strong>, les qualificateurs des classes, instances, propriétés et méthodes sont inclus dans le XML résultant. La valeur par défaut est <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td>PathLevel</td>
<td><strong>VT-I4</strong><br/> La valeur par défaut est 0 (zéro). Les valeurs possibles sont les suivantes :<br/>
<ul>
<li>0 : une &lt; classe &gt; ou un <INSTANCE> élément est créé selon que l’objet est une classe ou une instance.</li>
<li>1 : un <VALUE.NAMEDOBJECT> élément est généré.</li>
<li>2 : un <VALUE.OBJECTWITHLOCALPATH> élément est généré.</li>
<li>3 : un <VALUE.OBJECTWITHPATH> élément est généré.</li>
</ul></td>
</tr>
<tr class="even">
<td>ExcludeSystemProperties</td>
<td><strong>VT-BOOL</strong><br/> Si la <strong>valeur est true</strong>, les propriétés système, comme __NAMESPACE, sont exclues de la sortie.<br/></td>
</tr>
<tr class="odd">
<td>IncludeClassOrigin</td>
<td><strong>VT_BOOL</strong><br/> Si la <strong>valeur est true</strong>, l’attribut Origin de la classe est défini sur les <PROPERTY> éléments et <METHOD> . La valeur par défaut est <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

Pour plus d’informations sur la création d’un [**SWbemNamedValueSet**](swbemnamedvalueset.md), consultez [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md).

## <a name="examples"></a>Exemples

Le script suivant montre comment obtenir une représentation XML de la définition de classe [**\_ BIOS Win32**](/windows/desktop/CIMWin32Prov/win32-bios) . En spécifiant une instance particulière **du \_ BIOS Win32**, vous pouvez obtenir les données de cet objet en XML.


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



 


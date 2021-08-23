---
description: Un objet SWbemNamedValueSet est une collection d’objets SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Objet SWbemNamedValueSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdcc3ba2bde6dfdfd0cc732e4376ceb69ba60904f4d787d9030299c248ebb62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732669"
---
# <a name="swbemnamedvalueset-object"></a>Objet SWbemNamedValueSet

Un objet **SWbemNamedValueSet** est une collection d’objets [**SWbemNamedValue**](swbemnamedvalue.md) . Les méthodes et les propriétés de **SWbemNamedValueSet** sont principalement utilisées pour envoyer des informations supplémentaires aux fournisseurs lors de l’envoi de certains appels à WMI. Tous les appels dans [**SWbemServices**](swbemservices.md)et certains appels dans [**SWbemObject**](swbemobject.md)prennent un paramètre facultatif qui est un objet de ce type. Un client peut ajouter des informations à un objet **SWbemNamedValueSet** et envoyer l’objet **SWbemNamedValueSet** avec l’appel comme l’un des paramètres. Cet objet peut être créé par l’appel VBScript **CreateObject** .

Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).

> [!Note]  
> Important-si possible, n’utilisez pas ce mécanisme, car il peut rompre le modèle d’accès uniforme qui est la base de WMI. Si un fournisseur utilise ce mécanisme, il est important que ce mécanisme soit utilisé aussi avec modération que possible. Si un fournisseur a besoin d’une grande quantité d’informations de contexte hautement spécifiques pour répondre à une demande, tous les clients doivent être codés pour fournir ces informations. Ce mécanisme vous permet d’accéder à de tels fournisseurs, si nécessaire.

 

Un objet **SWbemNamedValueSet** est une collection d’éléments [**SWbemNamedValue**](swbemnamedvalue.md) . Ces éléments sont ajoutés à la collection à l’aide de la méthode [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) . Elles sont supprimées à l’aide de la méthode [**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md) et récupérées à l’aide de la méthode [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Vous pouvez accéder aux méthodes pour remplir toutes les informations de contexte requises par un fournisseur dynamique. Après avoir appelé l’une des méthodes [**SWbemServices**](swbemservices.md) , vous pouvez réutiliser l’objet **SWbemNamedValueSet** pour un autre appel.

Le fournisseur sous-jacent détermine les informations contenues dans un objet **SWbemNamedValueSet** . WMI n’utilise pas les informations, mais les transfère simplement au fournisseur. Les fournisseurs doivent publier les informations de contexte dont ils ont besoin pour traiter les demandes.

## <a name="members"></a>Membres

L’objet **SWbemNamedValueSet** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemNamedValueSet** a ces méthodes.



| Méthode                                            | Description                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Complémentaires**](swbemnamedvalueset-add.md)             | Ajoute un objet [**SWbemNamedValue**](swbemnamedvalue.md) à la collection.<br/>                                                  |
| [**Répliqué**](swbemnamedvalueset-clone.md)         | Effectue une copie de cette collection **SWbemNamedValueSet** .<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | Supprime tous les éléments de la collection, ce qui rend l’objet **SWbemNamedValueSet** vide.<br/>                                        |
| [**Élément**](swbemnamedvalueset-item.md)           | Récupère un objet [**SWbemNamedValue**](swbemnamedvalue.md) de la collection. Il s’agit de la méthode par défaut de l’objet.<br/> |
| [**Installez**](swbemnamedvalueset-remove.md)       | Supprime un objet [**SWbemNamedValue**](swbemnamedvalue.md) de la collection.<br/>                                             |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemNamedValueSet** a ces propriétés.



| Propriété                                             | Type d’accès          | Description                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Count**](swbemnamedvalueset-count.md)<br/> | Lecture seule<br/> | Nombre d’éléments dans la collection<br/> |



 

## <a name="examples"></a>Exemples

L’exemple VBScript suivant illustre la manipulation des jeux de valeurs nommées, dans le cas où la valeur nommée est un type tableau.


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



L’exemple perl suivant illustre la manipulation des jeux de valeurs nommées, dans le cas où la valeur nommée est un type tableau.


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 





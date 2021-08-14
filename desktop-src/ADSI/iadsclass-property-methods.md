---
title: Méthodes de propriété IADsClass (IADs. h)
description: Les méthodes de propriété de l’interface IADsClass obtiennent ou définissent les propriétés suivantes. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsClass ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8640c6a1d1f12ef959530b72618a503245992fae791dce4e6b9e9aec05bcb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428298"
---
# <a name="iadsclass-property-methods"></a>Méthodes de propriété IADsClass

Les méthodes de propriété de l’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) obtiennent ou définissent les propriétés suivantes. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**Résumé**
</dt> <dd> <dl>

Valeur booléenne qui indique si cette classe est abstraite ou non abstraite. Lorsque la **valeur est true**, cette classe est une classe abstraite qui ne peut pas être instanciée directement dans le service d’annuaire. Les classes abstraites ne peuvent être utilisées qu’en tant que Super classes.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **booléen**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**AuxDerivedFrom**
</dt> <dd> <dl>

Tableau de chaînes ADsPath qui indiquent les classes Super auxiliaires dont cette classe dérive.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Appoint**
</dt> <dd> <dl>

Valeur booléenne qui indique si cette classe est auxiliaire ou non. Lorsque la **valeur est true**, cette classe est une classe auxiliaire et ne peut pas être instanciée directement dans le service d’annuaire. Les classes auxiliaires ne peuvent être utilisées qu’en tant que Super classes d’autres classes auxiliaires ou en tant que source de propriétés supplémentaires sur les classes structurelles.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **booléen**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**IDENTIFICATEUR**
</dt> <dd> <dl>

CLSID spécifique au fournisseur facultatif identifiant l’objet COM qui implémente cette classe.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**Conteneur**
</dt> <dd> <dl>

Valeur booléenne qui indique si cette classe peut être un conteneur d’autres classes d’objets. Si cette valeur est **true**, vous pouvez appeler la méthode d' **extraction de \_ conteneur** pour récupérer un tableau des classes d’objets que cette classe peut contenir.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **booléen**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**Containment**
</dt> <dd> <dl>

Tableau **BSTR** dans lequel chaque élément est le nom d’une classe d’objet que cette classe peut contenir.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**DerivedFrom**
</dt> <dd> <dl>

Tableau de chaînes ADsPath qui indiquent les classes à partir desquelles cette classe a été dérivée.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**HelpFileContext**
</dt> <dd> <dl>

ID de contexte dans **HelpFileName** où se trouvent des informations spécifiques pour cette classe.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**HelpFileName**
</dt> <dd> <dl>

Nom d’un fichier d’aide qui contient plus d’informations sur les objets de cette classe.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**MandatoryProperties**
</dt> <dd> <dl>

**SAFEARRAY** de **Variant** s qui répertorie les propriétés qui doivent être définies pour que cette classe soit écrite dans le stockage. Si la classe ne contient qu’une seule propriété, l’opération **obtenir \_ MandatoryProperties** retourne un **BSTR**.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**NamingProperties**
</dt> <dd> <dl>

**SAFEARRAY** de **BSTR** qui répertorie les propriétés utilisées pour nommer les attributs de cette classe de schéma.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**OID**
</dt> <dd> <dl>

Identificateur d’objet spécifique au fournisseur qui définit cette classe. Cela est fourni pour autoriser l’extension de schéma, à l’aide de Active Directory, dans les services d’annuaire qui requièrent des OID spécifiques au fournisseur pour les classes.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**(OptionalProperties)**
</dt> <dd> <dl>

**SAFEARRAY** de **Variant** s qui répertorie les propriétés facultatives de cette classe de schéma. Si la classe ne contient qu’une seule propriété, l’opération **obtenir \_ (OptionalProperties)** retourne un **BSTR**.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**PossibleSuperiors**
</dt> <dd> <dl>

Tableau de chaînes ADsPath qui indiquent les classes de schéma qui peuvent contenir des instances de cette classe.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**PrimaryInterface**
</dt> <dd> <dl>

GUID d’identificateur spécifique au fournisseur facultatif qui associe une interface aux objets de cette classe de schéma. Par exemple, la classe « User » qui prend en charge [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) et **PrimaryInterface** est identifiée par l' **IID \_ IADsUser**. Ce doit être au format de chaîne standard d’un GUID, tel que défini par COM. Ce GUID est la valeur qui apparaît dans la propriété [**IADs :: obtenir \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) dans les instances de cette classe pour les fournisseurs qui implémentent cette propriété. L’identification d’une classe de schéma par l’IID de l’interface principale du code de la classe permet d’utiliser **QueryInterface** au moment de l’exécution pour déterminer si un objet est de la classe souhaitée.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment utiliser l’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) pour déterminer si un objet peut être un conteneur et, le cas échéant, répertorie les noms de tous les objets qu’il contient.


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



L’exemple de code suivant montre comment utiliser l’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) pour déterminer si un objet peut être un conteneur et, le cas échéant, répertorie les noms de tous les objets qu’il contient.


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsClass est défini en tant que C8F93DD0-4AE0-11CF-9E73-00AA004A5691<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsClass :: qualificateurs**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 






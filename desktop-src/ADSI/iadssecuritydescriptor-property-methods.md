---
title: Méthodes de propriété IADsSecurityDescriptor (IADs. h)
description: Les méthodes de propriété de l’interface IADsSecurityDescriptor obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsSecurityDescriptor ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103497"
---
# <a name="iadssecuritydescriptor-property-methods"></a>Méthodes de propriété IADsSecurityDescriptor

Les méthodes de propriété de l’interface [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtiennent ou définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**Contrôle**
</dt> <dd> <dl>

Indicateurs qui qualifient la signification du descripteur de sécurité. Les valeurs sont extraites de la structure de [**\_ \_ contrôle du descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) Win32.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

**DaclDefaulted**
</dt> <dd> <dl>

Indicateur du type BOOL qui indique si la liste DACL est dérivée d’un mécanisme par défaut, plutôt que d’être fournie explicitement par le fournisseur d’origine du descripteur de sécurité. Par exemple, si le créateur d’un objet ne spécifie pas de liste DACL, l’objet reçoit la DACL par défaut à partir du jeton d’accès du créateur. Cet indicateur peut affecter la façon dont le système traite la liste DACL, en ce qui concerne l’héritage de l’entrée du contrôle d’accès. Le système ignore cet indicateur si l' \_ indicateur de \_ présence DACL se présente n’est pas défini.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**DiscretionaryAcl**
</dt> <dd> <dl>

Liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) qui spécifie les types d’accès accordés à l’objet pour les utilisateurs et les groupes spécifiés. Pour plus d’informations sur les DACL, consultez [DACL null et listes DACL vides](/windows/desktop/AD/null-dacls-and-empty-dacls).

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

**Groupe**
</dt> <dd> <dl>

Groupe auquel appartient l’ID de sécurité du propriétaire.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

**GroupDefaulted**
</dt> <dd> <dl>

Indicateur du type BOOL qui indique si les données de groupe sont dérivées d’un mécanisme par défaut, plutôt que d’être explicitement fournies par le fournisseur d’origine du descripteur de sécurité.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

**Propriétaire**
</dt> <dd> <dl>

Propriétaire de l’objet.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

**OwnerDefaulted**
</dt> <dd> <dl>

Indicateur du type BOOL qui indique que les données de propriétaire sont dérivées d’un mécanisme par défaut, plutôt que d’être explicitement fournies par le fournisseur d’origine du descripteur de sécurité.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

**Faisant**
</dt> <dd> <dl>

Niveau de révision du descripteur de sécurité. Cette valeur est extraite de la structure des [**\_ \_ informations de révision**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) de la liste de contrôle d’accès Win32. Toutes les entrées du contrôle d’accès d’une liste de contrôle d’accès doivent être au même niveau de révision.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

**SaclDefaulted**
</dt> <dd> <dl>

Indicateur du type BOOL qui indique que la liste SACL est dérivée d’un mécanisme par défaut, plutôt que d’être explicitement fournie par le fournisseur d’origine du descripteur de sécurité. Cet indicateur peut affecter la façon dont le système gère la liste SACL, en ce qui concerne l’héritage de l’entrée du contrôle d’accès. Le système ignore cet indicateur si l' \_ indicateur de \_ présence SACL se présente n’est pas défini.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**SystemAcl**
</dt> <dd> <dl>

Liste de contrôle d’accès système utilisée pour générer des enregistrements d’audit pour l’objet.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment énumérer un descripteur de sécurité existant.


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsSecurityDescriptor est défini en tant que B8C787CA-9BDD-11D0-852C-00C04FD8D503<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 


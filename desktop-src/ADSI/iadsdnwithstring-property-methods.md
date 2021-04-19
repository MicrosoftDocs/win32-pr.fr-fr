---
title: Méthodes de propriété IADsDNWithString (IADs. h)
description: La méthode Property de l’interface IADsDNWithString définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsDNWithString ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512824"
---
# <a name="iadsdnwithstring-property-methods"></a>Méthodes de propriété IADsDNWithString

La méthode Property de l’interface [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**DNString**
</dt> <dd> <dl>

Chaîne DN associée à une valeur de chaîne.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

**StringValue**
</dt> <dd> <dl>

Valeur de chaîne associée à un DN d’un objet.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsDNWithString est défini en tant que 370DF02E-F934-11D2-BA96-00C04FB6D0D1<br/>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[**\_DN ADS \_ avec \_ chaîne**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 






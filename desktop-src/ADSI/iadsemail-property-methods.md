---
title: Méthodes de propriété IADsEmail (IADs. h)
description: La méthode Property de l’interface IADsEmail définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsEmail ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b857eab4fee357b67f796a6289a62e887f9c12a5579c233144a39f935d5ed35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691593"
---
# <a name="iadsemail-property-methods"></a>Méthodes de propriété IADsEmail

La méthode Property de l’interface [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**Adresse**
</dt> <dd> <dl>

Adresse e-mail de l’utilisateur.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

**Type**
</dt> <dd> <dl>

Type du message électronique.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
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
| IID<br/>                      | IID \_ IADsEmail est défini en tant que 97AF011A-478E-11D1-A3B4-00C04FB950DC<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[**\_E-mail ads**](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 






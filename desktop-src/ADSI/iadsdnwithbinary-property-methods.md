---
title: Méthodes de propriété IADsDNWithBinary (IADs. h)
description: La méthode Property de l’interface IADsDNWithBinary définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsDNWithBinary ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ab9fb355f2602d290c064f6636a13375ea92fdfbf0d6d47c1c6cf8d61e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023497"
---
# <a name="iadsdnwithbinary-property-methods"></a>Méthodes de propriété IADsDNWithBinary

La méthode Property de l’interface [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**BinaryValue**
</dt> <dd> <dl>

GUID d’un objet associé à un DN.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

**DNString**
</dt> <dd> <dl>

Chaîne DN associée au GUID d’un objet.

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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsDNWithBinary est défini en tant que 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1<br/>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[**\_DN ADS \_ avec \_ binaire**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 






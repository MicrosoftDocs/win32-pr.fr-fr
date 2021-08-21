---
title: Méthodes de propriété IADsPostalAddress (IADs. h)
description: La méthode Property de l’interface IADsPostalAddress définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPostalAddress ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd01887751a4389984a4bc765d924d6c8a8e81dd9a65be3b7a868a3cbb845cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691126"
---
# <a name="iadspostaladdress-property-methods"></a>Méthodes de propriété IADsPostalAddress

La méthode Property de l’interface [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**PostalAddress**
</dt> <dd> <dl>

Tableau de six chaînes contenant l’adresse postale de l’utilisateur.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
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
| IID<br/>                      | IID \_ IADsPostalAddress est défini en tant que 7ADECF29-4680-11D1-A3B4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[**\_POSTALADDRESS ads**](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 






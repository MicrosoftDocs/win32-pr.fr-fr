---
title: Méthodes de propriété IADsOctetList (IADs. h)
description: La méthode Property de l’interface IADsOctetList définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsOctetList ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa434eaf9cde95adb4b43d0261ac779d5183d9f3de2284704bc75cfa564521e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023437"
---
# <a name="iadsoctetlist-property-methods"></a>Méthodes de propriété IADsOctetList

La méthode Property de l’interface [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**OctetList**
</dt> <dd> <dl>

Séquence ordonnée de tableaux d’octets.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **variante**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
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
| IID<br/>                      | IID \_ IADsOctetList est défini en tant que 7B28B80F-4680-11D1-A3B4-00C04FB950DC<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[**\_liste des octets ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 






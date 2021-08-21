---
title: Méthodes de propriété IADsBackLink (IADs. h)
description: La méthode Property de l’interface IADsBackLink définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsBackLink ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2834ac74faa78418abfe1d960e4355aa6fa0c14999783ad9dfa47389f38eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691594"
---
# <a name="iadsbacklink-property-methods"></a>Méthodes de propriété IADsBackLink

La méthode Property de l’interface [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) définit la propriété décrite dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**ObjectName**
</dt> <dd> <dl>

Nom d’un objet auquel l’attribut de **lien précédent** est attaché.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

**RemoteID**
</dt> <dd> <dl>

Identificateur du serveur distant qui requiert une référence externe de l’objet spécifié par **ObjectName**.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
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
| IID<br/>                      | IID \_ IADsBackLink est défini en tant que FD1302BD-4080-11D1-A3AC-00C04FB950DC<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[**\_lien secondaire ads**](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 






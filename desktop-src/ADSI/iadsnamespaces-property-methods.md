---
title: Méthodes de propriété IADsNamespaces (IADs. h)
description: Les méthodes de propriété de l’interface IADsNamespaces obtiennent et définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsNamespaces ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742693"
---
# <a name="iadsnamespaces-property-methods"></a>Méthodes de propriété IADsNamespaces

Les méthodes de propriété de l’interface [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) obtiennent et définissent les propriétés décrites dans le tableau suivant. Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

La propriété **DefaultContainer** identifie un objet conteneur de base auquel vous pouvez lier et utiliser comme point de départ lors de la navigation. Ces données sont stockées et récupérées à partir de la valeur de Registre suivante.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI définit la propriété **DefaultContainer** pour fournir un moyen rapide d’obtenir un pointeur vers un objet conteneur ADSI précédemment défini.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Notes

Les fournisseurs doivent fournir cette propriété pour chaque utilisateur. Le conteneur par défaut est défini immédiatement après l’appel de **IADsNamespaces ::p ut \_ DefaultContainer**. L’appel de [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) n’est pas requis. En fait, l’objet espaces de noms fourni par le système renvoie **E \_ NOTIMPL** pour la méthode **IADs. setinfo** appelée sur cet objet. Lorsqu’un conteneur est l’objet Namespaces, une opération d’énumération produit toujours une liste d’objets d’espace de noms spécifiques au fournisseur. Quand [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) est utilisé pour obtenir un objet Namespace, le paramètre *bstrClass* est ignoré. Cela est dû au fait que le conteneur, autrement dit, l’objet Namespaces, contient un seul type d’objet, à savoir les objets d’espace de noms spécifiques au fournisseur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNamespaces est défini en tant que 28B96BA0-B330-11CF-A9AD-00AA006BC149<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Méthodes de propriété d’interface](interface-property-methods.md)
</dt> </dl>

 

 






---
title: Types de modification des attributs ADSI (IADs. h)
description: Utilisé avec le membre dwControlCode de la \_ \_ structure info attr ADS pour spécifier le type d’opération à effectuer lorsqu’un attribut est modifié à l’aide de la méthode IDirectoryObject SetObjectAttributes.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- types de modification d’attribut ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d057f1a67fb6e18be0b0ed7e3fc21e1276a4068017c44c4e28d125fe271046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181145"
---
# <a name="adsi-attribute-modification-types"></a>Types de modification des attributs ADSI

Les constantes suivantes sont utilisées avec le membre **dwControlCode** de la structure [**\_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) pour spécifier le type d’opération à effectuer lorsqu’un attribut est modifié à l’aide de la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Pour plus d’informations sur l’utilisation de ces valeurs, consultez [modification des attributs avec ADSI](modifying-attributes-with-adsi.md).

<dl> <dt>

<span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_attr- \_ effacer les annonces**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Entraîne la suppression de toutes les valeurs d’attribut d’un objet.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_ \_ mise à jour de l’attr ads**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Entraîne la mise à jour des valeurs d’attribut spécifiées.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_Ajout d’attr ADS \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Entraîne l’ajout des valeurs d’attribut spécifiées aux valeurs d’attribut existantes.


</dt> </dl> </dd> <dt>

<span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**suppression de l' \_ attr ADS \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Entraîne la suppression des valeurs d’attribut spécifiées d’un objet.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Ces constantes sont destinées à être utilisées avec la [**structure \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) dans la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Ces constantes ne doivent pas être confondues avec les membres de l’énumération enum de l' [**\_ opération de propriété \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , qui sont destinés à être utilisés avec la méthode [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_infos attr \_ ads**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[Modification d’attributs avec ADSI](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 






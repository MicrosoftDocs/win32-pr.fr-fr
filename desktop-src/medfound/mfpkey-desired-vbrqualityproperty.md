---
description: Spécifie le niveau de qualité souhaité pour l’encodage de flux audio (VBR) basé sur la qualité (1 passe).
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227513"
---
# <a name="mfpkey_desired_vbrquality-property"></a>MFPKEY \_ \_ propriété VBRQUALITY souhaitée

Spécifie le niveau de qualité souhaité pour l’encodage de flux audio (VBR) basé sur la qualité (1 passe).

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Cette valeur peut être comprise entre 0 et 100, où 100 correspond à la qualité maximale. La valeur 0 indique que la méthode d’encodage VBR basé sur la qualité ne doit pas être utilisée.

Pour énumérer les modes VBR qui répondent à un certain besoin de qualité, définissez les propriétés suivantes de l’encodeur.

-   Affectez à [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la **\_ valeur variant true**.
-   Affectez à [**MFPKEY la \_ contrainte \_ énumérée \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) la **\_ valeur variant true**.
-   Définissez **MFPKEY \_ \_ VBRQUALITY souhaité** sur la qualité souhaitée. Pour les modes sans perte, définissez la qualité souhaitée sur 100.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 

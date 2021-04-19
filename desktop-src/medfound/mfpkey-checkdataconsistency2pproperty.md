---
description: Spécifie si l’encodeur doit vérifier la cohérence des données entre les passes lors de l’exécution du codage VBR en deux passes. Lecture-écriture.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525349"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>MFPKEY \_ propriété CHECKDATACONSISTENCY2P

Spécifie si l’encodeur doit vérifier la cohérence des données entre les passes lors de l’exécution du codage VBR en deux passes. Lecture-écriture.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ true**

## <a name="remarks"></a>Notes

Si vous laissez cette propriété à sa valeur par défaut **Variant \_ true**, l’encodeur vérifie que les exemples d’entrée correspondent entre les deux passes et échoue s’il détecte une incohérence. Le scénario principal qui provoque une incohérence est lorsque l’entrée provient d’un appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista ou Windows 7<br/>                                                   |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 

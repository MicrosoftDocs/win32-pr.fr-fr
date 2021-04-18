---
title: DRM_SAPLEVEL (déconseillée)
description: Spécifie le niveau de chemin d’accès audio sécurisé (SAP) pris en charge par votre application.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- Format Windows Media DRM_SAPLEVEL (obsolète)
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522771"
---
# <a name="drm_saplevel-deprecated"></a>\_SAPLEVEL DRM (déconseillé)

\[**DRM \_ SAPLEVEL** n’est plus disponible pour une utilisation à partir de Windows Vista. Au lieu de cela, utilisez PUMA (Protected user mode audio) dans la bibliothèque Media Foundation. \]

La propriété **DRM \_ SAPLEVEL** spécifie le niveau de chemin d’accès audio sécurisé (SAP) pris en charge par votre application.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ SAPLEVEL

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Il s’agit d’une propriété en écriture seule qui est définie en appelant [**IWMDRMReader :: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty). La valeur est une représentation sous forme de chaîne de caractères larges du niveau SAP, telle que L "200". Les valeurs actuellement prises en charge sont 200 et 300.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|--------------------------------|
| Fin de la prise en charge des clients<br/> | Windows XP<br/>          |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 






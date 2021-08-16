---
title: Structure WMDM_PROP_CONFIG
description: La \_ structure WMDM prop \_ config décrit un ensemble de valeurs de propriété compatibles sur toutes les propriétés prises en charge par l’appareil pour un format particulier. Cette structure contient un certain nombre de descriptions de propriété dans un tableau \_ de \_ structures WMDM prop DESC.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- Structure de WMDM_PROP_CONFIG Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e50cd18f5b7646934a6add71674f93ebaae700ab39e57f833e555ea3688ecb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862819"
---
# <a name="wmdm_prop_config-structure"></a>Structure de configuration de WMDM \_ prop \_

La structure **WMDM \_ prop \_ config** décrit un ensemble de valeurs de propriété compatibles sur toutes les propriétés prises en charge par l’appareil pour un format particulier. Cette structure contient un certain nombre de descriptions de propriété dans un tableau de structures [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a>Membres

<dl> <dt>

**nPreference**
</dt> <dd>

Niveau de préférence de l’appareil pour cette configuration. La valeur la plus faible indique la configuration la plus préférée.

</dd> <dt>

**nPropDesc**
</dt> <dd>

Nombre de descriptions de propriétés contenues dans cette configuration. Il existe une seule Description de propriété pour chaque propriété prise en charge pour le format spécifié.

</dd> <dt>

**pPropDesc**
</dt> <dd>

Pointeur vers un tableau de structures [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) contenant des descriptions de propriété. La taille du tableau est égale à la valeur de **nPropDesc**. L’application doit libérer cette mémoire lorsqu’elle est terminée.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure de [**\_ \_ capacité de format WMDM**](wmdm-format-capability.md) retournée par [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) pour un format particulier est constituée d’un certain nombre de configurations de propriétés. **WMDM \_ Les \_** structures de configuration prop décrivent ces configurations.

Une configuration de propriété décrit des valeurs pour toutes les propriétés prises en charge pour un format donné. Les valeurs de différentes propriétés dans une configuration unique sont compatibles les unes avec les autres. Par exemple, pour un fichier audio, une configuration inclut des valeurs valides de taux d’échantillonnage et des valeurs valides de la vitesse de transmission, de telle sorte que toutes les combinaisons de ces taux d’échantillonnage et de bits peuvent être lues sur l’appareil.

L’appelant est tenu de libérer la mémoire utilisée par **pPropDesc**. Pour obtenir un exemple de la procédure à suivre, consultez [**WMDM \_ format \_ Capability**](wmdm-format-capability.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ formulaire valeurs valides \_ de l’énumération WMDM \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_fonction de format WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ énumération des valeurs prop WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**plage de valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 






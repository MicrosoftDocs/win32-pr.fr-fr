---
description: Spécifie une représentation numérique du compromis entre le lissage de mouvement et la qualité d’image de la sortie de codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 177ae5e9d1c8a9aba359000e04483c8e45c44f823c9db924155dd5ef3d5989a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954259"
---
# <a name="mfpkey_crisp-property"></a>\_Propriété Crisp MFPKEY

Spécifie une représentation numérique du compromis entre le lissage de mouvement et la qualité d’image de la sortie de codec.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCCrisp g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

75

## <a name="remarks"></a>Remarques

Cette valeur entière peut être comprise entre 0 et 100. Plus la valeur est élevée, plus le codec optimise l’encodage pour la qualité d’image des trames individuelles, ce qui réduit généralement le lissage des mouvements.

Cette propriété doit être définie uniquement pour l’encodage CBR (constante-bit-rate). Les optimisations pour l’encodage VBR (variable-bit-rate) fonctionnent différemment.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





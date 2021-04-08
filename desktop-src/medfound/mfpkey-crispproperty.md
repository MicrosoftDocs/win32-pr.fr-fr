---
description: Spécifie une représentation numérique du compromis entre le lissage de mouvement et la qualité d’image de la sortie de codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755485"
---
# <a name="mfpkey_crisp-property"></a>\_Propriété Crisp MFPKEY

Spécifie une représentation numérique du compromis entre le lissage de mouvement et la qualité d’image de la sortie de codec.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCCrisp g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

75

## <a name="remarks"></a>Notes

Cette valeur entière peut être comprise entre 0 et 100. Plus la valeur est élevée, plus le codec optimise l’encodage pour la qualité d’image des trames individuelles, ce qui réduit généralement le lissage des mouvements.

Cette propriété doit être définie uniquement pour l’encodage CBR (constante-bit-rate). Les optimisations pour l’encodage VBR (variable-bit-rate) fonctionnent différemment.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





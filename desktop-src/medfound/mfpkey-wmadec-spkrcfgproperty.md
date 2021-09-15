---
description: Spécifie la configuration de l’orateur sur l’ordinateur client.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: MFPKEY_WMADEC_SPKRCFG, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412906"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>MFPKEY \_ WMADEC \_ SPKRCFG, propriété

Spécifie la configuration de l’orateur sur l’ordinateur client.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACSpeakerConfig g

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="default-value"></a>Valeur par défaut

Aucune configuration d’orateur spécifique n’est utilisée.

## <a name="remarks"></a>Notes

Vous devez définir cette valeur sur l’une des constantes ou valeurs indiquées dans le tableau suivant. Les constantes sont définies dans Microsoft DirectSound et sont répertoriées ici pour des raisons pratiques. Pour résoudre ces noms de constantes pour votre compilateur, vous devez inclure dsound. h.



| Constante             | Valeur      | Description                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | L’audio est transmis directement, sans être configuré pour les intervenants. |
| \_casque DSSPEAKER | 0x00000001 | L’ordinateur client est équipé d’un casque.                             |
| \_mono DSSPEAKER      | 0x00000002 | L’ordinateur client est équipé d’un orateur monoaural.                    |
| DSSPEAKER \_ Quad      | 0x00000003 | L’ordinateur client est équipé de haut-parleurs Quadraphonic.                  |
| \_stéréo DSSPEAKER    | 0x00000004 | L’ordinateur client est équipé de haut-parleurs stéréo.                        |
| DSSPEAKER \_ surround  | 0x00000005 | L’ordinateur client est équipé de haut-parleurs Surround audio à quatre canaux.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | L’ordinateur client est équipé de cinq enceintes et d’un caisson de basses.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | L’ordinateur client est équipé de sept haut-parleurs et d’un caisson de basses.         |



 

La valeur définie pour cette propriété détermine les formats de sortie énumérés par le codec pour l’audio multicanal.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





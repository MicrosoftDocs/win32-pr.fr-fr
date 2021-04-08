---
description: Spécifie le profil de complexité du contenu encodé.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: MFPKEY_DECODERCOMPLEXITYPROFILE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864174"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>MFPKEY \_ propriété DECODERCOMPLEXITYPROFILE

Spécifie le profil de complexité du contenu encodé.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCDecoderComplexityProfile g

## <a name="data-type"></a>Type de données

**VT \_ BSTR**

## <a name="remarks"></a>Notes

Vous ne pouvez lire cette valeur qu’une fois l’encodage terminé.

Pour l’audio, cette propriété a l’une des valeurs suivantes.



| Valeur | Description                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| Ko  | Encodage standard avec un taux d’échantillonnage de 44,1 KHz et un taux binaire maximal de 161 Kbits/s.         |
| NIV  | Encodage standard avec des taux d’échantillonnage allant jusqu’à 48 KHz et une vitesse de transmission maximale de 161 Kbits/s.         |
| Mémoire  | Encodage standard avec des taux d’échantillonnage allant jusqu’à 48 KHz et une vitesse de transmission maximale de 385 Kbits/s.         |
| "M0a" | Encodage professionnel avec des taux d’échantillonnage allant jusqu’à 48 KHz et des vitesses de bit comprises entre 48 et 192 kbit/s.  |
| "M0b" | Codage professionnel avec des taux d’échantillonnage allant jusqu’à 48 KHz et un débit maximal de 192 Kbits/s.      |
| M1  | Codage professionnel avec des taux d’échantillonnage allant jusqu’à 48 KHz et un débit maximal de 384 Kbits/s.      |
| Carré  | Codage professionnel avec des taux d’échantillonnage allant jusqu’à 96 KHz et un débit maximal de 768 Kbits/s.      |
| M3  | Encodage professionnel avec des taux d’échantillonnage allant jusqu’à 96 KHz et un débit maximal de 1,5 Mbits/s.      |
| N1  | Encodage sans perte avec des taux d’échantillonnage allant jusqu’à 48 KHz et un maximum de 2 canaux.                |
| N2  | Encodage sans perte avec des taux d’échantillonnage allant jusqu’à 96 KHz et un maximum de 6 canaux (5,1 Surround). |
| N3  | Encodage sans perte avec des taux d’échantillonnage allant jusqu’à 96 KHz et un maximum de 8 canaux (7,1 Surround). |



 

Pour la vidéo, cette propriété a l’une des valeurs suivantes :



| Valeur | Description                                                                       |
|-------|-----------------------------------------------------------------------------------|
| FOURNISSEURS  | Profil avancé (disponible uniquement sur le codec du profil avancé Windows Media Video 9) |
| CP  | n’est plus pris en charge                                                               |
| CANAL  | Profil principal                                                                      |
| SR  | Profil simple                                                                    |



 

Pour le contenu vidéo, vous pouvez demander un niveau de profil en définissant [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) avant de commencer l’encodage. Le codec tentera d’effectuer un encodage dans les paramètres du niveau de complexité demandé, mais les autres paramètres que vous configurerez seront prioritaires. Vous devez toujours vérifier la valeur du profil de complexité réel après l’encodage au cas où votre demande n’a pas pu être honorée.

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

 

 





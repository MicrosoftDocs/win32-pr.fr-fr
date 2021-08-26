---
description: Spécifie le nombre de threads qui seront utilisés par l’encodeur.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ac8b6ec040ba07a2e38b1e9d8e2df6cf0fcbfcdbba14481e9b50379ecc10df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953909"
---
# <a name="mfpkey_numthreads-property"></a>MFPKEY \_ propriété NUMTHREADS

Spécifie le nombre de threads qui seront utilisés par l’encodeur.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCNumThreads g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

1

## <a name="remarks"></a>Remarques

Cette valeur est destinée à diviser l’encodage en plusieurs threads pour tirer parti des ordinateurs avec plusieurs processeurs. Le fractionnement des tâches d’encodage en plusieurs threads peut entraîner une légère diminution de la qualité par rapport à un seul thread.

pour l’encodeur vidéo (wmvencod.dll) fourni avec Windows XP et Windows Vista, cette propriété doit avoir la valeur 1, 2 ou 4. Les autres valeurs sont arrondies à la valeur inférieure.

pour l’encodeur vidéo (wmvencod.dll) fourni avec Windows 7, cette propriété doit avoir la valeur 1, 2, 4 ou 8. Les autres valeurs sont arrondies à la valeur inférieure.

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

 

 





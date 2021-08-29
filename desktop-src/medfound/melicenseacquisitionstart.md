---
description: Déclenché par le moteur de stratégie lorsque l’acquisition de licence est sur le le début. L’acquisition de licence est effectuée à l’aide de l’implémentation d’applications de l’interface IMFContentProtectionManager.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Événement MELicenseAcquisitionStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea326ff23c4d546f0b692a813ef92ccfce8e3cc97320a8129daa9cedc4867bfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228969"
---
# <a name="melicenseacquisitionstart-event"></a>Événement MELicenseAcquisitionStart

Déclenché par le moteur de stratégie lorsque l’acquisition de licence est sur le le début. L’acquisition de licence est effectuée à l’aide de l’implémentation de l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Lorsque l’acquisition de licence est terminée, le moteur de stratégie déclenche l’événement [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 





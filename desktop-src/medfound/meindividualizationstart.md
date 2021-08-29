---
description: Déclenché par le moteur de stratégie lorsque l’individualisation est sur le le début. L’individualisation est effectuée à l’aide de l’implémentation d’applications de l’interface IMFContentProtectionManager.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Événement MEIndividualizationStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297ed3dea2dbdfe45a8ea812b7a5c674e1ef1bfb1c136aa54cfd5cd463cf9b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957449"
---
# <a name="meindividualizationstart-event"></a>Événement MEIndividualizationStart

Déclenché par le moteur de stratégie lorsque l’individualisation est sur le le début. L’individualisation est effectuée à l’aide de l’implémentation de l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de l’application.

Une application individualisée est une application qui a reçu une mise à niveau de ses composants de gestion des droits numériques (DRM) qui la différencie de toutes les autres copies de la même application. Les propriétaires de contenu peuvent exiger que leurs fichiers protégés soient lus uniquement sur une application qui a été individualisée.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

Lorsque l’acquisition de licence est terminée, le moteur de stratégie déclenche l’événement [MEIndividualizationCompleted](meindividualizationcompleted.md) .

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

 

 





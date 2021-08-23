---
description: Demande un nouvel exemple d’entrée à partir du filtre de convertisseur vidéo amélioré (EVR).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0058f8d0b7f8404a59f8c7e4fc5a4029c5ebaf4bc4f5c1b2678b1ed8c0f4f90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686119"
---
# <a name="ec_sample_needed"></a>\_exemple EC \_ requis

Demande un nouvel exemple d’entrée à partir du filtre de [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR).

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificateur du flux d’entrée qui a besoin d’une nouvelle entrée.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Le mélangeur pour le filtre EVR envoie ce message lorsqu’il a besoin d’un nouvel exemple d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> </dl>

 

 





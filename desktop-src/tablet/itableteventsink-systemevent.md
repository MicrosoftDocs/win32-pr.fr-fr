---
description: Se produit lorsqu’un événement système est disponible.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'ITabletEventSink :: SystemEvent, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412266"
---
# <a name="itableteventsinksystemevent-method"></a>ITabletEventSink :: SystemEvent, méthode

Se produit lorsqu’un événement système est disponible.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TCID* \[ dans\]
</dt> <dd>

Identificateur de la tablette.

</dd> <dt>

*CID* \[ dans\]
</dt> <dd>

Identificateur du stylet.

</dd> <dt>

*événement* \[ dans\]
</dt> <dd>

Code de l’événement système.

</dd> <dt>

*EventData* \[ dans\]
</dt> <dd>

Données d’événement système.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

La liste suivante contient les valeurs valides pour le paramètre d’événement.

-   SE \_ EXPLOITER
-   SE \_ DOUBLE \_ pression
-   SE \_ clic \_ droit
-   SE \_ Déplacez
-   SE \_ \_glisser-déplacer vers la droite
-   SE \_ MAINTENIR la touche \_ entrée
-   SE \_ conserver le \_ reste
-   SE \_ POINTage \_ entrée
-   SE \_ pointage de survol \_
-   SE \_ \_clic central
-   SE \_ ESSENTIEL
-   SE \_ touche de modification \_
-   SE \_ MODE de mouvement \_
-   SE \_ MIRE

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 





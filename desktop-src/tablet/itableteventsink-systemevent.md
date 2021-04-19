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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523301"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

La liste suivante contient les valeurs valides pour le paramètre d’événement.

-   \_appui sur se
-   SE \_ double \_ Tap
-   clic \_ droit \_ sur
-   SE \_ faire glisser
-   SE \_ déplacer vers la droite \_
-   \_Appuyez sur \_ entrée
-   maintien de la \_ \_ sortie
-   \_point de suspension de la se \_
-   \_point de suspension de se \_
-   \_clic central \_ se
-   \_touche se
-   \_touche de modification \_ se
-   \_mode de mouvement de se \_
-   \_curseur se

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 





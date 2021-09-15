---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration lorsque l’application de contrôle du panneau de configuration se ferme. L’application de contrôle envoie le message une fois pour chaque boîte de dialogue que l’application prend en charge.
title: Message CPL_STOP (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412566"
---
# <a name="cpl_stop-message"></a>\_Message d’arrêt cpl

Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration lorsque l’application de contrôle du panneau de configuration se ferme. L’application de contrôle envoie le message une fois pour chaque boîte de dialogue que l’application prend en charge.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numéro de la boîte de dialogue.

</dd> <dt>

*lData* 
</dt> <dd>

Valeur que l’application du panneau de configuration a chargée dans le membre **lpData** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) de la boîte de dialogue. L’application charge le membre **lpData** en réponse au message [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.

## <a name="remarks"></a>Notes

En réponse à ce message, une application du panneau de configuration doit effectuer un nettoyage pour la boîte de dialogue donnée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**fermeture de CPL \_**](cpl-exit.md)
</dt> <dt>

[**CPL \_ GETCOUNT**](cpl-getcount.md)
</dt> </dl>

 

 

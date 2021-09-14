---
title: Message WM_DDE_ADVISE (DDE. h)
description: une application cliente échange dynamique de données (dde) publie le message de notification de l’échange de données (dde) WM \_ \_ dans une application de serveur dde pour demander au serveur de fournir une mise à jour pour un élément de données à chaque modification de l’élément.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE des données de message Exchange
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095401"
---
# <a name="wm_dde_advise-message"></a>\_Message de \_ notification DDE WM

une application cliente échange dynamique de données (dde) publie le message de **\_ \_ notification** de l’échange de données (dde) WM dans une application de serveur dde pour demander au serveur de fournir une mise à jour pour un élément de données à chaque modification de l’élément.

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre client qui publie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible est un handle vers un objet mémoire global contenant une structure [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) qui spécifie la façon dont les données doivent être envoyées.

Le mot de poids fort contient un atome qui identifie l’élément de données demandé.

</dd> </dl>

## <a name="remarks"></a>Notes

Si une application cliente prend en charge plusieurs formats de presse-papiers pour une seule rubrique et un seul élément, elle peut envoyer plusieurs messages de **\_ \_ notification** de l’échange de message pour la rubrique et l’élément, en spécifiant un format de presse-papiers différent pour chaque message. Notez qu’un serveur peut prendre en charge plusieurs formats uniquement pour les liaisons de données à chaud, et non pour les liaisons de données à chaud.

### <a name="posting"></a>Publication

L’application cliente publie le message de **\_ \_ notification** de l’échange de messages avec le protocole WM en appelant la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , et non la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

L’application cliente alloue l’objet mémoire globale à l’aide de la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Elle alloue Atom à l’aide de la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

L’application cliente doit créer ou réutiliser le paramètre **WM \_ DDE \_ Advise** *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si l’application réceptrice (serveur) répond avec un message [**d' \_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif, l’application de publication doit supprimer l’objet.

L’indicateur **fRelease** n’est pas utilisé dans les messages de **\_ \_ notification DDE de WM** , mais leur comportement de libération de données est similaire à celui des données de l’échange de [**\_ \_ données (DDE) WM**](wm-dde-data.md) et des messages d’entourage de données par le biais de la **propriété** **fRelease** . [**\_ \_**](wm-dde-poke.md)

### <a name="receiving"></a>Réception

L’application serveur publie le message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) pour répondre positivement ou négativement. Lors de la publication de l' **\_ \_ accusé** de réception DDE de WM, l’application peut réutiliser l’Atom ou le supprimer et en créer un nouveau. Si le message d’accusé de réception **\_ DDE DDE \_** est positif, l’application doit supprimer l’objet mémoire globale ; dans le cas contraire, l’application ne doit pas supprimer l’objet.

Le serveur doit créer ou réutiliser le paramètre [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>Dde. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**\_données DDE \_ WM**](wm-dde-data.md)
</dt> <dt>

[**en-dessous du protocole WM \_ DDE \_**](wm-dde-poke.md)
</dt> <dt>

[**\_requête DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 


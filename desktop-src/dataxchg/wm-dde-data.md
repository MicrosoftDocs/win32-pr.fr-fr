---
title: Message WM_DDE_DATA (DDE. h)
description: Une application serveur de échange dynamique de données (DDE) publie un \_ \_ message de données WM dans une application cliente DDE pour transmettre un élément de données au client ou pour informer le client de la disponibilité d’un élément de données.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513597"
---
# <a name="wm_dde_data-message"></a>\_Message de \_ données DDE WM

Une application serveur de échange dynamique de données (DDE) publie un message de **\_ \_ données WM** dans une application cliente DDE pour transmettre un élément de données au client ou pour informer le client de la disponibilité d’un élément de données.

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre de serveur qui publie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible est un handle vers un objet mémoire global contenant une structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) avec les données et des informations supplémentaires. Le descripteur doit être défini sur la valeur **null** si le serveur notifie au client que la valeur de l’élément de données a changé pendant une liaison de données à chaud. Un lien à chaud est établi par le client qui envoie un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de messages (DDE) WM avec le bit **fDeferUpd** défini.

Le mot de poids fort contient un atome qui identifie l’élément de données pour lequel les données ou la notification sont envoyées.

</dd> </dl>

## <a name="remarks"></a>Notes

### <a name="posting"></a>Publication

L’application serveur alloue l’objet mémoire globale à l’aide de la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Elle alloue Atom à l’aide de la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Le serveur doit créer ou réutiliser le paramètre de *lParam* de données de l' [](/windows/desktop/api/Dde/nf-dde-packddelparam) échange de **données ( \_ DDE \_ ) WM** en appelant la fonction PackDDElParam ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si l’application réceptrice (cliente) répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif, l’application de publication (serveur) doit supprimer l’objet mémoire globale ; dans le cas contraire, le client doit supprimer l’objet après avoir extrait son contenu en appelant la fonction [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .

Si l’application serveur définit le membre **fRelease** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) sur **false**, le serveur est responsable de la suppression de l’objet lors de la réception d’un accusé de réception positif ou négatif.

L’application serveur ne doit pas définir à la fois les membres **fAckReq** et **fRelease** de la structure [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) sur **false**. Si les deux membres ont la valeur **false**, il est impossible pour le serveur de déterminer quand supprimer l’objet.

### <a name="receiving"></a>Réception

Si **fAckReq** a la **valeur true**, l’application cliente doit envoyer le message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE pour répondre positivement ou négativement. Lors de la publication d’un accusé de réception **\_ DDE DDE \_**, le client peut réutiliser l’Atom ou le supprimer et en créer un nouveau.

Le client doit créer ou réutiliser le paramètre [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si **fAckReq** a la **valeur false**, l’application cliente doit supprimer l’atome.

Si l’application de publication a spécifié l’objet de mémoire globale comme **null**, l’application réceptrice peut demander au serveur d’envoyer les données en publiant un message de [**\_ \_ demande de DDE WM**](wm-dde-request.md) .

Après le traitement d’un message de **\_ \_ données. WM DDE** dans lequel l’objet mémoire globale n’a pas la **valeur null**, le client doit libérer l’objet, sauf si l’une des conditions suivantes est remplie :

-   Le membre **fRelease** a la **valeur false**.
-   Le membre **fRelease** a la **valeur true**, mais l’application cliente répond avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE négatif négatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>DDE. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)
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

[**\_avis DDE \_ WM**](wm-dde-advise.md)
</dt> <dt>

[**en-dessous du protocole WM \_ DDE \_**](wm-dde-poke.md)
</dt> <dt>

[**\_requête DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 


---
title: Message WM_DDE_ACK (DDE. h)
description: 'Le \_ \_ message d’accusé de réception DDE DDE avertit une application échange dynamique de données (DDE) de la réception et du traitement des messages suivants : WM \_ DDE \_ en attente, \_ exécution DDE WM \_ , \_ données DDE WM \_ , \_ notification DDE WM, notification DDE non- \_ \_ \_ notification, \_ lancement DDE WM \_ ou \_ requête DDE WM \_ (dans certains cas). Pour poster ce message, appelez la fonction PostMessage avec les paramètres suivants.'
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032780"
---
# <a name="wm_dde_ack-message"></a>Message d’accusé de réception DDE de WM \_ \_

Le message d’accusé de réception **\_ DDE \_ DDE** notifie une application échange dynamique de données (DDE) de la réception et du traitement des messages suivants : [**WM \_ DDE \_**](wm-dde-poke.md)en attente, WM [**\_ DDE \_ Execute**](wm-dde-execute.md), WM DDE [**\_ \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ readvit**](wm-dde-advise.md), [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md), [**WM \_ DDE \_ initiate**](wm-dde-initiate.md)ou [**WM \_ DDE \_ Request**](wm-dde-request.md) (dans certains cas).

Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Lors de la réponse à l' [**\_ \_ initialisation**](wm-dde-initiate.md)de l’échange de messages WM, ce paramètre est un handle de la fenêtre de serveur qui envoie le message.

Lors de la réponse à l' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md), ce paramètre est un handle de la fenêtre de serveur qui publie le message.

Lorsque vous répondez à tous les autres messages, ce paramètre est un handle vers la fenêtre du client ou du serveur qui publie le message.

</dd> <dt>

*lParam* 
</dt> <dd>

Lors de la réponse au lancement de l' [**\_ échange de liaison \_ WM**](wm-dde-initiate.md), le mot de poids faible contient un atome qui identifie l’application de réponse. Le mot de poids fort contient un atome qui identifie la rubrique pour laquelle une conversation est établie.

Lors de la réponse à l' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md), le mot de poids faible spécifie une structure [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenant une série d’indicateurs qui indiquent l’état de la réponse. Le mot de poids fort est un handle vers un objet de mémoire globale qui contient la chaîne de commande qui a été reçue dans le message d' **\_ \_ exécution DDE de WM** .

Lors de la réponse à tous les autres messages, le mot de poids faible spécifie une structure [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) contenant une série d’indicateurs qui indiquent l’état de la réponse. Le mot de poids fort contient un atome global qui identifie le nom de l’élément de données pour lequel la réponse est envoyée.

</dd> </dl>

## <a name="remarks"></a>Notes

### <a name="posting"></a>Publication

À l’exception de la réponse au message de [**\_ \_ lancement DDE de WM**](wm-dde-initiate.md) , l’application publie le message d' **\_ \_ accusé** de réception DDE en appelant la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , et non en appelant la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . Lors de la réponse à l' **\_ \_ initialisation** de l’échange de messages WM, l’application envoie le message d’accusé de réception **\_ \_ DDE** en appelant **SendMessage**. Dans ce cas, ni l’atome de nom d’application, ni l’atome de nom de rubrique ne doivent avoir la **valeur null** (même si le message « **WM \_ DDE \_ initiate** » spécifie des atomes **null** ).

Lors de la réception d’un message avec un Atom associé, la publication d’applications **WM \_ DDE \_ ACK** peut réutiliser l’atome qui accompagnait le message d’origine, ou il peut le supprimer et en créer un nouveau.

Lors de la reconnaissance de l' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md), l’application qui publie l' **\_ \_ accusé** de réception de l’échange de messages WM doit réutiliser l’objet mémoire globale identifié dans le message d’origine **WM \_ DDE \_ Execute** .

Tous les messages d’accusé de réception **\_ DDE \_ DDE** publiés doivent créer ou réutiliser le paramètre *lParam* en appelant la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou la fonction [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si une application a initié l’arrêt d’une conversation en publiant le protocole [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) et est en attente de confirmation, l’application en attente ne doit pas accuser réception (positif ou négatif) des messages suivants envoyés par l’autre application. L’application en attente doit supprimer tous les atomes ou objets de mémoire partagée reçus dans ces messages intermédiaires. Les objets de mémoire ne doivent pas être libérés si l’indicateur **fRelease** est défini sur **false** dans les messages de [**\_ \_ données**](wm-dde-data.md) d’interfonctionnement [**DDE de WM \_ \_**](wm-dde-poke.md) et de WM.

### <a name="receiving"></a>Réception

L’application qui reçoit un message « **WM \_ DDE \_ ACK** » doit supprimer tous les atomes accompagnant le message. Si l’application reçoit un **\_ \_ accusé** de réception DDE de WM en réponse à un message avec un objet de mémoire globale associé, et que l’objet a été envoyé avec les indicateurs **fRelease** définis sur **false**, l’application est responsable de la suppression de l’objet.

Si l’application reçoit un message **d' \_ \_ accusé** de réception DDE de WM négatif publié en réponse à un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de messages de ce fichier, l’application doit supprimer l’objet mémoire globale qui a été publié avec le message d' **\_ \_ avis DDE DDE** d’origine. Si l’application reçoit un message **d' \_ \_ accusé** de réception DDE de WM négatif publié en réponse à une demande de données de l' [**échange de \_ \_ données (DDE**](wm-dde-data.md)) WM, à un message d’exécution DDE ou à un message d' [**\_ \_ exécution DDE**](wm-dde-execute.md) de WM, l’application doit supprimer l’objet mémoire globale qui est publié avec le message d’origine **WM \_ DDE \_ Data**, **WM \_ DDE \_** en attente ou **WM \_ DDE \_ Execute** . [**\_ \_**](wm-dde-poke.md)

L’application qui reçoit un message **d' \_ \_ accusé** de réception DDE de WM publié doit libérer le paramètre *lParam* à l’aide de la fonction [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

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

[**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**\_avis DDE \_ WM**](wm-dde-advise.md)
</dt> <dt>

[**\_données DDE \_ WM**](wm-dde-data.md)
</dt> <dt>

[**\_exécution DDE de WM \_**](wm-dde-execute.md)
</dt> <dt>

[**\_lancement de DDE de WM \_**](wm-dde-initiate.md)
</dt> <dt>

[**en-dessous du protocole WM \_ DDE \_**](wm-dde-poke.md)
</dt> <dt>

[**\_requête DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

[**arrêt de l’échange de thread WM \_ \_**](wm-dde-terminate.md)
</dt> <dt>

[**informer de l' \_ échange de \_ notification**](wm-dde-unadvise.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[À propos de échange dynamique de données](about-dynamic-data-exchange.md)
</dt> </dl>

 


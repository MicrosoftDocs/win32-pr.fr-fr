---
description: Cette section fournit une vue d’ensemble du modèle de thread de manipulation directe, du mode de traitement des messages de fenêtre par manipulation directe et de la façon dont l’état d’une fenêtre d’affichage est modifié à mesure qu’une entrée est mappée aux mouvements de sortie.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Traitement des entrées avec DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 284a0a1866a2082e2c34c65de347b0dcdfab3a64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106536939"
---
# <a name="processing-input-with-directmanipulation"></a>Traitement des entrées avec DirectManipulation

Cette section fournit une vue d’ensemble du modèle de thread de [manipulation directe](direct-manipulation-portal.md) , du mode de traitement des messages de fenêtre par manipulation directe et de la façon dont l’état d’une fenêtre d’affichage est modifié à mesure qu’une entrée est mappée aux mouvements de sortie.

- [Workflow d’entrée](#input-flow)
- [Remarques](#remarks)

[La manipulation directe](direct-manipulation-portal.md) utilise deux threads pour coordonner les opérations asynchrones :

*Thread d’interface utilisateur* : thread qui possède le **HWND** associé à l’entrée. Ce thread est propriétaire de l’initialisation de [la manipulation directe](direct-manipulation-portal.md). Le traitement des entrées de la souris et du clavier se produit également sur le thread d’interface utilisateur.

*Thread délégué* : thread créé et détenu par [manipulation directe](direct-manipulation-portal.md). Le traitement des entrées tactiles se produit sur le thread délégué.

## <a name="input-flow"></a>Workflow d’entrée

Dans une configuration classique où le test de positionnement est effectué sur le thread d’interface utilisateur, les messages de fenêtre sont traités par [manipulation directe](direct-manipulation-portal.md) dans l’ordre suivant :

![Diagramme montrant l’ordre dans lequel les messages sont traités.](images/inputprocessing.png)

Pour une fenêtre d’affichage au repos :

1. Une série de messages de fenêtre atteint le thread délégué.
2. Les messages [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) et [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) sont envoyés par le thread délégué au thread de test de positionnement indépendant (IHT).
3. Si [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) est appelé à partir du thread IHT, les messages peuvent être envoyés au thread d’interface utilisateur par le thread délégué, en fonction de la valeur du [**\_ \_ type de DIRECTMANIPULATION HITTEST**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) lors de l’appel de [**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget) .
4. Si [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) n’est pas appelé à partir du thread IHT, les messages sont toujours envoyés par le thread délégué au thread d’interface utilisateur.
5. Le client peut appeler [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) à partir du thread d’interface utilisateur pour permettre à la [manipulation directe](direct-manipulation-portal.md) de détecter une manipulation.
6. Si une manipulation est détectée, la [manipulation directe](direct-manipulation-portal.md) envoie un message [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) pour notifier au client que l’entrée est gérée par manipulation directe. L’état de la fenêtre d’affichage est défini sur **en cours d’exécution** et la transformation de sortie est mise à jour.
7. Si une interaction autre qu’une manipulation est détectée, la [manipulation directe](direct-manipulation-portal.md) envoie les messages restants au thread d’interface utilisateur.

Pour une fenêtre d’affichage en mouvement (avec un État en cours d’exécution ou d’INERTIe), le message de fenêtre atteint d’abord le thread délégué, où la [manipulation directe](direct-manipulation-portal.md) effectue des tests sur toutes les fenêtres d’affichage en cours d’exécution. La manipulation directe affecte automatiquement le contact aux fenêtres d’affichage appropriées identifiées par le test de positionnement. L’état de la fenêtre d’affichage est RUNNING et la transformation de sortie est mise à jour.

Dans certains cas, un thread d’interface utilisateur d’application peut être trop lent pour répondre au test de positionnement. Un thread de test de positionnement peut être utilisé ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) pour permettre au client de déplacer les messages [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) et [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) vers un thread spécifique afin d’autoriser le test de positionnement.

## <a name="remarks"></a>Notes

En règle générale, la [manipulation directe](direct-manipulation-portal.md) envoie uniquement des messages [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) et [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) au thread d’interface utilisateur, en préservant les messages ultérieurs en attendant une réponse du client. Si le client appelle [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), les seuls messages reçus par le thread d’interface utilisateur lorsqu’une manipulation est détectée sont [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) et [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)et le [message WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

Le client peut ne pas appeler [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) lors du traitement des messages [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) et [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . Dans ce cas, la [manipulation directe](direct-manipulation-portal.md) envoie tous les messages au thread d’interface utilisateur sans analyser les messages pour voir s’il existe une manipulation. Le client peut ensuite choisir n’importe quel point pour appeler **SetContact** et faire en sorte que la manipulation directe démarre la détection des manipulations et envoie des messages de [message WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) lorsqu’un message est détecté.

**Windows 10 et versions ultérieures :** Vous pouvez choisir les manipulations que vous souhaitez gérer en appelant [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) avant d’appeler [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) sur un message [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) ou [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . **DeferContact** garantit que tous les messages suivants sont envoyés au thread d’interface utilisateur pour la période spécifiée.

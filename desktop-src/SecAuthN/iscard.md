---
description: Vous permet d’ouvrir et de gérer une connexion à une carte à puce.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interface ISCard (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011254"
---
# <a name="iscard-interface"></a>Interface ISCard

\[L’interface **ISCard** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

L’interface **ISCard** vous permet d’ouvrir et de gérer une connexion à une [*carte à puce*](../secgloss/s-gly.md). Chaque connexion à une carte requiert une seule instance correspondante de l’interface **ISCard** .

Le gestionnaire de [*ressources*](../secgloss/r-gly.md) de carte à puce doit être disponible chaque fois qu’une instance de **ISCard** est créée. Si ce service n’est pas disponible, la création de l’interface échoue.

L’exemple suivant illustre une utilisation type de l’interface **ISCard** . L’interface **ISCard** est utilisée pour la connexion à la carte à puce, l’envoi d’une [*transaction*](../secgloss/t-gly.md)et la libération de la carte à puce.

**Pour soumettre une transaction à une carte spécifique**

1.  Créer une interface **ISCard** .
2.  Connectez-vous à une carte à puce en spécifiant un [*lecteur*](../secgloss/r-gly.md) de carte à puce ou en utilisant un handle valide précédemment établi.
3.  Créer des commandes de transaction avec des interfaces de carte à puce [**ISCardCmd**](iscardcmd.md)et [**ISCardISO7816**](iscardiso7816.md) .
4.  Utilisez **ISCard** pour envoyer les commandes de transaction en vue de leur traitement par la carte à puce.
5.  Utilisez **ISCard** pour libérer la carte à puce.
6.  Libérez l’interface **ISCard** .

## <a name="members"></a>Membres

L’interface **ISCard** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCard** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **ISCard** possède ces méthodes.



| Méthode                                          | Description                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | Attache un objet à un handle de carte à puce ouvert et configuré.<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | Ouvre la carte à puce dans le lecteur nommé.<br/>                                                                                                                                                                            |
| [**Detach**](iscard-detach.md)                 | Ferme la connexion ouverte à la carte à puce.<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | Réclame un accès exclusif à la carte à puce.<br/>                                                                                                                                                                           |
| [**Rattacher**](iscard-reattach.md)             | Réinitialise et réinitialise la carte à puce.<br/>                                                                                                                                                                             |
| [**Libellé**](iscard-transaction.md)       | Exécute une opération d’écriture et de lecture sur l’objet de commande de carte à puce ([*unité de données de protocole d’application*](../secgloss/a-gly.md)).<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | Libère l’accès exclusif à la carte à puce.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Propriétés

L’interface **ISCard** possède les propriétés suivantes.



| Propriété                                               | Type d’accès          | Description                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Lecture seule<br/> | Récupère la [*chaîne ATR*](../secgloss/a-gly.md) de la carte à puce.<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | Lecture seule<br/> | Récupère le handle de la carte à puce connectée.<br/>                                                                                                                                  |
| [**Context**](iscard-get-context.md)<br/>       | Lecture seule<br/> | Récupère le handle de [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md) actuel.<br/>                            |
| [**Protocol**](iscard-get-protocol.md)<br/>     | Lecture seule<br/> | Récupère l’identificateur du protocole en cours d’utilisation sur la carte à puce.<br/>                                                                                                        |
| [**Statut**](iscard-get-status.md)<br/>         | Lecture seule<br/> | Récupère l' [*État*](../secgloss/s-gly.md) actuel de la [*carte à puce*](../secgloss/s-gly.md) .<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



 

 

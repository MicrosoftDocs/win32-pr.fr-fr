---
description: PNRP utilise la fonction WSANSPIoctl pour recevoir des notifications sur les modifications apportées aux éléments suivants.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP et WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cc07415fb483e75af8d836274d45a2c53f205e3aae15f893f909d2363c0d15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553309"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP et WSANSPIoctl

PNRP utilise la fonction [**WSANSPIoctl**](winsock-nsp-reference-links.md) pour recevoir des notifications sur les modifications apportées aux éléments suivants :

-   Liste de clouds réseau
-   Disponibilité des résultats d’une demande de résolution de noms

Le premier appel à [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) définit le type d’informations sur lequel un client est averti. un client peut être averti avec un message Windows, une routine de saisie semi-automatique, un handle vers un objet WSAEVENT ou un port. Pour plus d’informations sur les options et la définition du paramètre *lpCompletion* , consultez **WSANSPIoctl**.

Pour continuer à recevoir des notifications après un appel à [**WSALookupServiceNext**](winsock-nsp-reference-links.md), une application doit à nouveau appeler **WSANSPIoctl** .

La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloque même si **WSANSPIoctl** est appelé. Avant d’appeler **WSALookupServiceNext**, une application doit attendre jusqu’à ce qu’elle reçoive une notification, si le blocage est un problème.

Lors de l’appel de cette fonction, les paramètres doivent avoir les valeurs suivantes :

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*Fonction*
</dt> <dd>

Spécifie le handle retourné par [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) .

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Doit être **SIO \_ NSP \_ notifier la \_ modification**.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

Doit avoir la **valeur null**.

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

Doit être égal à zéro (0).

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

Doit avoir la **valeur null**.

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Doit être égal à zéro (0).

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

Doit avoir la **valeur null**.

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Spécifie une **valeur null** ou un pointeur vers une structure [**WSACOMPLETION**](winsock-nsp-reference-links.md) .

</dd> </dl>

Une fois la notification reçue, appelez [**WSALookupServiceNext**](winsock-nsp-reference-links.md) une fois pour obtenir les résultats.

Pour mettre fin à une recherche, appelez [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).

## <a name="resolution-notifications"></a>Notifications de résolution

Un client peut être notifié à chaque fois qu’une entrée de résolution de nom est ajoutée. Le client appelle ensuite [**WSALookupServiceNext**](winsock-nsp-reference-links.md) pour obtenir les données de résolution.

Si le client n’utilise pas cette technique, un appel à [**WSALookupServiceNext**](winsock-nsp-reference-links.md) peut être bloqué jusqu’à ce que le délai d’attente spécifié se produise.

## <a name="cloud-list-notifications"></a>Notifications de liste de clouds

Un client peut être averti chaque fois qu’une modification est apportée à un ensemble de clouds.

La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retourne le **WSA \_ E \_ \_** plus comme délimiteur défini. L’application cliente doit énumérer les clouds existants jusqu’à ce que ce message soit retourné, puis utiliser un schéma de notification pour récupérer les modifications ultérieures à mesure qu’elles se produisent. Une application cliente peut également appeler **WSALookupServiceNext**, mais l’appel est bloqué jusqu’à ce qu’une modification se produise.

La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retourne un Cloud dans une structure **WSAQUERYSET** . L’un des indicateurs suivants est retourné dans le membre **dwOutputFlags** .



| Valeur               | Description                                             |
|---------------------|---------------------------------------------------------|
| le résultat \_ est \_ ajouté   | Le Cloud retourné est ajouté.                    |
| RÉSULTAT \_ \_ modifié | Le Cloud retourné est modifié.                  |
| le résultat \_ est \_ supprimé | Le Cloud retourné est supprimé et n’est pas valide. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[PNRP et WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP et WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP et WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[Codes d’erreur du NSP PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSALookupServiceBegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**WSAQUERYSET**
</dt> </dl>

 

 




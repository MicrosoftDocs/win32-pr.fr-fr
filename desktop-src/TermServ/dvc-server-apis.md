---
title: API serveur DVC
description: Les API de serveur de canal virtuel dynamique (DVC) sont implémentées par le serveur Connexion Bureau à distance (RDC) de la connexion.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f43ab4032e4500732e2f9ee6cfa9a2c17f8b1892e55973ba633758792f00bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353972"
---
# <a name="dvc-server-apis"></a>API serveur DVC

Les API de serveur de canal virtuel dynamique (DVC) sont implémentées par le serveur Connexion Bureau à distance (RDC) de la connexion.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**IWTSServerChannel**](iwtsserverchannel.md)
</dt> <dd>

Cette interface n’est pas prise en charge.

</dd> <dt>

[**IWTSServerChannelManager**](iwtsserverchannelmanager.md)
</dt> <dd>

Cette interface n’est pas prise en charge.

</dd> <dt>

[**TPriority**](tpriority.md)
</dt> <dd>

Cette énumération n'est pas utilisée.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Changements de comportement pour d’autres API serveur

-   L’API serveur a été étendue avec un appel supplémentaire qui ouvre un canal virtuel dynamique (DVC). L’appel supplémentaire est effectué à l’aide de la fonction [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Lors de l’utilisation de cette API avec DVC, elle ajoutera toujours les données lues avec l' [**\_ \_ en-tête**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)de l’PDU de canal. Cela signifie que toute lecture doit être effectuée avec au moins le bloc de données de **\_ \_ longueur PDU de canal** passé comme mémoire tampon d’entrée.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Si le descripteur de fichier du DVC est récupéré en appelant [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) avec le paramètre *WTSVirtualFileHandle*, la même règle s’applique. Toutes les lectures incluent l' [**\_ \_ en-tête**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)de l’PDU du canal, et la mémoire tampon de lecture doit être au moins égale à la taille de la **\_ PDU \_ du canal** .

 

 
---
description: Prise en charge des extensions MTP
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: Prise en charge des extensions MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16a80b640b50346f1724aec771d8ffd82de565f078e5b3e1d562c346e34973a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193570"
---
# <a name="supporting-mtp-extensions"></a>Prise en charge des extensions MTP

## <a name="media-transfer-protocol"></a>Protocole de transfert de médias

Le protocole MTP (Media Transfer Protocol) est une extension du protocole PTP (Picture Transfer Protocol). Par conséquent, toutes les sémantiques de protocole PTP sont valides dans MTP.

MTP communique à l’aide de commandes et de réponses entre deux parties, l’initiateur et le répondeur. Les rôles des appareils impliqués sont très clairement définis. Le PC est généralement l’initiateur et l’appareil est toujours le répondeur. Un appareil non-PC peut également être un initiateur (par exemple, un étage de voiture ou un boîtier Microsoft X). Un appareil ne peut jamais assumer les deux rôles en même temps.

L’initiateur démarre la communication en envoyant une commande au répondeur. Le répondeur traite la commande et renvoie une réponse appropriée. Une phase de données peut être associée à la commande. Si c’est le cas, la direction du Workflow doit être connue au préalable et acceptée par l’initiateur et le répondeur. N’oubliez pas qu’il n’existe pas d’en-tête descriptif indiquant des flux de données pour les nouvelles commandes.

Le répondeur peut démarrer une communication indépendante de l’initiateur. Par exemple, le répondeur peut envoyer des événements à l’initiateur. Toutefois, aucune donnée ne peut être envoyée avec l’événement. Si des données doivent être lues dans le cadre de l’événement, l’initiateur doit envoyer une commande MTP et l’appareil peut envoyer des données en réponse à la commande.

Pour obtenir une description complète de MTP, reportez-vous à la [spécification MTP](https://www.usb.org/sites/default/files/MTPv1_1.zip).

## <a name="sending-mtp-commands"></a>Envoi de commandes MTP

Les applications peuvent envoyer des commandes MTP à un appareil en appelant la méthode [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) . La commande envoyée varie selon qu’il existe une phase de données, et si toutes les données associées sont lues ou écrites sur l’appareil. Le tableau suivant décrit les trois commandes d’extension MTP possibles.

N’oubliez pas que ces commandes sont spécifiques à MTP ; et sont donc uniquement implémentées par le pilote de classe MTP WPD.



| Commande  | Description  |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**\_transfert de \_ \_ données de \_ fin \_ MTP \_ MTP de commande wpd**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | Émet une commande MTP qui signale la conclusion d’une opération de lecture ou d’écriture de données.              |
| [**commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ sans \_ \_ phase Data**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | Émet une commande MTP sans une phase de données correspondante.                                         |
| [**commande \_ wpd \_ MTP \_ ext \_ Execute Command Execute \_ \_ avec les \_ données \_ à \_ écrire**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | Émet une commande MTP qui est suivie de données d’accompagnement, qui seront écrites sur l’appareil. |
| [**commande \_ wpd \_ MTP \_ ext \_ Execute Command Execute \_ \_ avec les \_ données \_ à \_ lire**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | Émet une commande MTP qui est suivie de données d’accompagnement, qui sont lues à partir de l’appareil.       |
| [**\_commande wpd \_ MTP MTP de \_ lecture des \_ \_ données**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | Émet une commande MTP qui envoie les données de l’appareil au PC.                                  |
| [**\_données d' \_ \_ écriture MTP \_ ext \_ de la commande wpd**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | Émet une commande MTP qui envoie des données à l’appareil à partir du PC.                                  |



 

Quelle que soit la phase, vous devez spécifier le code de l' **\_ \_ \_ \_ opération \_ ext MTP de la propriété wpd** et les paramètres de l' **\_ \_ \_ \_ opération MTP \_ ext de la propriété wpd** .

Si le pilote MTP a pu envoyer la commande à l’appareil, les valeurs de retour contiennent toujours le **\_ Code de \_ \_ \_ réponse \_ MTP ext de la propriété wpd**. Si le code de réponse indique une réussite et si la sémantique de la commande autorise les paramètres de réponse, les paramètres de **\_ \_ \_ réponse MTP ext \_ \_ de la propriété wpd** seront également disponibles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 

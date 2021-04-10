---
description: Net.exe peut être utilisé pour arrêter et démarrer le protocole IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862553"
---
# <a name="netexe"></a>Net.exe

Net.exe peut être utilisé pour arrêter et démarrer le protocole IPv6. Le redémarrage D’ipv6 réinitialise le protocole comme si l’ordinateur redémarrait, ce qui peut modifier les numéros d’interface. Net.exe possède de nombreuses sous-commandes. Les commandes suivantes s’appliquent à IPv6 :

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**
</dt> <dd>

Arrête le protocole IPv6 et le décharge de la mémoire. Cette commande échoue si des sockets IPv6 sont ouverts.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET START tcpip6**
</dt> <dd>

Démarre le protocole IPv6 s’il a été arrêté. Si un nouveau fichier de pilote de Tcpip6.sys est présent dans le répertoire% SystemRoot% \\ system32 \\ drivers, ce fichier de pilote est chargé.

</dd> </dl>

 

 




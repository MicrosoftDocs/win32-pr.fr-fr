---
title: Validation d’une PDU
description: Lorsque l’application WinSNMP appelle la fonction SnmpSendMsg ou la fonction SnmpEncodeMsg, l’implémentation de l’utilitaire WinSNMP de Microsoft vérifie la validité de l’PDU et les autres paramètres de la fonction.
ms.assetid: 0f5754ff-3688-465b-a1ad-bf7d89d7dbd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d3fe0f9831f285b51b3060517d2037a8ec05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380220"
---
# <a name="validating-a-pdu"></a>Validation d’une PDU

Lorsque l’application WinSNMP appelle la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ou la fonction [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) , l’implémentation de l’utilitaire WinSNMP de Microsoft vérifie la validité de l’PDU et les autres paramètres de la fonction.

La valeur d’un composant de données PDU (ou champ) peut être valide individuellement, mais elle peut être non valide en association avec les valeurs d’autres champs. Par exemple, à moins que le champ **\_ type d’unité** d’alimentation (PDU) du PDU soit SNMP \_ PDU \_ GETBULK ou SNMP \_ PDU \_ Response, les champs d' **\_ État d’erreur** et d' **\_ index des erreurs** doivent être égaux à zéro. Toute autre combinaison de valeurs constitue un PDU non valide.

L’implémentation rejette les PDU non valides et retourne l’état d’erreur SNMPAPI \_ échec. Il définit un code d’erreur étendu égal à \_ PDU SNMPAPI \_ non valide.

 

 





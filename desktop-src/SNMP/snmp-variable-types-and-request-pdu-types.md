---
title: Types de variables SNMP et types de PDU de demande
description: Les définitions de certains types de variable SNMP et les types de PDU de demande ont changé. Le fichier SNMP. h mappe les anciens types aux nouveaux types correspondants.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728956"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a>Types de variables SNMP et types de PDU de demande

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les définitions de certains types de variable SNMP et les types de PDU de demande ont changé. Le fichier SNMP. h mappe les anciens types aux nouveaux types correspondants.

## <a name="modified-snmp-variable-types"></a>Types de variable SNMP modifiés

Vous devez utiliser les nouveaux types de variables SNMP listés dans le tableau ci-dessous lorsque vous développez des applications de gestionnaire qui utilisent l’API de gestion SNMP de Microsoft. Le tableau répertorie les anciens types de variable SNMP avec les nouveaux types de variables correspondants.

| Ancien type de variable        | Nouveau type de variable |
|--------------------------|-------------------|
| \_ \_ Adresse IP ASN RFC1155  | \_adresse IP ASN    |
| \_Compteur RFC1155 \_ ASN    | \_COUNTER32 ASN    |
| \_Jauge ASN RFC1155 \_      | \_Gauge32 ASN      |
| ASN \_ RFC1155 \_ graduations  | \_graduations ASN    |
| \_RFC1155 ASN \_ opaque     | ASN \_ opaque       |
| ASN \_ RFC1213 \_ DISPSTRING | \_OCTETSTRING ASN  |



 

## <a name="modified-snmp-pdu-request-types"></a>Types de demandes PDU SNMP modifiés

Vous devez utiliser les nouveaux types de PDU SNMP figurant dans le tableau ci-dessous lorsque vous développez des applications de gestionnaire qui utilisent l’API de gestion SNMP de Microsoft. Le tableau répertorie les anciens types de PDU SNMP avec les nouveaux types de PDU correspondants.

| Ancien type d’unité d’alimentation                 | Nouveau type de PDU        |
|------------------------------|---------------------|
| ASN \_ RFC1157 \_ GETREQUEST     | \_récupération du PDU SNMP \_      |
| ASN \_ RFC1157 \_ GETNEXTREQUEST | \_PDU SNMP \_ GetNext  |
| ASN \_ RFC1157 \_ GETRESPONSE    | \_réponse PDU \_ SNMP |
| ASN \_ RFC1157 \_ SETREQUEST     | \_ensemble d’PDU SNMP \_      |
| \_Interruption ASN RFC1157 \_           | \_V1TRAP PDU \_ SNMP   |



 

 

 
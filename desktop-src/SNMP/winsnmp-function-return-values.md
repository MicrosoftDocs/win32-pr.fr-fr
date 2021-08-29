---
title: Valeurs de retour de la fonction WinSNMP
description: La valeur de retour d’un appel de fonction WinSNMP peut être un handle vers une ressource que l’implémentation de l’WinSNMP Microsoft alloue pour l’application WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee75d85bf2e9b48f0b3172332f4340b21271ec37a9bc1027d63750927710f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142812"
---
# <a name="winsnmp-function-return-values"></a>Valeurs de retour de la fonction WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

La valeur de retour d’un appel de fonction WinSNMP peut être un handle vers une ressource que l’implémentation de l’WinSNMP Microsoft alloue pour l’application WinSNMP.

Le tableau suivant répertorie les cinq types de descripteurs de ressources que l’implémentation alloue.



| Type de handle    | Description                       |
|----------------|-----------------------------------|
| \_session HSNMP | Handle vers une session WinSNMP       |
| \_entité HSNMP  | Handle vers une entité SNMP          |
| \_contexte HSNMP | Handle vers un contexte SNMP         |
| \_PDU HSNMP     | Handle vers une unité de données de protocole    |
| HSNMP \_ VBL     | Handle vers une liste de liaisons de variables |



 

Pour plus d’informations, consultez [objets descripteur de ressource](resource-handle-objects.md).

La valeur de retour peut également être une valeur d’entier long non signé du type **smiUINT32** qui représente une \_ valeur d’État SNMPAPI.

Le tableau suivant répertorie les valeurs d’État WinSNMP et leur signification.



| Statut           | Description                                                                      |
|------------------|----------------------------------------------------------------------------------|
| échec de SNMPAPI \_ | Indique une erreur. Équivaut à 0 ou **null**.                                    |
| réussite de SNMPAPI \_ | Indique que la fonction s’est terminée avec succès. Équivaut à 1 ou à un nombre positif. |



 

 

 
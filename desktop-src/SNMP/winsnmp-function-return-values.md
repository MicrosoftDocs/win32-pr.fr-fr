---
title: Valeurs de retour de la fonction WinSNMP
description: La valeur de retour d’un appel de fonction WinSNMP peut être un handle vers une ressource que l’implémentation de l’WinSNMP Microsoft alloue pour l’application WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031734"
---
# <a name="winsnmp-function-return-values"></a>Valeurs de retour de la fonction WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

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



 

 

 
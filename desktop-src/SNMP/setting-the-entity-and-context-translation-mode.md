---
title: Définition du mode de traduction entité et contexte
description: L’application WinSNMP peut spécifier l’interprétation et la traduction des paramètres d’entité et de contexte en définissant le mode de traduction entité et contexte. L’implémentation de l’WinSNMP Microsoft stocke le mode dans une base de données.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50b5ecfb1a4703795f970f5d7c13ceaa3d64980
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028913"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Définition du mode de traduction entité et contexte

L’application WinSNMP peut spécifier l’interprétation et la traduction des paramètres d’entité et de contexte en définissant le mode de traduction entité et contexte. L’implémentation de l’WinSNMP Microsoft stocke le mode dans une base de données.

Le paramètre de l’entité et du mode de traduction du contexte détermine la manière dont la fonction [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) et la fonction [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) interprètent les chaînes d’entrée. Le paramètre détermine également le type de chaîne de sortie que les fonctions [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) et [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) retournent. Pour plus d’informations, consultez [prise en charge des chaînes d’adresses IPX dans WinSNMP](support-for-ipx-address-strings-in-winsnmp.md).

L’implémentation retourne l’entité et le mode de traduction de contexte par défaut actuels dans le paramètre *nTranslateMode* de la fonction [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) . Pour récupérer l’entité et le mode de traduction de contexte actifs en vigueur pour l’implémentation, une application peut appeler la fonction [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) à tout moment.

Les modes d’entité et de traduction de contexte valides sont les suivants.

| Mode                      | Signification                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ traduit       | L’implémentation utilise sa base de données pour traduire des noms conviviaux pour les entités SNMP et les objets managés. L’implémentation les traduit en composants SNMPv1 ou SNMPv2C.                                                                                                  |
| SNMPAPI non \_ traduit \_ v1 | L’implémentation interprète les paramètres d’entité SNMP comme des adresses de transport SNMP littérales et des paramètres de contexte en tant que chaînes de communauté SNMP littérales. Pour les entités de destination SNMPv2, l’implémentation crée des messages SNMP sortants qui contiennent une valeur de zéro dans le champ version. |
| SNMPAPI non \_ traduit \_ v2 | L’implémentation interprète les paramètres d’entité SNMP comme des adresses de transport SNMP et les paramètres de contexte en tant que chaînes de communauté SNMP littérales. Pour les entités de destination SNMPv2, l’implémentation crée des messages SNMP sortants qui contiennent une valeur de 1 dans le champ version.            |



 

L’implémentation tente d’associer des ressources dans sa base de données à l’adresse de transport littérale de l’entité de gestion.

Pour modifier le mode de traduction d’entité et de contexte, une application WinSNMP doit appeler la fonction [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) . Si le mode de traduction demandé n’est pas valide, la fonction échoue et [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) retourne le code d’erreur SNMPAPI \_ mode \_ non valide.

 

 





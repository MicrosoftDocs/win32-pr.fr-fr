---
title: Chaînes de style C
description: Une application WinSNMP peut utiliser des chaînes de style C se terminant par un caractère NULL pour convertir des objets d’entité et d’identificateur d’objet (OID) vers et à partir de leurs représentations sous forme de chaîne.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839098"
---
# <a name="c-style-strings"></a>Chaînes de style C

Une application WinSNMP peut utiliser des chaînes de style C se terminant par un caractère **null** pour convertir des objets d’entité et d’identificateur d’objet (OID) vers et à partir de leurs représentations sous forme de chaîne.

Les fonctions WinSNMP qui manipulent des chaînes de style C incluent [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)et [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Étant donné que [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) et [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) retournent un pointeur vers une variable de chaîne de style C, l’application WinSNMP doit passer une valeur appropriée dans le paramètre *Size* lorsqu’il effectue des appels à ces fonctions. Pour plus d’informations, consultez les pages de référence de ces fonctions.

> [!Note]  
> Le paramètre *Context* des fonctions [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) et [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) doit être une structure de chaîne d’octets, c’est-à-dire une structure [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) . Le paramètre de *contexte* ne peut pas être une chaîne de style C. La chaîne contenue dans une structure **smiOCTETS** ne nécessite pas d’octet de fin **null**.

 

 

 





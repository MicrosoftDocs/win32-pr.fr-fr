---
title: Configuration logicielle requise pour l’API WinSNMP
description: Une application WinSNMP doit accéder à l’API WinSNMP par le biais de la bibliothèque de liens dynamiques WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cf78c4937996a44b2a82ebeb0b2963f9a4ffaada0288068b07cd3b60432c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886069"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Configuration logicielle requise pour l’API WinSNMP

Une application WinSNMP doit accéder à l’API WinSNMP par le biais de la bibliothèque de liens dynamiques WSNMP32.DLL.

Les fichiers suivants sont requis pour prendre en charge les fonctionnalités de l’API WinSNMP.



| Nom de fichier     | Description                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. LIB  | Bibliothèque WinSNMP                                                                              |
| WSNMP32.DLL  | Fournit l’interface WinSNMP                                                                   |
| WINSNMP. Manutention    | Fichier d’en-tête WinSNMP                                                                          |
| SNMPTRAP.EXE | Reçoit des interruptions SNMP et les transfère à MGMTAPI.DLL, la bibliothèque API du Gestionnaire Microsoft SNMP |
| SNMPAPI.DLL  | Fournit des utilitaires SNMP                                                                      |



 

 

 





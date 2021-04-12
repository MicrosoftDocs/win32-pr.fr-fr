---
title: Configuration logicielle requise pour l’API WinSNMP
description: Une application WinSNMP doit accéder à l’API WinSNMP par le biais de la bibliothèque de liens dynamiques WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190728"
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



 

 

 





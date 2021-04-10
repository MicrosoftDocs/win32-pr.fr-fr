---
title: Création d’une liste de liaisons de variables
description: La fonction SnmpCreateVbl crée une nouvelle liste de liaisons de variables.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196898"
---
# <a name="creating-a-variable-binding-list"></a>Création d’une liste de liaisons de variables

La fonction [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crée une nouvelle liste de liaisons de variables. Si l’application WinSNMP spécifie un nom de variable et une valeur, la fonction crée la liste et ajoute le nom et la valeur comme première entrée de la liste. Si l’application spécifie la **valeur null** pour le nom de la variable, la fonction crée une liste vide.

Pour copier une liste de liaisons de variables, appelez la fonction [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . La fonction crée une nouvelle liste de liaisons de variables et initialise la nouvelle liste à l’aide d’une copie des données dans la liste de liaisons de la variable source.

La fonction [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) et la fonction [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) allouent toute mémoire nécessaire pour la nouvelle liste de liaisons de variables. L’application WinSNMP doit libérer les ressources associées à ces listes. Il est recommandé que l’application effectue cette opération en faisant correspondre chaque appel à [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) et [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) avec un appel correspondant à la fonction [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) lorsqu’il est approprié de libérer la mémoire allouée.

 

 





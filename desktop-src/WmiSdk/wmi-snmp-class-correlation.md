---
description: La corrélation affecte l’ensemble des classes retournées à partir du stockage SMIR.
ms.assetid: 799a0866-e7a0-492f-956e-b13bf591babe
ms.tgt_platform: multiple
title: Corrélation de classe SNMP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d795b7e998e3b7392baa45c23d688f1a2cef6a4069f6671d4c209788e7c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815702"
---
# <a name="wmi-snmp-class-correlation"></a>Corrélation de classe SNMP WMI

La corrélation affecte l’ensemble des classes retournées à partir du stockage SMIR. Les classes corrélées sont celles qu’un appareil SNMP donné peut prendre en charge au moment de l’énumération. L’énumération non corrélée retourne toutes les classes présentes dans le stockage SMIR, que l’appareil les prenne en charge ou non. La corrélation est une fonctionnalité du fournisseur SNMP SNMP qui peut être activée ou désactivée (par défaut).

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

La corrélation peut vous empêcher de voir toutes les classes qui sont réellement prises en charge par un appareil. Si vous savez qu’une classe particulière est prise en charge, mais qu’elle n’apparaît pas dans le stockage SMIR, cela peut être dû à plusieurs raisons, dont l’une est la corrélation. Envisagez de désactiver la corrélation avant d’écrire sur l’appareil en question. Toutefois, la désactivation de la corrélation entraîne la probabilité que de nombreuses classes non prises en charge par l’appareil s’affichent dans le stockage SMIR. En outre, il y a un coût de performance dans l’utilisation de la corrélation, car l’appareil est interrogé pour voir les classes qu’il prend en charge. Lorsque la corrélation est activée, le fournisseur SNMP provoque une énumération des classes prises en charge par l’appareil, comme le résultat de l’exécution d’un outil de *parcours MIB* .

Par exemple, un gestionnaire de réseau souhaite connaître plusieurs éléments clés de données sur tous les hubs gérés dans un réseau particulier. Une base de données des appareils actuels et leurs MIB pris en charge existent déjà. il n’est donc pas nécessaire de s’appuyer sur la fonction de corrélation de l’appareil pour fournir les éléments de données pris en charge. Dans ce cas, la corrélation peut être désactivée.

L’exemple suivant montre comment désactiver la corrélation.


```VB
set objNamedValueSet = CreateObject( _
    "WbemScripting.SWbemNamedValueSet") 
objNamedValueSet.Add "Correlate", FALSE, 0
```



en revanche, un autre gestionnaire de réseau peut souhaiter surveiller tous les lecteurs de disque de l’ordinateur UNIX sur le réseau, mais il n’est pas familiarisé avec les données MIB sur ces machines. Dans ce cas, la corrélation est activée.

 

 




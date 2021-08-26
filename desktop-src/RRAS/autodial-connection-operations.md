---
title: Opérations de connexion automatique
description: Lorsqu’une tentative de connexion à une adresse réseau échoue parce que l’hôte ne peut pas être atteint, le système recherche l’adresse dans la base de données de mappage de la numérotation automatique.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f65f62121d631dcf035e641c9d0d4d89850d7673e1c47b82ff4a4889dff49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030499"
---
# <a name="autodial-connection-operations"></a>Opérations de connexion automatique

Lorsqu’une tentative de connexion à une adresse réseau échoue parce que l’hôte ne peut pas être atteint, le système recherche l’adresse dans la base de données de mappage de la numérotation automatique. Si l’adresse est dans la base de données, le système lance une opération de numérotation automatique pour le [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)), le cas échéant, qui correspond à l’emplacement de numérotation TAPI local.

L’API RAS fournit des fonctions qui vous permettent de définir et d’interroger des paramètres de numérotation automatique qui contrôlent les connexions de numérotation automatique. Vous pouvez appeler la fonction [**RasSetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) pour activer ou désactiver la fonctionnalité de numérotation automatique pour un emplacement de numérotation TAPI spécifié. La fonction [**RasGetAutodialEnable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) indique si la fonctionnalité de numérotation automatique est activée pour un emplacement de numérotation TAPI spécifié. Pour plus d’informations sur les emplacements de numérotation TAPI, consultez la documentation relative à TAPI. Vous pouvez appeler la fonction [**RasSetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) pour définir d’autres paramètres de connexion de numérotation automatique. Par exemple, vous pouvez désactiver les connexions de numérotation automatique pour la session d’ouverture de session en cours. Appelez la fonction [**RasGetAutodialParam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) pour déterminer la valeur actuelle des paramètres de connexion de numérotation automatique.

Le système fournit une interface utilisateur par défaut pour les opérations de numérotation automatique. Toutefois, vous pouvez créer une bibliothèque de liens dynamiques (DLL) de numérotation automatique pour fournir une interface utilisateur personnalisée pour les opérations de numérotation automatique qui impliquent des entrées d’annuaire téléphonique spécifiées. Votre DLL de numérotation automatique doit exporter une version ANSI et une version Unicode d’un gestionnaire de numérotation automatique [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) .

Pour activer votre gestionnaire de numérotation automatique personnalisé pour une entrée de l’annuaire téléphonique, appelez la fonction [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour définir les propriétés de cette entrée. Les membres **szAutodialDll** et **szAutodialFunc** de la structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) passée à **RASSETENTRYPROPERTIES** spécifient le nom de votre dll de numérotation automatique et le nom de votre fonction [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) , à l’exclusion du suffixe « A » ou « W ».

Lorsque le système démarre une opération de numérotation automatique pour une entrée de l’annuaire téléphonique avec un gestionnaire de numérotation automatique personnalisé, il appelle le [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)spécifié. La fonction **RASADFunc** reçoit un pointeur vers une structure [**RASADPARAMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) qui indique l’emplacement et la fenêtre parente de la fenêtre de votre interface utilisateur. Votre **RASADFunc** peut démarrer un thread pour effectuer l’opération de numérotation personnalisée. La fonction **RASADFunc** retourne la **valeur true** pour indiquer qu’elle a pris le relais, ou **false** pour permettre au système d’effectuer la numérotation. Votre opération de numérotation personnalisée doit utiliser la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour effectuer la numérotation réelle. Une fois l’opération de numérotation terminée, l’opération de numérotation personnalisée indique la réussite ou l’échec en définissant la variable vers laquelle pointe le paramètre *lpdwRetCode* passé à [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca).

 

 
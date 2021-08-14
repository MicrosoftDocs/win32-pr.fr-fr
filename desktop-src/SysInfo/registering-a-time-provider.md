---
description: Le système charge un fournisseur de temps en fonction de ses informations de configuration stockées dans le registre.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Inscription d’un fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eeb7bce1370e443eaf3eb42d78cdfd058cf2c38147da038de1e921d85e957f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763924"
---
# <a name="registering-a-time-provider"></a>Inscription d’un fournisseur de temps

Le système charge un fournisseur de temps en fonction de ses informations de configuration stockées dans le registre. Chaque fournisseur de temps doit créer la clé de Registre suivante :

**HKEY \_ \_ \\ Système d’ordinateur local** services de \\ **CurrentControlSet** \\  \\  \\ **TimeProviders** \\ *providerName*

Le tableau suivant décrit les valeurs qui doivent exister dans la clé de chaque fournisseur.



| Valeur             | Description                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | Nom de la DLL qui contient le fournisseur. Cette valeur est du type **reg \_ SZ**.                                                                                                                                     |
| **Activé**       | Indique si le fournisseur doit être démarré. Si la valeur est 1, le fournisseur est démarré. Dans le cas contraire, le fournisseur n’est pas démarré. Cette valeur est de type **reg \_ DWORD**.                                           |
| **InputProvider** | Indique si le fournisseur est un fournisseur d’entrée ou un fournisseur de sortie. Si la valeur est 1, le fournisseur est un fournisseur d’entrée. Dans le cas contraire, le fournisseur est un fournisseur de sortie. Cette valeur est de type **reg \_ DWORD**. |



 

Le gestionnaire de fournisseurs de temps énumère les clés sous la clé **TimeProviders** et démarre chaque fournisseur activé. Les fournisseurs sont démarrés au démarrage du système et chaque fois qu’il y a des modifications de paramètres.

Chaque fournisseur de temps peut également stocker des informations de configuration spécifiques à l’application dans le registre.

 

 




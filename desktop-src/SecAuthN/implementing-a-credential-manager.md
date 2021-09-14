---
description: Répertorie les exportations de DLL qui doivent être implémentées pour créer un gestionnaire d’informations d’identification.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Implémentation d’un gestionnaire d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011298"
---
# <a name="implementing-a-credential-manager"></a>Implémentation d’un gestionnaire d’informations d’identification

Pour créer un gestionnaire d’informations d’identification, vous devez créer une DLL qui exporte les fonctions suivantes :

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Pour restaurer les notifications aux fonctions [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) et [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) pour l’ouverture de session par carte à puce, créez une entrée de Registre appelée **SmartCardLogonNotify** comme **DWORD**, puis définissez-la sur 1 :

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

**Windows Server 2003 et Windows XP :** L’entrée de Registre **SmartCardLogonNotify** n’est pas obligatoire.

En outre, les gestionnaires d’informations d’identification doivent également prendre en charge la fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) pour le démarrage de WNNC \_ (la prise en charge d’autres index n’est pas requise pour les gestionnaires d’informations d’identification). Cela indique à MPR qu’un gestionnaire d’informations d’identification démarrera. En appelant **NPGetCaps** avec le paramètre *NINDEX* défini sur WNNC \_ Start, le MPR obtient le temps d’attente avant d’appeler les fonctions de point d’entrée de gestion des informations d’identification du fournisseur. Et si le MPR dispose de ces informations, il peut le transférer au gestionnaire d’informations d’identification, en définissant le délai d’expiration.

 

 




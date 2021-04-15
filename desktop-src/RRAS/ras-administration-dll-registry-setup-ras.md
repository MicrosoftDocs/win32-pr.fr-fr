---
title: Configuration du registre des DLL d’administration RAS
description: Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant des informations sous la clé suivante dans le registre.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507406"
---
# <a name="ras-administration-dll-registry-setup"></a>Configuration du registre des DLL d’administration RAS

Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant des informations sous la clé suivante dans le registre.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

Pour inscrire la DLL, définissez les valeurs suivantes sous cette clé.



| Nom de la valeur    | Données de valeur                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | Chaîne **\_ SZ reg** qui contient le nom complet convivial de la dll. |
| *DLLPath*     | Chaîne **\_ SZ reg** contenant le chemin d’accès complet de la dll.                  |



 

Par exemple, l’entrée de Registre pour une DLL d’administration RAS d’une société fictive nommée ProElectron, Inc. peut être :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName* : **reg \_ SZ** : dll d’administration RAS ProElectron

*DllPath* : **reg \_ SZ** : C : \\ NT \\ system32 \\ntwkadm.dll

Le programme d’installation d’une DLL d’administration RAS doit également fournir des fonctionnalités de suppression/désinstallation. Si un utilisateur supprime la DLL, le programme d’installation doit supprimer les entrées de registre de la DLL.

 

 





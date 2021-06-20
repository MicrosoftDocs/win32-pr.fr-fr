---
title: Configuration du registre des DLL d’administration RAS
description: Comprendre la configuration requise pour l’inscription d’une DLL d’administration du service d’accès à distance (RAS) tierce avec RAS.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406712"
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

 

 





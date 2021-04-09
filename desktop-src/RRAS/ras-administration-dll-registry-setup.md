---
title: À propos de la configuration du registre des DLL d’administration RAS
description: Le programme d’installation d’une DLL d’administration RAS tierce doit inscrire la DLL auprès de RAS en fournissant des informations sous la clé suivante dans le registre.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- Administration RAS RRAS, configuration du registre DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103841713"
---
# <a name="about-ras-administration-dll-registry-setup"></a>À propos de la configuration du registre des DLL d’administration RAS

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



 

Étant donné que RAS prend en charge plusieurs DLL d’administration RAS, la valeur de Registre **DllPath** peut contenir une liste de chemins séparés par des points-virgules. Par exemple, l’entrée de Registre pour une DLL d’administration RAS d’une société fictive nommée ProElectron, Inc., peut être la suivante :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*: **reg \_ SZ** : dll d’administration RAS ProElectron

*DllPath*: **reg \_ SZ** : C : \\ NT \\ system32 \\ntwkadm.dll ; C : \\ NT \\ system32 \\ntwkadm2.dll

RAS appelle les dll dans l’ordre dans lequel elles sont répertoriées dans cette valeur de registre. La valeur de Registre *DisplayName* ne contient toujours qu’un seul nom d’affichage.

Le programme d’installation d’une DLL d’administration RAS doit également fournir des fonctionnalités de suppression et de désinstallation. Si un utilisateur supprime la DLL, le programme d’installation doit supprimer les entrées de Registre pour la DLL.

**Windows 2000/NT :** RAS ne prenant en charge qu’une seule DLL d’administration RAS, la valeur de Registre **DllPath** ne peut pas contenir une liste de chemins séparés par des points-virgules.

 

 





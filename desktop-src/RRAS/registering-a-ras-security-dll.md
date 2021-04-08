---
title: Inscription d’une DLL de sécurité RAS
description: Le programme d’installation d’une DLL de sécurité RAS doit inscrire la DLL auprès du serveur RAS Windows NT/Windows 2000.
ms.assetid: 90a1f30e-ea68-4859-b436-219c25016677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae856b33b2233ae114a281d96447719d9b2832
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672773"
---
# <a name="registering-a-ras-security-dll"></a>Inscription d’une DLL de sécurité RAS

Le programme d’installation d’une DLL de sécurité RAS doit inscrire la DLL auprès du serveur RAS Windows NT/Windows 2000. Une seule DLL de sécurité RAS peut être inscrite, car la prise en charge de plusieurs dll de sécurité n’est pas fournie. Pour inscrire une DLL de sécurité RAS, définissez la valeur *DllPath* sous la clé suivante dans le registre :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            SecurityHost
```



| Nom de la valeur | Données de valeur                                                                                                                                                   |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DLLPath*  | Chaîne **\_ SZ reg** qui contient le chemin d’accès de la dll. Cette chaîne doit spécifier le chemin d’accès complet, sauf si la DLL se trouve dans un répertoire listé dans le chemin d’accès système. |



 

Le programme d’installation d’une DLL de sécurité RAS doit également fournir des fonctionnalités de suppression/désinstallation. Si un utilisateur supprime la DLL, le programme d’installation doit supprimer la valeur *DllPath* du Registre. Le service RAS ne démarre pas si la valeur *DllPath* spécifie une dll qui est introuvable.

Une DLL de sécurité RAS doit exporter les fonctions [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) et [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) .

 

 





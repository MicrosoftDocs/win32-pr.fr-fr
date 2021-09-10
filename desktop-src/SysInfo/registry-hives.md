---
description: Une ruche est un groupe logique de clés, de sous-clés et de valeurs dans le Registre qui contient un ensemble de fichiers de prise en charge contenant des sauvegardes de ses données.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Ruches du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f942a275855c710de53a0d93df0b4654dd596f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368524"
---
# <a name="registry-hives"></a>Ruches du Registre

Une *ruche* est un groupe logique de clés, de sous-clés et de valeurs dans le Registre qui contient un ensemble de fichiers de prise en charge chargés en mémoire lors du démarrage du système d’exploitation ou lorsqu’un utilisateur se connecte.

Chaque fois qu’un nouvel utilisateur ouvre une session sur un ordinateur, une nouvelle ruche est créée pour cet utilisateur avec un fichier distinct pour le profil utilisateur. C’est ce que l’on appelle la *ruche du profil utilisateur*. La ruche d’un utilisateur contient des informations de Registre spécifiques relatives aux paramètres de l’application, au bureau, à l’environnement, aux connexions réseau et aux imprimantes de l’utilisateur. Les ruches de profil utilisateur se trouvent sous la clé **HKEY \_ Users** .

Les fichiers du Registre ont les deux formats suivants : standard et latest. le format standard est le seul format pris en charge par Windows 2000. elle est également prise en charge par les versions ultérieures de Windows à des fins de compatibilité descendante. le format le plus récent est pris en charge à partir de Windows XP. sur les versions de Windows qui prennent en charge le format le plus récent, les ruches suivantes utilisent toujours le format standard : **HKEY \_ CURRENT \_ USER**, **hkey \_ local \_ machine \\ SAM**, **hkey \_ local \_ machine \\ Security** et **hkey \_ users \\ . PAR défaut**; toutes les autres ruches utilisent le format le plus récent.

La plupart des fichiers de prise en charge pour les ruches se trouvent dans le répertoire% SystemRoot% \\ system32 \\ config. Ces fichiers sont mis à jour chaque fois qu’un utilisateur ouvre une session. Les extensions de nom de fichier des fichiers de ces répertoires, ou, dans certains cas, l’absence d’extension, indiquent le type de données qu’elles contiennent. Le tableau suivant répertorie ces extensions, ainsi qu’une description des données contenues dans le fichier.



| Extension       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aucun<br/> | Copie complète des données Hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| . Alt<br/> | Une copie de sauvegarde de la ruche critique du système de l' **\_ \_ ordinateur \\ local HKEY** . Seule la clé système a un fichier. Alt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Journal des transactions des modifications apportées aux clés et aux entrées de valeur dans la ruche.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| . SAV<br/> | Copie de sauvegarde d’une ruche.<br/> **Windows Server 2003 et Windows XP/2000 :** Copie des fichiers Hive tels qu’ils ont été examinés à la fin de l’étape en mode texte dans le programme d’installation. Le programme d’installation comporte deux étapes : le mode texte et le mode graphique. La ruche est copiée dans un fichier. SAV après l’étape en mode texte du programme d’installation pour la protéger contre les erreurs qui peuvent se produire en cas d’échec de la phase en mode graphique du programme d’installation. Si le programme d’installation échoue pendant l’étape en mode graphique, seule l’étape en mode graphique se répète lorsque l’ordinateur est redémarré. le fichier. SAV est utilisé pour restaurer les données Hive.<br/> |



 

Le tableau suivant répertorie les ruches standard et leurs fichiers de prise en charge.



| Ruche du Registre                      | Fichiers de prise en charge                           |
|------------------------------------|--------------------------------------------|
| **configuration de HKEY \_ Current \_**          | System, System. Alt, System. log, System. SAV |
| **HKEY \_ Current \_ User**            | Ntuser. dat, Ntuser. dat. log                 |
| **HKEY \_ Sam de l' \_ ordinateur local \\**      | Sam, Sam. log, Sam. SAV                      |
| **HKEY \_ sécurité de l' \_ ordinateur local \\** | Security, Security. log, Security. SAV       |
| **HKEY \_ logiciel de l' \_ ordinateur local \\** | Logiciel, Software. log, Software. SAV       |
| **HKEY \_ local \_ machine \\ System**   | System, System. Alt, System. log, System. SAV |
| **HKEY \_ Users \\ . VALEURS**          | Default (par défaut). log ; default. SAV          |



 

 

 





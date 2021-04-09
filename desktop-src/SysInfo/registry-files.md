---
description: Les applications peuvent enregistrer une partie du Registre dans un fichier, puis charger à nouveau le contenu du fichier dans le registre.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: Fichiers du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44916618946f6541495186aa5843799c9b864fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952163"
---
# <a name="registry-files"></a>Fichiers du Registre

Les applications peuvent enregistrer une partie du Registre dans un fichier, puis charger à nouveau le contenu du fichier dans le registre. Un fichier de Registre est utile quand une grande quantité de données est manipulée, lorsque de nombreuses entrées sont effectuées dans le registre, ou lorsque les données sont transitives et doivent être chargées, puis déchargées à nouveau. Les applications qui sauvegardent et restaurent des parties du Registre sont susceptibles d’utiliser des fichiers du Registre.

Pour enregistrer une clé et ses sous-clés et valeurs dans un fichier de Registre, une application peut appeler la fonction [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) ou [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) .

[**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) et [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) créent le fichier avec l’attribut archive. Le fichier est créé dans le répertoire actif du processus pour une clé locale, et dans le répertoire% SystemRoot% \\ system32 pour une clé distante.

Les fichiers du Registre ont les deux formats suivants : standard et latest. Le format standard est le seul format pris en charge par Windows 2000. Elle est également prise en charge par les versions ultérieures de Windows pour la compatibilité descendante. [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) crée des fichiers au format standard.

Le format le plus récent est pris en charge à partir de Windows XP. Les fichiers de Registre créés dans ce format ne peuvent pas être chargés sur Windows 2000. [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) peut enregistrer les fichiers du Registre dans l’un ou l’autre format en spécifiant le format reg \_ standard \_ ou le \_ format reg latest \_ . Par conséquent, il peut être utilisé pour convertir les fichiers de Registre qui utilisent le format standard au format le plus récent.

Pour réécrire le fichier de Registre dans le registre, une application peut utiliser les fonctions [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya), [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)ou [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) comme suit.

-   **RegLoadKey** charge les données de Registre à partir d’un fichier spécifié dans une sous-clé spécifiée sous **HKEY \_ Users** ou **HKEY \_ local \_ machine** sur l’ordinateur de l’application appelante ou sur un ordinateur distant. La fonction crée la sous-clé spécifiée si elle n’existe pas déjà. Après l’appel de cette fonction, une application peut utiliser la fonction [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) pour restaurer le registre à son état précédent.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) remplace une clé et toutes ses sous-clés et valeurs dans le registre par les données contenues dans un fichier spécifié. Les nouvelles données prennent effet lors du prochain démarrage du système.
-   [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) charge les données de Registre à partir d’un fichier spécifié dans une clé spécifiée sur l’ordinateur de l’application appelante ou sur un ordinateur distant. Cette fonction remplace les sous-clés et les valeurs inférieures à la clé spécifiée par les sous-clés et les valeurs qui suivent la clé de niveau supérieur dans le fichier.

La fonction [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) établit une connexion à un handle de Registre prédéfini sur un autre ordinateur. Une application utilise cette fonction principalement pour accéder à des informations à partir d’un Registre distant sur d’autres ordinateurs dans un environnement réseau, ce que vous pouvez également effectuer à l’aide de l’éditeur du Registre. Vous pouvez avoir besoin d’accéder à un Registre distant pour sauvegarder un registre ou en réguler l’accès réseau. Notez que vous devez disposer des autorisations appropriées pour accéder à un Registre distant à l’aide de cette fonction.

 

 




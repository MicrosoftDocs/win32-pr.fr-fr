---
title: documentation Téléphone RAS
description: les livres Téléphone fournissent une méthode standard pour collecter et spécifier les informations dont le gestionnaire de connexions d’accès à distance a besoin pour établir une connexion à distance.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Téléphone books, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba80b11696df220a904a13685855818b945794c17b9bd4233e9f897592ee7b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868419"
---
# <a name="ras-phone-books"></a>documentation Téléphone RAS

les livres Téléphone fournissent une méthode standard pour collecter et spécifier les informations dont le gestionnaire de connexions d’accès à distance a besoin pour établir une connexion à distance. Téléphone livres associent des noms d’entrée à des informations telles que des numéros de téléphone, des ports COM et des paramètres de modem. Chaque entrée de l’annuaire téléphonique contient les informations nécessaires pour établir une connexion RAS.

Téléphone livres sont stockés dans des fichiers de l’annuaire téléphonique, qui sont des fichiers texte qui contiennent les noms d’entrée et les informations associées. RAS crée un fichier d’annuaire téléphonique nommé RASPHONE. PBK. L’utilisateur peut utiliser la boîte de dialogue principale d' **accès réseau à distance** pour créer des fichiers de l’annuaire téléphonique personnel. L’API RAS ne prend pas actuellement en charge la création d’un fichier d’annuaire téléphonique. Certaines fonctions RAS, telles que la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , ont un paramètre qui spécifie un fichier d’annuaire téléphonique. Si l’appelant ne spécifie pas de fichier d’annuaire téléphonique, la fonction utilise le fichier de l’annuaire téléphonique par défaut, qui est celui sélectionné par l’utilisateur dans la feuille de propriétés préférences de l' **utilisateur** de la boîte de dialogue **accès réseau à distance** .

Windows NT 4,0 fournit les fonctions [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) et [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) qui affichent l’interface utilisateur RAS intégrée qui permet aux utilisateurs d’utiliser des annuaires téléphoniques et des entrées d’annuaire téléphonique.

**Windows 95 :** L’accès réseau à distance stocke les entrées d’annuaire téléphonique dans le registre plutôt que dans un fichier d’annuaire téléphonique. Windows 95 ne prend pas en charge les fichiers de l’annuaire téléphonique personnel ou les fonctions qui affichent les boîtes de dialogue intégrées RAS.

 

 





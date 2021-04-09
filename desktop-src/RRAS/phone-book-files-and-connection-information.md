---
title: Phone-Book les fichiers et les informations de connexion
description: Un appel RasDial doit spécifier les informations dont le gestionnaire de connexions d’accès à distance a besoin pour établir la connexion.
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d352772eec057edd6ab8c9f53640c50ea0fc73
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102136"
---
# <a name="phone-book-files-and-connection-information"></a>Phone-Book les fichiers et les informations de connexion

Un appel [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) doit spécifier les informations dont le gestionnaire de connexions d’accès à distance a besoin pour établir la connexion. En règle générale, l’appel de **rasdial** fournit les informations de connexion en spécifiant une entrée d’annuaire téléphonique. Les informations de connexion dans une entrée d’annuaire téléphonique incluent les numéros de téléphone, les vitesses en BPS, les [informations d’authentification de l’utilisateur et d'](user-authentication-information.md) [autres informations de connexion](other-connection-information.md).

Un client RAS utilise les paramètres de la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour spécifier un fichier d’annuaire téléphonique et une entrée dans ce fichier. Le paramètre *lpszPhonebookPath* peut spécifier le nom d’un fichier d’annuaire téléphonique, ou il peut avoir la **valeur null** pour indiquer que le fichier de l’annuaire téléphonique par défaut doit être utilisé. Le paramètre *lpRasDialParams* pointe vers une structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) qui spécifie le nom de l’entrée de l’annuaire téléphonique à utiliser.

Pour afficher la liste des entrées d’annuaire téléphonique à partir desquelles l’utilisateur peut sélectionner une connexion, un client RAS peut appeler la fonction [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) pour énumérer les entrées dans un fichier d’annuaire téléphonique.

Pour établir une connexion sans utiliser une entrée de l’annuaire téléphonique, l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) peut spécifier une chaîne vide pour le membre **szEntryName** de la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . Le membre **RASDIALPARAMS. szPhoneNumber** doit contenir le nombre à appeler. Dans ce cas, le gestionnaire de connexions d’accès à distance utilise le premier port de modem disponible et les valeurs par défaut pour tous les autres paramètres.

 

 
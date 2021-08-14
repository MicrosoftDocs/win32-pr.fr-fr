---
title: Autres informations de connexion
description: Les membres de la structure RASDIALPARAMS peuvent également spécifier les informations de connexion suivantes.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c596dbfb160766283beb9c48a5faf4e8258dcf0361ad7a504188a29207c0500f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789930"
---
# <a name="other-connection-information"></a>Autres informations de connexion

Les membres de la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) peuvent également spécifier les informations de connexion suivantes.

-   Un numéro de téléphone pour remplacer le numéro dans l’entrée de l’annuaire téléphonique.
-   Numéro de téléphone de [rappel](callback-connections.md) que le serveur distant peut rappeler pour établir la connexion.
-   Nom du domaine de réseau distant sur lequel l’authentification doit se produire.

Pour le numéro de rappel et le domaine, les membres [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) peuvent indiquer que le service d’accès à distance doit utiliser les informations de l’entrée de l’annuaire téléphonique, ou il peut fournir des informations qui remplacent les données de l’annuaire téléphonique.

Un client RAS peut utiliser le paramètre *lpRasDialExtensions* de la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour déterminer si RAS utilise un préfixe ou un suffixe de numéro de téléphone spécifié dans une entrée d’annuaire téléphonique.

 

 
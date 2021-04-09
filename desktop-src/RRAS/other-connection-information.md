---
title: Autres informations de connexion
description: Les membres de la structure RASDIALPARAMS peuvent également spécifier les informations de connexion suivantes.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941098"
---
# <a name="other-connection-information"></a>Autres informations de connexion

Les membres de la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) peuvent également spécifier les informations de connexion suivantes.

-   Un numéro de téléphone pour remplacer le numéro dans l’entrée de l’annuaire téléphonique.
-   Numéro de téléphone de [rappel](callback-connections.md) que le serveur distant peut rappeler pour établir la connexion.
-   Nom du domaine de réseau distant sur lequel l’authentification doit se produire.

Pour le numéro de rappel et le domaine, les membres [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) peuvent indiquer que le service d’accès à distance doit utiliser les informations de l’entrée de l’annuaire téléphonique, ou il peut fournir des informations qui remplacent les données de l’annuaire téléphonique.

Un client RAS peut utiliser le paramètre *lpRasDialExtensions* de la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour déterminer si RAS utilise un préfixe ou un suffixe de numéro de téléphone spécifié dans une entrée d’annuaire téléphonique.

 

 
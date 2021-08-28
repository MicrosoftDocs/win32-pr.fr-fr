---
description: Définit un profil haut débit mobile.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Référence du schéma de profil haut débit mobile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82fd085264747807578a260cb7cf0ed254dec7d55a375a77fe022f064e51e9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035767"
---
# <a name="mobile-broadband-profile-schema-reference"></a>Référence du schéma de profil haut débit mobile

Le schéma de profil haut débit mobile définit un profil haut débit mobile.

Les profils stockent les paramètres de configuration réseau et d’utilisateur liés à la connexion haut débit mobile. Ils stockent également les préférences utilisateur pour une connexion.

L’élément racine d’un profil haut débit mobile est l’élément [**MBNProfile**](schema-mbnprofile-element.md) . Chaque profil a un seul élément racine. tous les éléments de schéma de profil de haut débit Mobile utilisés par Windows 7 se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WWAN/profile/v1` et les éléments utilisés par Windows 8 se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WWAN/profile/v2` .

Le schéma de profil haut débit mobile impose strictement l’ordre des nœuds. Les nœuds spécifiés dans un profil doivent adhérer au **schéma de profil haut débit mobile** et s’afficher dans l’ordre indiqué dans la définition de schéma. Par exemple, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) doit être spécifié immédiatement après [**AccessString**](schema-accessstring-contexttype-element.md).

-   [Schéma de profil de haut débit mobile v1](mobile-broadband-profile-schema.md)
-   [Schéma de profil haut débit mobile v2](mobile-broadband-profile-schema-v2.md)
-   [Schéma de profil haut débit mobile v3](mobile-broadband-profile-schema-v3.md)
-   [V4 de schéma de profil haut débit mobile](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))

 

 

---
description: 'Pour publier une application en fonction de l’installation par utilisateur lorsque l’application requiert des privilèges élevés (c’est-à-dire système) pour l’installation, utilisez les instructions de la liste suivante :'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Publication d’une application Per-User à installer avec des privilèges élevés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdced246f90a345b5b2cc599541119a26e29e4d9a1d708be1ee8299d55d3c28d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082959"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Publication d’une application Per-User à installer avec des privilèges élevés

Pour publier une application en fonction de l’installation par utilisateur lorsque l’application requiert des privilèges élevés (c’est-à-dire système) pour l’installation, utilisez les instructions de la liste suivante :

-   votre processus doit être un service qui s’exécute sous le compte système LocalSystem sur Windows XP ou version ultérieure.
-   Générez un script de publication en appelant [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) ou [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).
-   Votre processus doit emprunter l’identité de l’utilisateur qui est la cible de la publication.
-   Appelez [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)et utilisez les \_ raccourcis SCRIPTFLAGS CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ appinfo \| SCRIPTFLAGS \_ \_ \| \_ REGDATA CNFGINFO SCRIPTFLAGS.

Lorsque vous suivez les instructions, vous publiez une application auprès d’un utilisateur spécifié et, lorsque l’utilisateur choisit d’installer, l’application est installée avec des privilèges élevés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise à jour corrective des applications gérées par utilisateur](patching-per-user-managed-applications.md)
</dt> </dl>

 

 




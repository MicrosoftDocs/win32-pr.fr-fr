---
title: Syntaxe de chaîne (temps généralisé)
description: Format de chaîne d’heure défini par les normes ASN. 1. | Syntaxe de chaîne (temps généralisé)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de syntaxe de chaîne (temps généralisé)
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bf7d965b03b75f4186b807098a5262c402d0c19104a4c09357958b38a77a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580209"
---
# <a name="stringgeneralized-time-syntax"></a>Syntaxe de chaîne (temps généralisé)

Format de chaîne d’heure défini par les normes ASN. 1. Utilisez cette syntaxe pour stocker des valeurs d’heure au format Generalized-Time.

Le format de la syntaxe de Generalized-Time est « AAAAMMJJHHMMSS. 0Z ». « 20010928060000.0 Z » est un exemple de valeur acceptable. Le « Z » indique qu’il n’y a pas de différence de temps. Active Directory stocke la date/l’heure sur l’heure GMT (Greenwich Mean Time). Si aucune différence de temps n’est spécifiée, la valeur par défaut est GMT.

Si l’heure est spécifiée dans un fuseau horaire différent de GMT, la différence entre le fuseau horaire et l’heure GMT est ajoutée à la chaîne au lieu de « Z » sous la forme « AAAAMMJJHHMMSS. 0 \[ +/- \] hhmm ». « 20010928060000.0 + 0200 » est un exemple de valeur acceptable. La différence est basée sur la formule suivante : GMT = local + différentielle.

Pour plus d’informations, consultez ISO 8601 et X680.



| Entrée | Valeur |
|--------------|----------------------------------------------------------------------------|
| Name         | String(Generalized-Time)                                                   |
| ID de syntaxe    | 2.5.5.11                                                                   |
| ID OM        | 24                                                                         |
| Type MAPI    | SYSTIME                                                                    |
| Type ADS     | \_heure UTC \_ ADSTYPE                                                         |
| Type de variante | \_Date VT                                                                   |
| SDS, type     | [System.DateTime](/dotnet/api/system.datetime) |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[System.DateTime](/dotnet/api/system.datetime)
</dt> </dl>

 

 

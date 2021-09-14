---
description: 'Pour obtenir un handle vers un volume en vue d’une utilisation avec des opérations de journal des modifications du numéro de séquence de mise à jour (USN), appelez la fonction CreateFile avec le paramètre lpFileName défini sur une chaîne au format suivant : \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Obtention d’un handle de volume pour les opérations de journal des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009893"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Obtention d’un handle de volume pour les opérations de journal des modifications

Pour obtenir un handle vers un volume en vue d’une utilisation avec des opérations de journal des modifications du numéro de séquence de mise à jour (USN), appelez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec le paramètre *lpFileName* défini sur une chaîne au format suivant : \\ \\ . \\ *X*:

Notez que *X* est la lettre qui identifie le lecteur sur lequel le volume NTFS s’affiche.

Si le volume n’a pas de lettre de lecteur, utilisez la syntaxe décrite dans [attribution d’un nom à un volume](naming-a-volume.md).

 

 




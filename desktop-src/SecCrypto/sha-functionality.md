---
description: Le fournisseur de base d’origine a signalé de manière incorrecte que l’algorithme de hachage SHA énumère les algorithmes par des appels à CryptGetProvParam avec le paramètre PP \_ ENUMALGS spécifié.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Fonctionnalité SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749557"
---
# <a name="sha-functionality"></a>Fonctionnalité SHA

Le fournisseur de base d’origine a signalé de manière incorrecte que l’algorithme de hachage [*SHA*](../secgloss/s-gly.md) énumère les algorithmes par des appels à [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec le paramètre pp \_ ENUMALGS spécifié. Ce problème a été résolu dans le fournisseur de base. Le fournisseur de base révisé et le fournisseur étendu et signalent désormais correctement SHA-1.

Une \_ constante SHA1 CALG définie a été ajoutée à Wincrypt. h avec la même valeur que CALG \_ Sha.

 

 

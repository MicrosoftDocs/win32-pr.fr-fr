---
description: Le fournisseur de base d’origine a signalé de manière incorrecte que l’algorithme de hachage SHA énumère les algorithmes par des appels à CryptGetProvParam avec le paramètre PP \_ ENUMALGS spécifié.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Fonctionnalité SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728415b746681121593a3e93f62a66168e59ca49b6f7737b6f39565ba00200d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900329"
---
# <a name="sha-functionality"></a>Fonctionnalité SHA

Le fournisseur de base d’origine a signalé de manière incorrecte que l’algorithme de hachage [*SHA*](../secgloss/s-gly.md) énumère les algorithmes par des appels à [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec le paramètre pp \_ ENUMALGS spécifié. Ce problème a été résolu dans le fournisseur de base. Le fournisseur de base révisé et le fournisseur étendu et signalent désormais correctement SHA-1.

Une \_ constante SHA1 CALG définie a été ajoutée à Wincrypt. h avec la même valeur que CALG \_ Sha.

 

 

---
title: Génération d’une boîte de dialogue pour la sélection de formats restreints
description: Génération d’une boîte de dialogue pour la sélection de formats restreints
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Gestionnaire de compression audio (ACM), génération de boîtes de dialogue
- ACM (gestionnaire de compression audio), génération de boîtes de dialogue
- Exemples ACM, génération de boîtes de dialogue
- génération de boîtes de dialogue
- acmFormatChoose fonction)
- Gestionnaire de compression audio (ACM), sélection de formats restreints
- ACM (gestionnaire de compression audio), sélection de formats restreints
- Exemples ACM, sélection de formats restreints
- sélection de formats restreints
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119481"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Génération d’une boîte de dialogue pour la sélection de formats restreints

Vous pouvez utiliser la boîte de dialogue créée par la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , mais limiter ou contrôler les formats dans la boîte de dialogue. Pour ce faire, vous pouvez utiliser l' \_ indicateur ACMFORMATCHOOSE STYLEF \_ ENABLEHOOK pour raccorder la procédure de dialogue. L’application peut ensuite filtrer les formats en répondant au message [**mm \_ ACM \_ FORMATCHOOSE**](mm-acm-formatchoose.md) dans la procédure de message de la boîte de dialogue.

 

 





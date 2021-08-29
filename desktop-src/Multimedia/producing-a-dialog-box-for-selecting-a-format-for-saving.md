---
title: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
description: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Gestionnaire de compression audio (ACM), génération de boîtes de dialogue
- ACM (gestionnaire de compression audio), génération de boîtes de dialogue
- Exemples ACM, génération de boîtes de dialogue
- génération de boîtes de dialogue
- acmFormatChoose fonction)
- Gestionnaire de compression audio (ACM), sélection du format d’enregistrement
- ACM (gestionnaire de compression audio), sélection du format d’enregistrement
- Exemples ACM, sélection du format d’enregistrement
- sélection du format d’enregistrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65288e4a15712ec86bcf48a8f8088da9f6d5944f298119b21766be238168bf3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805775"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a>Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement

Vous pouvez souhaiter qu’une application enregistre les données Waveform-Audio existantes dans un autre format. Par exemple, un éditeur Wave audio peut enregistrer un fichier Waveform-Audio sous forme de fichier compressé. Pour répertorier uniquement les formats de destination suggérés pour un format source spécifié dans la boîte de dialogue créée par la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , spécifiez le format de la source dans le membre **pwfxEnum** et l' \_ \_ indicateur de suggestion FORMATENUMF de l’ACM dans le membre **fdwEnum** de la structure [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .

De même, pour répertorier les formats de destination valides pour un format spécifié, utilisez l' \_ indicateur ACM FORMATENUMF \_ Convert au lieu de l' \_ indicateur de suggestion FORMATENUMF ACM \_ .

 

 





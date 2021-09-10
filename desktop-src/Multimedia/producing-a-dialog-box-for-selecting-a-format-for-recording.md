---
title: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
description: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Gestionnaire de compression audio (ACM), génération de boîtes de dialogue
- ACM (gestionnaire de compression audio), génération de boîtes de dialogue
- Exemples ACM, génération de boîtes de dialogue
- génération de boîtes de dialogue
- acmFormatChoose fonction)
- Audio Compression Manager (ACM), sélection du format de recodage
- ACM (gestionnaire de compression audio), sélection du format de recodage
- Exemples ACM, sélection du format de recodage
- sélection du format de recodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364064"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement

Une application peut permettre à l’utilisateur de sélectionner un format pour lequel un périphérique Wave-Audio installé fournit une prise en charge native. Par exemple, vous souhaiterez peut-être qu’un éditeur Wave Audio enregistre de nouvelles données audio Waveform sans utiliser de compresseur ou décompresseur ACM pour fournir une couche de traduction. Pour ce faire, utilisez la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , en spécifiant le \_ matériel ACM FORMATENUMF et les \_ \_ \_ indicateurs d’entrée ACM FORMATENUMF dans le membre **fdwEnum** de la structure [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .

 

 





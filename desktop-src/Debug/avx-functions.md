---
description: Fonctions Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: AVX, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d4645fc9869931e094fa6fd84a8c5b79b1ff09a6fcfd65df3f3b043fe84573
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815609"
---
# <a name="avx-functions"></a>AVX, fonctions

Les fonctions Intel AVX sont les suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                   | Description                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**CopyContext**](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | Copie une structure de contexte source (y compris les XState) dans une structure de contexte de destination initialisée.<br/>         |
| [**GetEnabledXStateFeatures**](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | Obtient un masque de fonctionnalités XState activées sur des processeurs x86 ou x64.<br/>                                                    |
| [**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | Retourne le masque des fonctionnalités XState définies dans une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .<br/>                        |
| [**InitializeContext**](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | Initialise une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) à l’intérieur d’une mémoire tampon avec la taille et l’alignement nécessaires.<br/>       |
| [**LocateXStateFeature**](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | Récupère un pointeur vers l’état du processeur pour une fonctionnalité XState dans une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .<br/> |
| [**SetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | Définit le masque des fonctionnalités XState définies dans une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .<br/>                             |



 

 

 





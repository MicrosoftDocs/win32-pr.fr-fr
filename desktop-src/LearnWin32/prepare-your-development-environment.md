---
title: Préparer votre environnement de développement
description: Préparer votre environnement de développement
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094310"
---
# <a name="prepare-your-development-environment"></a>Préparer votre environnement de développement

pour écrire un programme Windows en C ou C++, vous devez installer le kit de développement logiciel (SDK) de Microsoft Windows ou Microsoft Visual Studio. le SDK Windows contient les en-têtes et les bibliothèques nécessaires à la compilation et à la liaison de votre application. le SDK Windows contient également des outils en ligne de commande pour générer des applications Windows, y compris le compilateur Visual C++ et l’éditeur de liens. bien que vous puissiez compiler et générer Windows des programmes avec les outils en ligne de commande, nous vous recommandons d’utiliser Microsoft Visual Studio. vous pouvez télécharger gratuitement des Visual Studio Community ou des versions d’évaluation gratuites d’autres versions de Visual Studio [ici](https://visualstudio.microsoft.com/downloads/).

chaque version de la SDK Windows cible la dernière version de Windows, ainsi que plusieurs versions précédentes. les notes de publication répertorient les plateformes prises en charge, mais sauf si vous gérez une application pour une version très ancienne de Windows, vous devez installer la dernière version du SDK Windows. vous pouvez télécharger les SDK Windows les plus récentes [ici](https://developer.microsoft.com/windows/downloads/windows-10-sdk).

le SDK Windows prend en charge le développement d’applications 32 bits et 64 bits. les api Windows sont conçues afin que le même code puisse être compilé pour 32 bits ou 64 bits sans modification.

> [!Note]  
> le SDK Windows ne prend pas en charge le développement de pilotes matériels, et cette série ne traite pas du développement des pilotes. pour plus d’informations sur l’écriture d’un pilote matériel, consultez [Prise en main avec des pilotes Windows](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Suivant

[Windows Conventions de codage](windows-coding-conventions.md)

## <a name="related-topics"></a>Rubriques connexes

* [Télécharger Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [télécharger SDK Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
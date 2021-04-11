---
title: Préparer votre environnement de développement
description: Préparer votre environnement de développement
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314933"
---
# <a name="prepare-your-development-environment"></a>Préparer votre environnement de développement

Pour écrire un programme Windows en C ou C++, vous devez installer le kit de développement logiciel (SDK) Microsoft Windows ou Microsoft Visual Studio. Le SDK Windows contient les en-têtes et les bibliothèques nécessaires à la compilation et à la liaison de votre application. Le SDK Windows contient également des outils en ligne de commande pour la génération d’applications Windows, notamment le compilateur Visual C++ et l’éditeur de liens. Bien que vous puissiez compiler et générer des programmes Windows avec les outils en ligne de commande, nous vous recommandons d’utiliser Microsoft Visual Studio. Vous pouvez télécharger un téléchargement gratuit de Visual Studio Community ou des versions d’évaluation gratuites d’autres versions de Visual Studio [ici](https://visualstudio.microsoft.com/downloads/).

Chaque version de la SDK Windows cible la version la plus récente de Windows, ainsi que plusieurs versions précédentes. Les notes de publication répertorient les plateformes prises en charge, mais sauf si vous gérez une application pour une très ancienne version de Windows, vous devez installer la dernière version de la SDK Windows. Vous pouvez télécharger les SDK Windows les plus récentes [ici](https://developer.microsoft.com/windows/downloads/windows-10-sdk).

Le SDK Windows prend en charge le développement d’applications 32 bits et 64 bits. Les API Windows sont conçues de façon à ce que le même code puisse être compilé pour 32 bits ou 64 bits sans modification.

> [!Note]  
> Le SDK Windows ne prend pas en charge le développement de pilotes matériels, et cette série ne traite pas du développement des pilotes. Pour plus d’informations sur l’écriture d’un pilote matériel, consultez [prise en main avec les pilotes Windows](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Suivant

[Conventions de codage Windows](windows-coding-conventions.md)

## <a name="related-topics"></a>Rubriques connexes

* [Télécharger Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Télécharger SDK Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
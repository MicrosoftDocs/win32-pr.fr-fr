---
description: Cette rubrique décrit les différences entre les versions binaires de la bibliothèque Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Version de la bibliothèque à référencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312869"
---
# <a name="which-library-version-to-reference"></a>Version de la bibliothèque à référencer

Cette rubrique décrit les différences entre les versions binaires de la bibliothèque Tablet PC.

## <a name="tablet-pc-library-versions"></a>Versions de la bibliothèque Tablet PC

les fichiers binaires de la bibliothèque Tablet PC (Microsoft.Ink.dll) ont été mis à jour dans Windows Vista. ces fichiers binaires sont appelés « version 6,0 » pour incide avec la version de Windows dans laquelle ils sont publiés.

la version la plus récente des fichiers binaires compatibles avec Windows XP est appelée « version 1,7 ».

le SDK Windows peut être installé sur les ordinateurs Vista et XP, et le SDK Windows comprend les deux versions de Microsoft.Ink.dll.

Celles-ci sont installées dans :

1. % ProgramFiles% \\ assemblys de référence \\ Microsoft \\ Tablet \\ PC v 1.7 \\Microsoft.Ink.dll

2. % ProgramFiles% \\ assemblys de référence \\ Microsoft \\ Tablet \\ PC v 6.0 \\Microsoft.Ink.dll

les fichiers binaires de version 6,0 sont uniquement compatibles avec Windows vista, et les applications écrites pour eux doivent uniquement être exécutées sur Windows Vista.

une application écrite avec les binaires de la version 1,7 doit s’exécuter sans modification quand elle est installée sur Windows Vista.

 

 




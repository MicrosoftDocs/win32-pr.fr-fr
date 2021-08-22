---
description: Cette rubrique décrit les différences entre les versions binaires de la bibliothèque Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Version de la bibliothèque à référencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899866dd11bbe72f9476ee3b645ed4e5612fe7043dae38675bd206e81562ca68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589279"
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

 

 




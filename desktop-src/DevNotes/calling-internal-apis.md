---
description: Le fichier d’en-tête winternl. h expose les prototypes des API Windows internes. Étant donné qu’il n’y a pas de bibliothèque d’importation associée, les développeurs doivent utiliser la liaison dynamique au moment de l’exécution pour appeler les fonctions décrites dans ce fichier d’en-tête.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Appel d’API internes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950578"
---
# <a name="calling-internal-apis"></a>Appel d’API internes

Le fichier d’en-tête winternl. h expose les prototypes des API Windows internes. Étant donné qu’il n’y a pas de bibliothèque d’importation associée, les développeurs doivent utiliser la liaison dynamique au moment de l’exécution pour appeler les fonctions décrites dans ce fichier d’en-tête.

Les fonctions et structures dans winternl. h sont internes au système d’exploitation et peuvent être modifiées d’une version de Windows à l’autre, voire entre les service packs pour chaque version. Pour maintenir la compatibilité de votre application, vous devez utiliser à la place les fonctions publiques équivalentes. Des informations supplémentaires sont disponibles dans le fichier d’en-tête, winternl. h, ainsi que la documentation de chaque fonction.

Si vous utilisez ces fonctions, vous pouvez y accéder via la liaison dynamique au moment de l’exécution à l’aide de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Cela donne à votre code la possibilité de répondre correctement si la fonction a été modifiée ou supprimée du système d’exploitation. Toutefois, les modifications de signature peuvent ne pas être détectables.

 

 

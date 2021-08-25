---
title: Création d’un Flux temporaire
description: Création d’un Flux temporaire
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate fonction)
- AVIStreamRelease fonction)
- AVIMakeCompressedStream fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33ce8d4ec6fd88a7283588d35955432cbe01a4855565928dca83d40afa8b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785699"
---
# <a name="creating-temporary-streams"></a>Création d’un Flux temporaire

Les flux temporaires peuvent être bénéfiques de plusieurs façons. Vous pouvez utiliser un flux temporaire comme flux de travail, par exemple, lors de la modification du format de flux. Ou vous pouvez créer un flux temporaire pour contenir des parties d’autres flux qui ont été copiés.

Vous pouvez créer un flux en mémoire qui n’est associé à aucun fichier à l’aide de la fonction [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) . Cette fonction retourne l’adresse de l’interface au nouveau flux à un emplacement spécifié et est utilisée en interne par d’autres fonctions qui créent des flux temporaires.

Vous pouvez créer un flux compressé à partir d’un flux non compressé à l’aide de la fonction [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) . Vous identifiez le flux à compresser, la méthode de compression et les options de compression, ainsi que le gestionnaire du nouveau flux.

Lorsque vous avez fini d’utiliser un flux créé avec **AVIStreamCreate** ou **AVIMakeCompressedStream**, fermez le flux à l’aide de la fonction [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . **AVIStreamRelease** libère les ressources utilisées par le flux temporaire.

 

 





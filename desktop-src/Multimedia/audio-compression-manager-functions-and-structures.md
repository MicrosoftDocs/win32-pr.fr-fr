---
title: Fonctions et structures du gestionnaire de compression audio
description: Fonctions et structures du gestionnaire de compression audio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- audio multimédia, fonctions ACM
- audio, fonctions ACM
- le gestionnaire de compression audio (ACM), fonctions
- ACM (gestionnaire de compression audio), fonctions
- audio multimédia, structures ACM
- audio, structures ACM
- le gestionnaire de compression audio (ACM), structures
- ACM (gestionnaire de compression audio), structures
- Structures ACM
- Fonctions ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007281"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Fonctions et structures du gestionnaire de compression audio

Les fonctions ACM se répartissent en plusieurs catégories. Les conventions d’affectation des noms pour les fonctions facilitent l’identification de ces catégories. Les noms de fonctions (à deux exceptions près) se présentent sous la forme *acmGroupFunction*, où *Group* désigne la catégorie ACM (telle que « Driver », « format », « FormatTag », « Filter », « FilterTag » ou « Stream ») et *Function* décrit l’action effectuée par la fonction.

Les fonctions dans les groupes de filtres et de formats sont très similaires. Presque toutes les fonctions qui agissent sur les filtres possèdent une fonction parallèle qui agit sur les formats.

Dans le groupe format, certaines fonctions utilisent des balises de format Waveform-Audio (le membre **wFormatTag** d’une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ), tandis que d’autres requièrent des formats audio Wave complets (la structure **WAVEFORMATEX** complète). (Pour obtenir des informations de référence sur la structure **WAVEFORMATEX** , consultez [erreur](error.md).)

Dans le groupe filtre, certaines fonctions utilisent des balises de filtre Waveform-Audio (le membre **dwFilterTag** d’une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), tandis que d’autres requièrent des filtres Wave-audio complets (la structure **WAVEFILTER** complète).

Les fonctions du groupe de flux représentent les nombreuses étapes impliquées dans une conversion : ouverture d’une instance de conversion, préparation de la conversion, exécution de la conversion, nettoyage après la conversion terminée et fermeture de l’instance de conversion.

 

 
---
title: Gestion des erreurs avec les fonctions audio
description: Gestion des erreurs avec les fonctions audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimédia, erreurs audio de forme d’onde
- Erreurs audio, audio Wave
- audio multimédia, erreurs audio auxiliaires
- audio, erreurs audio auxiliaires
- sons Waveform, Erreurs
- audio auxiliaire, Erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbb332ed0be06a829c169bdf333f3f4ce73a6e9dff81b22949174216dd4017d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141082"
---
# <a name="handling-errors-with-audio-functions"></a>Gestion des erreurs avec les fonctions audio

Les fonctions Wave-audio et auxiliaire-audio retournent une valeur différente de zéro lorsqu’une erreur se produit. Windows fournit des fonctions qui convertissent ces valeurs d’erreur en descriptions textuelles des erreurs. L’application doit toujours examiner les valeurs d’erreur pour déterminer comment procéder, mais les descriptions textuelles des erreurs peuvent être utilisées dans les boîtes de dialogue qui décrivent les erreurs aux utilisateurs.

Vous pouvez utiliser les fonctions suivantes pour récupérer les descriptions textuelles des valeurs d’erreur audio :



| Fonction                                           | Description                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Récupère une description textuelle d’une erreur d’entrée audio Wave spécifiée.  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Récupère une description textuelle d’une erreur de sortie Wave-Audio spécifiée. |



 

Les seules fonctions audio qui ne retournent pas de valeurs d’erreur sont [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)et [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs). Ces fonctions retournent zéro si aucun appareil n’est présent dans un système ou si elles rencontrent des erreurs.

 

 
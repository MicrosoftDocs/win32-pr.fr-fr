---
title: Opérations de réseau DRM
description: Opérations de réseau DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media Format SDK, DRM Network Operations
- ASF (Advanced Systems Format), opérations de réseau DRM
- ASF (format de systèmes avancés), opérations de réseau DRM
- gestion des droits numériques (DRM), opérations réseau
- DRM (gestion des droits numériques), opérations réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f026ed972b88a1e6290bdd513012c2fab758da2c5b4b91a6a1162df5d258207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771749"
---
# <a name="drm-network-operations"></a>Opérations de réseau DRM

Plusieurs opérations DRM requièrent que votre application se connecte à un service s’exécutant sur un réseau. Ces opérations incluent l’individualisation, l’acquisition de licence, la révocation de licence et la sauvegarde et la restauration de licence.

Comme pour toute transaction réseau, votre application doit prendre en compte de nombreuses difficultés lors de l’inclusion de fonctionnalités nécessitant des opérations réseau. Votre application doit suivre l’état de l’opération dans l’étendue qui est possible pour la fonctionnalité spécifique, généralement en gérant les messages d’État. Vous devez fournir des commentaires à l’utilisateur sur l’État. Si une opération échoue à la première tentative, vous devez permettre à l’utilisateur de réessayer. Dans de nombreux cas, la première tentative rencontre des difficultés, mais une tentative suivante se termine sans erreur.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 





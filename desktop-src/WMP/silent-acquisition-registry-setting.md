---
title: Paramètre de registre d’acquisition en mode silencieux
description: Paramètre de registre d’acquisition en mode silencieux
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510218"
---
# <a name="silent-acquisition-registry-setting"></a>Paramètre de registre d’acquisition en mode silencieux

Le lecteur Microsoft Windows Media utilise la valeur de Registre suivante pour déterminer s’il faut activer l’acquisition en mode silencieux, un État dans lequel le lecteur télécharge automatiquement les droits d’utilisation lorsque l’utilisateur lit ou synchronise le contenu protégé.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **MediaPlayer** \\ **Préférences** \\ **SilentAcquisition**

La valeur SilentAcquisition se présente sous la forme suivante :



| Nom              | Type           | Description                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **\_valeur DWORD reg** | Définissez cette valeur sur 1 pour activer l’acquisition en mode silencieux ou sur 0 pour désactiver l’acquisition en mode silencieux. La valeur par défaut est 1. |



 

Pour spécifier une valeur, l’utilisateur peut démarrer le lecteur Windows Media, ouvrir la boîte de dialogue **options** , cliquer sur l’onglet **confidentialité** , puis activer ou désactiver la case à cocher **Télécharger automatiquement les droits d’utilisation lors de la lecture ou de la synchronisation d’un fichier** . La sélection de cette case à cocher affecte la valeur 1 à SilentAcquisition. la désactivation de la case à cocher lui affecte la valeur 0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 





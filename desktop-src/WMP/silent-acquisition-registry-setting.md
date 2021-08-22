---
title: Paramètre de registre d’acquisition en mode silencieux
description: Paramètre de registre d’acquisition en mode silencieux
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bdab93c58dd92b5f0522f26ea192150cad4a44ae9a6edfbd0bde770f07a0262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507959"
---
# <a name="silent-acquisition-registry-setting"></a>Paramètre de registre d’acquisition en mode silencieux

Microsoft Lecteur Windows Media utilise la valeur de registre suivante pour déterminer s’il faut activer l’acquisition en mode silencieux, un état dans lequel le lecteur télécharge automatiquement les droits d’utilisation lorsque l’utilisateur lit ou synchronise le contenu protégé.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **MediaPlayer** \\ **Préférences** \\ **SilentAcquisition**

La valeur SilentAcquisition se présente sous la forme suivante :



| Name              | Type           | Description                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **\_valeur DWORD reg** | Définissez cette valeur sur 1 pour activer l’acquisition en mode silencieux ou sur 0 pour désactiver l’acquisition en mode silencieux. La valeur par défaut est 1. |



 

pour spécifier une valeur, l’utilisateur peut démarrer Lecteur Windows Media, ouvrir la boîte de dialogue **Options** , cliquer sur l’onglet **confidentialité** , puis activer ou désactiver la case à cocher **télécharger automatiquement les droits d’utilisation lors de la lecture ou de la synchronisation d’un fichier** . La sélection de cette case à cocher affecte la valeur 1 à SilentAcquisition. la désactivation de la case à cocher lui affecte la valeur 0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> </dl>

 

 





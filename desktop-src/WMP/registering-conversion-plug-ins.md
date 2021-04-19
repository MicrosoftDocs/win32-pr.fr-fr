---
title: Inscription des plug-ins de conversion
description: Inscription des plug-ins de conversion
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Lecteur Windows Media, plug-ins de conversion
- Plug-ins du lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, inscription
- Registre, plug-ins de conversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513459"
---
# <a name="registering-conversion-plug-ins"></a>Inscription des plug-ins de conversion

Les formats tiers doivent être inscrits avant que le lecteur Windows Media puisse instancier et utiliser le plug-in de conversion. Pour inscrire votre fichier à des fins de conversion, vous devez inscrire l’extension de nom de fichier associée à votre format.

La liste des extensions de nom de fichier inscrites est conservée sous la forme d’un ensemble de clés de registre. Pour plus d’informations sur l’inscription de formats tiers, consultez Paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md). Le tableau suivant répertorie les paramètres de valeur de Registre permettant d’inscrire un format tiers pour la conversion à l’aide d’un plug-in de conversion.



| Valeur                  | Paramètre                                                     |
|------------------------|-------------------------------------------------------------|
| **Runtime**            | 13                                                          |
| **autorisations**        | 8 (autorisation pour la bibliothèque).                             |
| **ConvertPluginCLSID** | ID de classe du plug-in de conversion, au format de registre. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de plug-ins de conversion**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 





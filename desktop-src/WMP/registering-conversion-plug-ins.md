---
title: Inscription des plug-ins de conversion
description: Inscription des plug-ins de conversion
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Lecteur Windows Media, plug-ins de conversion
- plug-ins Lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, inscription
- Registre, plug-ins de conversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e6741a27c665b8a99cda2c756fa28cbdbb16f92564f26c16e077c5c5be8859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861539"
---
# <a name="registering-conversion-plug-ins"></a>Inscription des plug-ins de conversion

les formats tiers doivent être inscrits avant Lecteur Windows Media pouvez instancier et utiliser le plug-in de conversion. Pour inscrire votre fichier à des fins de conversion, vous devez inscrire l’extension de nom de fichier associée à votre format.

La liste des extensions de nom de fichier inscrites est conservée sous la forme d’un ensemble de clés de registre. pour plus d’informations sur l’inscription de formats tiers, consultez [Paramètres du registre](file-name-extension-registry-settings.md)de l’Extension de nom de fichier. Le tableau suivant répertorie les paramètres de valeur de Registre permettant d’inscrire un format tiers pour la conversion à l’aide d’un plug-in de conversion.



| Valeur                  | Paramètre                                                     |
|------------------------|-------------------------------------------------------------|
| **Runtime**            | 13                                                          |
| **Autorisations**        | 8 (autorisation pour la bibliothèque).                             |
| **ConvertPluginCLSID** | ID de classe du plug-in de conversion, au format de registre. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de plug-ins de conversion**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 





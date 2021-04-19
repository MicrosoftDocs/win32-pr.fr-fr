---
title: Pour ajouter des données de script à l’en-tête
description: Pour ajouter des données de script à l’en-tête
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK, ajout de données de script aux en-têtes
- ASF (Advanced Systems Format), ajout de données de script aux en-têtes
- ASF (format de systèmes avancés), ajout de données de script aux en-têtes
- scripts, ajout de données aux en-têtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106511065"
---
# <a name="to-add-script-data-to-the-header"></a>Pour ajouter des données de script à l’en-tête

Vous pouvez inclure des commandes de script dans l’en-tête d’un fichier ASF. Pour écrire des commandes de script dans l’en-tête au moment de l’encodage, procédez comme suit. Effectuez ces étapes avant d’appeler [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

1.  Obtenez un pointeur vers l’interface **IWMHeaderInfo** en appelant **IWMWriter :: QueryInterface**.
2.  Ajoutez chaque commande de script souhaitée en appelant [**IWMHeaderInfo :: AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript). Chaque appel prend les deux chaînes séparément et l’heure de présentation à utiliser pour la commande en tant que paramètres.

Quand une application lit le fichier, elle doit récupérer toutes les commandes de script. Pour rechercher toutes les commandes de script dans l’en-tête d’un fichier, procédez comme suit. Cette opération doit être effectuée avant de commencer la lecture.

1.  Obtenez un pointeur vers l’interface **IWMHeaderInfo** de l’objet lecteur (ou un objet lecteur synchrone) en appelant la méthode **QueryInterface** d’une autre interface dans l’objet.
2.  Récupérez le nombre total de scripts dans l’en-tête en appelant [**IWMHeaderInfo :: GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).
3.  Parcourez l’ensemble des scripts de l’en-tête un par un en utilisant des appels à [**IWMHeaderInfo :: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).
4.  Créez une liste des heures de présentation afin que votre application puisse réagir aux commandes au moment opportun.

> [!Note]  
> Lorsque vous utilisez DRM pour chiffrer un fichier, aucune commande de script ne peut avoir une heure de présentation de 0.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Utilisation des commandes de script**](using-script-commands.md)
</dt> </dl>

 

 





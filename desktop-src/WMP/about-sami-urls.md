---
title: À propos des URL SAMI
description: À propos des URL SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Fichiers de Media Interchange (SAMI) synchronisés, fichiers
- SAMI (Synchronized Accessible Media Interchange), fichiers
- SAMI (Synchronized Accessible Media Interchange), URL
- SAMI (Synchronized Accessible Media Interchange), URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196590"
---
# <a name="about-sami-urls"></a>À propos des URL SAMI

Les fichiers SAMI peuvent être associés à des fichiers multimédias numériques à l’aide d’une URL unique. Pour ce faire, utilisez *le* paramètre d’URL sami. Le paramètre d’URL est précédé de l’URL de base et d’un ? . Une URL avec un paramètre *sami* respecte la syntaxe suivante :

*URL*? *same* = *captionsURL*.

La valeur du paramètre URL suit le nom du paramètre et le signe égal, comme dans l’exemple suivant :


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Cette syntaxe d’URL est couramment utilisée dans un lien hypertexte ou un métafichier Windows Media pour établir une liaison directe avec les emplacements du fichier multimédia numérique et du fichier SAMI. Lorsque l’utilisateur clique sur le lien hypertexte, le lecteur Windows Media démarre en mode complet et lit le contenu multimédia numérique.

Si le paramètre d’URL *sami* n’est pas spécifié, le lecteur Windows Media recherche un fichier sami qui se trouve dans le même emplacement que le fichier multimédia numérique et qui porte le même nom de fichier, à l’exception de l’extension de nom de fichier, qui doit être. SMI. Si un tel fichier est présent, il est automatiquement ouvert si l’affichage des sous-titres a été activé dans le lecteur.

Les sous-titres sont activés dans le lecteur Windows Media en cliquant sur le menu **lire** , puis en cliquant sur **légendes et** sous-titres, puis en cliquant **sur activé**. Si les sous-titres sont activés, les légendes contenues dans le fichier SAMI s’affichent pendant la lecture de l’élément multimédia.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 





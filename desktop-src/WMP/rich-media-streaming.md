---
title: Diffusion multimédia enrichie
description: Diffusion multimédia enrichie
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Lecteur Windows Media, présentations basées sur le Web
- modèle objet Lecteur Windows Media, présentations basées sur le Web
- modèle objet, présentations basées sur le Web
- Lecteur Windows Media Présentations mobiles, basées sur le Web
- contrôle de ActiveX Lecteur Windows Media, présentations basées sur le Web
- Lecteur Windows Media contrôle Mobile ActiveX, présentations basées sur le Web
- contrôle de ActiveX, présentations basées sur le Web
- Lecteur Windows Media, diffusion multimédia riche
- Lecteur Windows Media modèle objet, diffusion multimédia riche
- modèle objet, diffusion multimédia riche
- Lecteur Windows Media Mobile, diffusion multimédia riche
- contrôle de ActiveX Lecteur Windows Media, diffusion multimédia riche
- Lecteur Windows Media contrôle de ActiveX Mobile, diffusion multimédia riche
- contrôle de ActiveX, diffusion multimédia riche
- Présentations basées sur le Web, diffusion multimédia riche
- création de présentations basées sur le Web, diffusion multimédia riche
- diffusion multimédia enrichie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010887"
---
# <a name="rich-media-streaming"></a>Diffusion multimédia enrichie

Les pages Web complexes contiennent de nombreux composants différents qui sont normalement transférés séparément. Sur une connexion lente, ces pages affichent un seul élément à la fois et peuvent prendre plusieurs minutes pour s’afficher complètement. Cela peut vous empêcher de synchroniser efficacement les pages Web avec vos médias numériques. La solution à ce problème est la diffusion multimédia enrichie, ce qui signifie que vous ajoutez vos pages Web à votre flux de données multimédias numériques afin qu’elles soient fournies en même temps que les données audio ou vidéo.

La diffusion multimédia en continu riche utilise une disposition de jeu de frames simple et se comporte exactement comme un basculement d’URL normal. Tout comme dans le basculement d’URL, les commandes de script d’URL incorporées dans les flux de données multimédias numériques sont utilisées pour afficher le contenu dans le frame cible. au lieu de pointer vers des pages sur le Web, toutefois, les commandes de script d’URL sont utilisées par Lecteur Windows Media série 9 ou version ultérieure pour accéder aux fichiers dans le cache Internet Explorer où le contenu HTML diffusé est placé lors de sa réception. tout comme avec le basculement d’URL normal, vous pouvez écrire des gestionnaires d’événements qui répondent à ces commandes de script d’url, ou vous pouvez laisser le contrôle de Lecteur Windows Media gérer tout automatiquement.

> [!Note]  
> Tout contenu HTML fourni via le streaming multimédia enrichi est lu dans la zone de sécurité Internet et est soumis aux paramètres de sécurité du navigateur de l’utilisateur.

 

pour plus d’informations sur la création de présentations multimédias riches, consultez le kit de développement logiciel (sdk) Windows media Format 9 ou version ultérieure et le kit de développement logiciel (sdk) Windows media encoder 9.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de présentations Web-Based**](creating-web-based-presentations.md)
</dt> <dt>

[**Utilisation d’un script pour contrôler le basculement d’URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 





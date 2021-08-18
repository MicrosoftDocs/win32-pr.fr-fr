---
description: Utiliser la balise meta pour garantir la compatibilité future
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Utiliser la balise meta pour garantir la compatibilité future
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0cff3dab146d67303d57c97b2298614c5ae0142b18a3bd2d141fbf90e86ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994589"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Utiliser la balise meta pour garantir la compatibilité future

Windows Internet Explorer 8 vous permet de contrôler les modes de compatibilité des documents. vous pouvez donc demander au navigateur de restituer les pages Web de la même façon que les versions antérieures du navigateur. Vous pouvez également choisir le moment de la mise à jour de la page Web, tout en continuant à utiliser et à fonctionner correctement.

## <a name="setting-the-meta-element"></a>Définition de l’élément meta

L’élément **meta** comprend un attribut **content** qui vous permet de spécifier le mode dans lequel le contenu est restitué pour la page Web, comme le montre le tableau suivant.



| Valeur | Mode de rendu                                                 |
|-------|----------------------------------------------------------------|
| IE = 9  | utiliser le mode de rendu des normes d’Internet Explorer 9 Windows   |
| IE = 8  | Utiliser le mode de rendu des normes d’Internet Explorer 8           |
| IE = 7  | utiliser le mode de rendu des normes d’Internet Explorer 7 Windows   |
| IE=5  | Utiliser le mode de rendu des normes de Microsoft Internet Explorer 5 |



 

Pour plus d’informations sur la compatibilité et l’en-tête X-UA-compatible, consultez Définition de la [compatibilité des documents](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) dans MSDN Library.

L’exemple de code suivant montre comment forcer l’affichage d’une page Web en mode Internet Explorer 8.


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a>Utilisation d’un en-tête HTTP

De nombreux sites Web contiennent des milliers (ou des dizaines de milliers) de pages Web individuelles, ce qui signifie que la définition de l’élément **meta** sur chaque document est irréalisable. Si vous souhaitez définir l’élément **meta** pour toutes les pages ou une collection de pages sélectionnées par dossier, vous pouvez modifier la configuration de votre serveur à la place et ajouter les métadonnées X-UA-Compatible dans l' [en-tête http](/previous-versions/cc817572(v=msdn.10)).

Pour les sites qui requièrent différentes valeurs d’élément **méta** pour les pages sur le même serveur, il existe plusieurs outils qui génèrent et insèrent automatiquement l’élément **meta** approprié. Par exemple, l’utilitaire [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) de Aggiorno insère et supprime la fonctionnalité de balise de compatibilité d’Internet Explorer 8 et peut aider votre site à respecter des normes de compatibilité spécifiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 

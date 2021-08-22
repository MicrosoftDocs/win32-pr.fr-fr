---
title: ConnectType VML (attribut)
description: ConnectType VML (attribut)
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76910977c0673500be2e91d9f387b1e61782a1460e5de0d513784caa6f0f1633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999259"
---
# <a name="vml-connecttype-attribute"></a>ConnectType VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le type de points de connexion utilisé pour attacher des formes à d’autres formes. En lecture/écriture. **Chaîne**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* o :connecttype = " *expression* " >

**Remarques**

Ces valeurs comprennent :



| Valeur    | Description                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| aucun     | Aucun site de connexion. Par défaut.                                                                                                         |
| rect     | Quatre points de connexion standard aux milieux des côtés supérieur, inférieur, gauche et droit.                                                   |
| segments | Les points d’édition de la forme sont utilisés. Les points de modification sont les points noirs d’un éditeur graphique qui permettent de sélectionner des parties d’une forme. |
| custom   | Tableau personnalisé d’emplacements de connexion.                                                                                               |



 

*Microsoft Office Attribut extensions*

 

 
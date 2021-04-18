---
title: ConnectorType VML (attribut)
description: ConnectorType VML (attribut)
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512314"
---
# <a name="vml-connectortype-attribute"></a>ConnectorType VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Indique le type de connecteur utilisé pour joindre des formes. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :ConnectorType = " *expression* " >

**Remarques**

Ces valeurs comprennent :



| Valeur    | Description                    |
|----------|--------------------------------|
| aucun     | Aucun connecteur.                  |
| angles | Par défaut. Connecteur droit. |
| coud    | Connecteur en forme de coude.     |
| courbe   | Connecteur courbé.            |



 

Cet attribut peut également être utilisé par un moteur de règles d’un éditeur graphique.

*Attribut extensions Microsoft Office*

**Exemple**

La forme utilise une ligne droite comme connecteur.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 
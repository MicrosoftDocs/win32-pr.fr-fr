---
title: Attribut SRC (VMLFrame) (VML)
description: Attribut SRC (VMLFrame) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315492"
---
# <a name="src-attribute-vmlframevml"></a>Attribut SRC (VMLFrame) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la source de données pour le frame. En lecture/écriture. **Chaîne**.

**S’applique à**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Syntaxe de balise**

<v : *Element* SRC = " *expression* " >

**Syntaxe du script**

*Element* . src = "*expression*"

*expression* = *élément*. SRC

**Remarques**

L’attribut **src** peut impliquer les syntaxes suivantes :

-   URL vers un fichier externe. Le fichier doit être un fichier XML au format suivant :
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   Dans le fichier, vous devez avoir une ou plusieurs formes VML avec des ID valides qui peuvent être référencées à l’aide de la syntaxe suivante :
    ```HTML
       filename#shapename
    ```

    

-   Dans la référence suivante, les fichiers externes ont l’extension. Vml, mais vous pouvez utiliser n’importe quelle extension :
    ```HTML
       external.vml#image01
    ```

    

-   Vous pouvez référencer une forme dans le même fichier à l’aide de la syntaxe suivante :
    ```HTML
       #shapename
    ```

    

Si **clip** a la **valeur false**, la forme est mise à l’échelle pour s’ajuster au cadre. Si la **valeur est true**, toutes les parties de la forme qui sont en dehors du frame ne seront pas affichées.

Notez que [origin](origin-attribute--vmlframe--vml.md) et [Size](size-attribute--vmlframe.md) ne sont pas utilisés, sauf si **clip** a la **valeur true**.

**Attribut standard VML**

**Exemple**

L’image définie dans le fichier externe sera découpée.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 
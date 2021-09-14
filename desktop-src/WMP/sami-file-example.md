---
title: Exemple de fichier SAMI
description: Exemple de fichier SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- modèle objet Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Lecteur Windows Media Mobile, accessible en SAMI (Synchronized Accessible Media Interchange)
- contrôle de ActiveX Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- Lecteur Windows Media contrôle Mobile ActiveX, SAMI (synchronized Accessible Media Interchange)
- contrôle de ActiveX, SAMI (synchronized Accessible Media Interchange)
- Fichiers de Media Interchange (SAMI) synchronisés, fichiers
- SAMI (Synchronized Accessible Media Interchange), fichiers
- SAMI (Synchronized Accessible Media Interchange), exemple de code
- SAMI (Synchronized Accessible Media Interchange), exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416174"
---
# <a name="sami-file-example"></a>Exemple de fichier SAMI

L’exemple de code suivant est un fichier SAMI complet avec un ensemble de texte de légende fermé et plusieurs déclarations de classe pour le style de texte et la langue de légende.


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



Les styles définis dans un fichier SAMI sont conformes à la syntaxe du sélecteur CSS standard pour les éléments, les classes et les ID. Dans l’élément BODY, tous les éléments P ont le style défini pour le sélecteur d’élément P dans l’élément STYLE. L’attribut Class d’un élément spécifie le langage de cet élément tel que défini par les sélecteurs de classe dans l’élément STYLE (les sélecteurs qui commencent par des points). Les noms de langage spécifiés par les sélecteurs de classe peuvent être n’importe quelle chaîne. Les éléments avec l’attribut ID spécifié ont un style supplémentaire appliqué comme indiqué par les sélecteurs d’ID dans l’élément STYLE (les sélecteurs préfixés par des \# caractères).

lorsqu’ils sont utilisés conjointement avec le modèle objet Lecteur Windows Media, les sélecteurs de classe correspondent à *ClosedCaption*. Propriété **SAMILang** , qui peut être utilisée pour spécifier la langue des légendes. Les sélecteurs d’ID correspondent au *ClosedCaption*. Propriété **SAMIStyle** , qui peut être utilisée pour spécifier le style dans lequel les sous-titres apparaîtront.

Pour plus d’informations sur la création de fichiers SAMI, voir présentation de SAMI 1,0 sur le [site Web de Microsoft](/documentation/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 
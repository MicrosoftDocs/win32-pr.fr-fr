---
title: Détection du lecteur
description: Détection du lecteur
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Lecteur Windows Media des magasins en ligne, détection des joueurs
- magasins en ligne, détection des joueurs
- tapez 1 magasins en ligne, détection des joueurs
- tapez 2 magasins en ligne, détection des joueurs
- Lecteur Windows Media des magasins en ligne, détection de lecteur
- magasins en ligne, détection de lecteur
- types 1 magasins en ligne, détection de lecteur
- type 2 magasins en ligne, détection de lecteur
- détection de lecteur
- détection des joueurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d511fc8c14a901c6823715293c5eb621b45762cd5e9fae78d8c4df503a03bf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863509"
---
# <a name="detecting-the-player"></a>Détection du lecteur

lorsque vous créez une page web pour votre boutique en ligne, vous pouvez décider que vous souhaitez que les utilisateurs puissent afficher la page dans un navigateur Web ou dans Lecteur Windows Media. Vous pouvez utiliser un script ASP pour déterminer si votre page Web est hébergée dans le lecteur.

l’exemple de code suivant récupère le paramètre de version de la chaîne de requête d’URL pour déterminer si la page est hébergée dans Lecteur Windows Media :


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



notez que le code précédent suppose que le paramètre de version existe dans la chaîne de requête lorsqu’il est hébergé dans Lecteur Windows Media. Cela est vrai pour les pages ouvertes par l’utilisateur, mais peut ne pas être vrai pour les pages ouvertes à l’aide de **External. NavigateTaskPaneURL**. Pour que la chaîne de requête de version existe lors de la navigation par programmation, vous devez ajouter le paramètre version à l’appel de méthode ou ajouter dynamiquement la version à l’URL de base de l’élément **Navigate** de votre document serviceInfo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du document ServiceInfo de manière dynamique**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





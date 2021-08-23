---
title: Utilisation de la substitution d’URL et de serveur
description: Utilisation de la substitution d’URL et de serveur
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows Sélections de métafichiers multimédias, substitutions d’URL
- sélections, substitutions d’URL
- sélections de métafichiers, substitutions d’URL
- Windows Sélections de métafichiers multimédia, substitutions de serveur
- sélections, substitutions de serveur
- sélections de métafichiers, substitutions de serveur
- Windows Sélections de métafichiers multimédias, substitutions de protocole
- sélections, substitutions de protocole
- sélections de métafichiers, substitutions de protocole
- Lecteur Windows Media, substitutions d’URL
- Lecteur Windows Media, substitutions de serveur
- Lecteur Windows Media, substitutions de protocole
- Substitutions d’URL
- substitutions de serveur
- substitutions de protocole
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3988ff019fba838e86ea1d0e7b0f6124c367bb8b505a0f2d2e2f639b94d93e52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465672"
---
# <a name="using-url-and-server-rollover"></a>Utilisation de la substitution d’URL et de serveur

Vous pouvez utiliser des sélections de métafichiers pour fournir un moyen de basculer automatiquement vers d’autres sources de contenu lorsqu’un flux n’est pas accessible ou lu. Vous pouvez utiliser cette méthode de substitution pour spécifier les sources du même contenu sur différents serveurs ou sur différents types de serveurs. vous pouvez, par exemple, spécifier une première alternative sur un serveur de média Windows différent. En cas d’échec de lecture de ce contenu, le client peut basculer vers une deuxième alternative sur un serveur Web. Lecteur Windows Media essaie automatiquement de basculer vers différents protocoles selon ses paramètres de propriété de média Windows avant d’essayer les url de substitution dans la sélection.

Définissez la substitution de serveur et de protocole en plaçant successivement plusieurs éléments **ref** dans un élément d' **entrée** . Chaque élément **ref** spécifie un autre emplacement ou protocole pour un fichier multimédia ou un flux.

Exemple de code


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> </dl>

 

 





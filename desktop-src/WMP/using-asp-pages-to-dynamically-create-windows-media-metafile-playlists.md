---
title: utilisation de Pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media
description: utilisation de Pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Windows Sélections de métafichiers multimédia, création
- sélections de métafichiers, création
- sélections, création
- Windows Playlists de métafichier multimédia, création dynamique
- sélections de métafichiers, création dynamique
- sélections, création dynamique
- Windows Sélections de métafichiers multimédias, pages ASP
- sélections de métafichiers, pages ASP
- sélections, pages ASP
- création d’Windows sélections de métafichiers multimédia
- création dynamique d’Windows sélections de métafichiers multimédia
- pages ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519052"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>utilisation de Pages ASP pour créer dynamiquement des sélections de métafichiers Windows Media

Vous pouvez utiliser les pages de Active Server (fichiers ASP ou. asp) pour générer dynamiquement des sélections en fonction des informations fournies par les utilisateurs. une page ASP est une page web dynamique utilisée conjointement avec Microsoft Internet Information Services (IIS). ASP est un environnement dans lequel vous pouvez combiner du code HTML, des scripts et des composants serveur ActiveX réutilisables pour créer des solutions d’entreprise Web dynamiques et puissantes. les pages ASP activent les scripts côté serveur pour IIS avec la prise en charge native de microsoft Visual Basic scripting Edition (VBScript) et de microsoft JScript. Cette discussion part du principe que vous êtes familiarisé avec ASP et en définissant des variables.

toutes les informations d’en-tête doivent être contenues sur la première ligne de la chaîne de page ASP retournée à Lecteur Windows Media.

lorsque vous utilisez des pages asp pour générer des sélections, vous devez spécifier des valeurs pour les propriétés **ContentType** et **expires** de l’objet de **réponse** dans la page ASP en raison de problèmes de latence avec Lecteur Windows Media. la valeur **Response. ContentType** doit être une extension de nom de fichier valide pour Windows les fichiers multimédias. Les valeurs acceptables sont WMA, Wax, WMV, wvx, ASF et asx.

la propriété **Response. expires** spécifie la durée, en secondes, pendant laquelle Lecteur Windows Media met en cache le fichier de sélection. si vous spécifiez la valeur zéro, Lecteur Windows Media demande une nouvelle sélection à partir du serveur chaque fois que l’utilisateur actualise la page.

Pour plus d’informations sur l’utilisation de l’objet de **réponse** dans Active Server pages, consultez le kit de développement Platform SDK.

le code suivant est un exemple de page ASP utilisée pour générer une sélection de métafichier multimédia Windows.


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> </dl>

 

 





---
title: Utilisation de liens relatifs dans les sous-fichiers
description: Utilisation de liens relatifs dans les sous-fichiers
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Sélections de métafichiers Windows Media, liens relatifs
- sélections, liens relatifs
- sélections de métafichiers, liens relatifs
- sous-fichiers, liens relatifs
- Fichiers Windows Media, liens relatifs
- liens relatifs
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839726"
---
# <a name="using-relative-links-in-metafiles"></a>Utilisation de liens relatifs dans les sous-fichiers

Les liens relatifs sont une fonctionnalité entièrement prise en charge des fichiers Windows Media. Vous pouvez utiliser des liens relatifs dans les sous-fichiers de la même façon que vous les utilisez dans des documents HTML. L’utilisation de liens relatifs vous permet de créer des métafichiers portables, ce qui signifie que vous pouvez copier ou déplacer l’intégralité d’une structure de répertoires vers un autre serveur sans mettre à jour les chemins d’accès aux fichiers graphiques utilisés comme bannières ou les attributs **href** des éléments **moreinfo** (s’ils font référence à des fichiers sur le même serveur Web que le métafichier stocké). Les liens relatifs fonctionnent, dans toutes les applications qui les prennent en charge, car les parties de l’URL non incluses dans l’attribut **href** d’un élément sont incluses dans l’URL envoyée par l’application au serveur lorsque cette URL est demandée. Cela signifie que le protocole (par exemple, https://), le nom du serveur et le répertoire virtuel dans lequel se trouve le fichier contenant le lien relatif sont tous inclus dans l’URL qui est envoyée au serveur. Si le fichier multimédia, ou l’URL que vous liez à l’aide d’un lien relatif ne réside pas sur le même serveur que le métafichier, le lien relatif n’est pas valide.

> [!Note]  
> Ces informations sur les liens relatifs sont correctes uniquement lors de l’utilisation d’un lien vers les fichiers de données ouverts dans le lecteur Windows Media autonome. Quand vous utilisez le contrôle du lecteur Windows Media incorporé, tous les liens sont relatifs à la page sur laquelle le contrôle est hébergé, sauf si l’élément enfant de **base** de l’élément **ASX** est utilisé pour rediriger le chemin d’accès relatif.

 

Tous les liens relatifs dans le métafichier doivent être entièrement relatifs, et non relatifs au lecteur, pour la diffusion multimédia en continu. Quand une URL commence par un \\ caractère «», le lien est relatif au lecteur. Le lecteur Windows Media tente d’ouvrir le fichier auquel il est lié sur le lecteur à partir duquel le métafichier a été ouvert, généralement un serveur Web. Étant donné que les serveurs Web utilisent des répertoires virtuels, le lecteur Windows Media tente de trouver le fichier multimédia ou le flux spécifié dans un sous-répertoire d’un répertoire virtuel sur le serveur Web à partir duquel le métafichier a été ouvert. Un utilisateur n’a pas accès à un répertoire de serveur. L’exemple de cette section illustre l’utilisation d’un lien complet.

Vous pouvez utiliser des liens relatifs au lecteur lors de l’utilisation de métafichiers sur un seul ordinateur sur lequel tous les fichiers multimédias liés dans la sélection de métafichiers existent sur un dispositif de stockage sur cet ordinateur. Toutefois, vous ne pouvez pas diffuser le contenu multimédia de cette manière.

Lorsque vous utilisez un lien vers un autre métafichier pour autoriser les liens relatifs, le nom affiché comme titre par le lecteur Windows Media est le titre dans le métafichier d’origine.

Les liens relatifs ne peuvent pas être utilisés pour les URL vers un serveur multimédia de diffusion en continu, car différents protocoles sont utilisés pour accéder au contenu multimédia en continu.

Dans l’exemple de sélection suivant, le premier **ENTRYREF** contient une URL pour une autre playlist, relative. Wax.


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



L’exemple suivant est le fichier relative. Wax, qui contient des liens relatifs.


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



L’URL qui contient la référence à la playlist, relative. Wax, peut exister dans une sélection de métafichiers partout où elle est accessible à l’utilisateur. Pour que l’URL soit traitée avec succès, il doit y avoir un serveur Web nommé « example.microsoft.com ». Ce serveur Web doit avoir un répertoire virtuel défini en tant que « sous-fichiers ». La sélection référencée, relative. Wax, doit exister sur le serveur Web nommé « example.microsoft.com » dans le répertoire virtuel « cafiles ».

Pour que les fichiers multimédias référencés dans la playlist relative. Wax soient correctement accessibles et joués, il doit y avoir un répertoire nommé « Graphics », qui est un sous-répertoire du répertoire virtuel du serveur « metadirectorys ». Le fichier graphique Logo1.jpg, référencé dans l’élément **Banner** , doit être le sous-répertoire nommé Graphics.

De même, un document nommé Category1.htm doit résider dans un sous-répertoire nommé Category1. Le répertoire nommé Category1 doit exister sous la forme d’un sous-répertoire du répertoire virtuel « méta-fichiers » sur le serveur Web example.microsoft.com.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création de sélections de métafichiers**](creating-metafile-playlists.md)
</dt> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





---
title: Exemples d’applications du SDK Windows Media format
description: Exemples d’applications du SDK Windows Media format
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media Format SDK, exemples d’applications
- gestion des droits numériques (DRM), exemples d’applications
- DRM (gestion des droits numériques), exemples d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464075"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Exemples d’applications du SDK Windows Media format

L’exemple de code fourni avec ce kit de développement logiciel (SDK) se présente sous la forme de projets pour Microsoft Visual Studio 2005. La plupart des exemples sont en C++, mais ManagedWMFSDKWrapper et ManagedMetadataEdit requièrent C#.

Ces exemples ne fonctionneront pas si le kit de développement logiciel (SDK) Windows Media format ou le SDK Windows Player n’a pas été installé.

Les informations d’utilisation de chaque exemple sont contenues dans un fichier de readme.txt dans chaque répertoire d’exemple.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>SAML</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AudioPlayer</td>
<td>Lit les fichiers Windows Media, y compris les fichiers protégés par DRM. Elle est contrôlée par le biais d’une interface graphique utilisateur, et les commandes incluent Play, pause, Seek et Stop. Il peut lire des fichiers locaux ou des fichiers lus à partir d’Internet (y compris ceux de la sortie sur Internet à l’aide de l’exemple WMVNetWrite).
<blockquote>
[!Note]<br />
Les parties DRM de cet exemple ne sont pas prises en charge sur les versions x64 de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>DRMHeader</td>
<td>DRMHeader est une application console qui utilise l’interface <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> de l’éditeur de métadonnées pour lire les attributs DRM des fichiers sans les lier à la bibliothèque statique DRM.
<blockquote>
[!Note]<br />
Cet exemple n’est pas pris en charge sur les versions x64 de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>DRMShow</td>
<td>DRMShow est une application console qui montre comment lire les propriétés <a href="wmformat-glossary.md"><em>DRM</em></a> d’un fichier Windows Media à l’aide de la méthode <strong>IWMDRMReader :: GetDRMProperty</strong> . Cet exemple illustre l’utilisation de la méthode <strong>IWMDRMReader :: GetDRMProperty</strong> et des propriétés qui peuvent être récupérées à partir du lecteur DRM. Il ne montre pas comment acquérir une licence pour du contenu protégé par DRM. Cet exemple requiert la génération de la bibliothèque de stubs DRM WMStubDRM. lib.<br/>
<blockquote>
[!Note]<br />
Cet exemple n’est pas pris en charge sur les versions x64 de Windows.
</blockquote>
<br/> Lorsque vous acquérez WMStubDRM. lib auprès de Microsoft, la bibliothèque se voit attribuer un niveau de sécurité d’application. Si le niveau de sécurité de la bibliothèque que vous recevez n’est pas suffisant pour lire un fichier protégé, cet exemple affiche une erreur.<br/></td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSCopy</td>
<td>Transcode un ou plusieurs fichiers en fichier ASF à l’aide du filtre de l’enregistreur ASF DirectShow DirectShow. Le fichier d’entrée peut être n’importe quel format compressé ou non compressé pris en charge par DirectShow.</td>
</tr>
<tr class="odd">
<td>DirectShowInterop/DSPlay</td>
<td>Cet exemple est un lecteur de fichiers multimédias audio/vidéo interactif avec prise en charge de <a href="wmformat-glossary.md"><em>DRM</em></a> . Il utilise le filtre de lecteur ASF WM de DirectShow pour lire les fichiers Windows Media (ASF, WMA, WMV) sans protection DRM et les fichiers qui utilisent DRM à un niveau de 100 ou plus. Pour plus d’informations, consultez readme.txt dans le répertoire de l’exemple.</td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSSeekFm</td>
<td>Cet exemple montre comment utiliser le filtre de lecteur ASF DirectShow DirectShow pour lire du contenu ASF dans un graphique de filtre DirectShow et comment utiliser la prise en charge de la recherche de frame dans le kit de développement logiciel (SDK) de format Windows Media.</td>
</tr>
<tr class="odd">
<td>Géré/WMFSDKWrapper</td>
<td>Cet assembly géré sert de wrapper utilisé par les exemples de code managé pour accéder à certaines interfaces de métadonnées de ce kit de développement logiciel (SDK).</td>
</tr>
<tr class="even">
<td>Géré/MetadataEdit</td>
<td>Cette application C# peut être utilisée pour afficher et modifier des métadonnées à partir de fichiers Windows Media.</td>
</tr>
<tr class="odd">
<td>MetaDataEdit</td>
<td>Il s’agit d’une version C++ de l’application MetadataEdit managée.</td>
</tr>
<tr class="even">
<td>ReadFromStream</td>
<td>Cet exemple d’application console montre comment lire des données à partir de <strong>IStream</strong> avec WMReader. La source <strong>IStream</strong> a été implémentée pour utiliser un fichier au format Windows Media (WMA/WMV/ASF).
<blockquote>
[!Note]<br />
Cet exemple n’indique pas comment traiter les exemples de supports provenant de WMReader. Pour obtenir des exemples de traitement audio/vidéo ou d’autres types d’exemples de médias, reportez-vous à d’autres exemples, par exemple AudioPlayer, qui sont inclus dans le kit de développement logiciel (SDK) du format Windows Media.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UncompAVIToWMV</td>
<td>Cet exemple d’application console montre le code nécessaire pour compresser un fichier AVI dans un fichier WMV. Il montre comment fusionner des exemples pour des flux audio et vidéo à partir de plusieurs fichiers AVI et les fusionner dans des flux similaires ou créer un flux basé sur le profil de flux source. Il montre également comment créer un flux arbitraire, effectuer un encodage multipasse, ajouter du code temporel SMPTE et appliquer la protection DRM version 1.</td>
</tr>
<tr class="even">
<td>WMGenProfile/exe</td>
<td>Cet exemple a été mis à jour à partir de la version 7,1. Il s’agit désormais d’une application de boîte de dialogue MFC. L’exemple WMGenProfile illustre l’utilisation de la bibliothèque statique WMGenProfile. Il sert également d’outil pour la création de profils. Cet outil est destiné aux développeurs familiarisés avec le format Windows Media. L’interface utilisateur n’a pas été testée pour l’expérience utilisateur et n’est pas censée être une recommandation sur la façon de présenter ces informations à un utilisateur.</td>
</tr>
<tr class="odd">
<td>WMGenProfile/lib</td>
<td>L’exemple de bibliothèque GenProfile illustre la création de profils. Il montre comment créer des flux et des types de médias pour différents types de flux (audio, vidéo, script, image, transfert de fichiers et Web). Il ne montre pas comment utiliser des profils système ou comment convertir des profils système en profils qui spécifient les codecs de série Windows Media Audio et Video 9.</td>
</tr>
<tr class="even">
<td>WMProp</td>
<td>Cette application console montre comment récupérer des attributs à l’aide de l’objet de l’éditeur de métadonnées et des informations de profil du lecteur.</td>
</tr>
<tr class="odd">
<td>WMStats</td>
<td>Cette application console affiche les statistiques sur les lecteurs et les rédacteurs. Plusieurs instances de WMStats peuvent également être utilisées simultanément sur un ordinateur. Démarrez une instance en tant que serveur pour envoyer le flux au réseau, puis exécutez une deuxième instance en tant que client pour vérifier que le serveur est correctement diffusé.</td>
</tr>
<tr class="even">
<td>WMSyncReader</td>
<td>Cet exemple d’application console montre comment lire un fichier multimédia à l’aide de <strong>IWMSyncReader</strong> sans créer de thread supplémentaire ou à l’aide de rappels. Les fonctionnalités suivantes sont implémentées : lecture des exemples compressés ou décompressés<br/> Recherche basée sur le temps<br/> Recherche basée sur des frames<br/> Source dérivée <strong>IStream</strong><br/></td>
</tr>
<tr class="odd">
<td>WMVAppend</td>
<td>Cette application console prend deux fichiers Windows Media pour l’entrée et tente de créer un fichier de sortie avec le contenu du premier suivi du deuxième. L’exemple compare les profils des deux fichiers d’entrée pour s’assurer qu’ils sont suffisamment similaires pour être ajoutés. Si ce n’est pas le cas, un message d’erreur s’affiche. Par exemple, un message d’erreur se produit lorsqu’un fichier est audio uniquement et le second est un fichier vidéo audio ou lorsque deux fichiers audio ont des vitesses de transmission différentes. L’exemple accepte des sources à vitesse de transmission variable (VBR). Toutefois, lors de la comparaison des profils des deux sources VBR, l’exemple ignore la différence de vitesse de transmission moyenne, car deux flux VBR auront des taux de bits moyens différents, même s’ils ont été créés à l’aide du même profil. WMVAppend ne peut pas comparer le taux binaire de pointe des flux VBR basés sur un taux binaire non restreint, ou le niveau de qualité des flux VBR basés sur la qualité, car ces informations n’existent pas dans les fichiers sources. C’est la responsabilité de l’utilisateur de s’assurer que deux fichiers sources sont créés à l’aide du même profil. Dans le cas contraire, vous pouvez créer un contenu non valide.<br/></td>
</tr>
<tr class="even">
<td>WMVCopy</td>
<td>Cet exemple montre le code nécessaire pour copier un fichier WMV. Il montre comment lire et écrire des exemples compressés, lire des attributs d’en-tête et des scripts, et modifier les attributs d’en-tête.</td>
</tr>
<tr class="odd">
<td>WMVNetWrite</td>
<td>Cette application console montre comment un fichier Windows Media est diffusé en continu sur Internet. L’exemple requiert la spécification d’un port, puis le fichier peut être lu à l’aide d’un lecteur.</td>
</tr>
<tr class="even">
<td>WMVRecompress</td>
<td>Cette application console montre comment recompresser un fichier WMV. Il illustre la lecture des exemples non compressés, l’écriture d’exemples non compressés et l’encodage à plusieurs passes, la sortie multicanaux et la recompression intelligente.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du kit de développement logiciel (SDK) Windows Media format**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 






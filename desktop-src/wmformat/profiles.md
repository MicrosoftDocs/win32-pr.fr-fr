---
title: Profils
description: Profils
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Media Format SDK, profils
- ASF (Advanced Systems Format), profils
- ASF (format des systèmes avancés), profils
- Windows Media Format SDK, fichiers. prx
- Fichiers ASF (Advanced Systems Format), fichiers. prx
- ASF (format des systèmes avancés), fichiers. prx
- Windows Media Format SDK, éditeur de profil
- ASF (Advanced Systems Format), éditeur de profil
- ASF (format des systèmes avancés), éditeur de profil
- fichiers. prx
- fichiers PRX
- Éditeur de profil
- Windows Encodeur multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de244445a7c1301c7a14ef273b81ac9fd9cbfb62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295854"
---
# <a name="profiles"></a>Profils

Un profil est une collection de données qui décrit la configuration d’un fichier ASF. Au minimum, un profil doit contenir des paramètres de configuration pour un seul flux.

Les informations de flux dans un profil contiennent la vitesse de transmission, la fenêtre de mémoire tampon et les propriétés de média du flux. Les informations de flux pour l’audio et la vidéo décrivent exactement comment le média est configuré dans le fichier, y compris le codec (le cas échéant) utilisé pour compresser les données.

Un profil contient également des informations sur les différentes fonctionnalités de fichier ASF qui seront utilisées dans les fichiers créés avec. Cela inclut l' [exclusion mutuelle](mutual-exclusion.md), la [hiérarchisation des flux](stream-prioritization.md), le [partage de bande passante](bandwidth-sharing.md)et les extensions d’unité de [données](data-unit-extensions.md).

les versions précédentes du kit de développement logiciel (SDK) de Format multimédia Windows offraient des profils système préconfigurés, qui pouvaient être utilisés pour créer des types de fichiers courants ou modifiés légèrement pour répondre aux besoins de votre application. les profils système ne sont pas pris en charge pour les codecs de la série Media 9 Windows. Cela est dû au fait que le nombre de types de fichiers « communs » a augmenté de façon exponentielle avec l’ajout de nouvelles fonctionnalités. Il est prévu que presque tous les créateurs de contenu aient besoin d’aller au-delà des solutions simples fournies par les profils système. Vous pouvez toujours utiliser les anciens profils système comme point de départ. Pour plus d’informations, consultez [utilisation des profils système](using-system-profiles.md).

Vous devez fournir l’enregistreur avec un profil pour chaque fichier que vous écrivez. Vous pouvez spécifier un profil à utiliser avec le writer en appelant [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).

les données de profil existent dans différentes formes qui peuvent être utilisées par le kit de développement logiciel (SDK) de Format multimédia Windows. Vous pouvez également accéder aux informations de profil de plusieurs façons. Cela peut entraîner une confusion en ce qui concerne un profil et comment il est utilisé.

Le diagramme suivant montre comment les données de profil sont utilisées dans le kit de développement logiciel (SDK).

![Diagramme montrant le déroulement des informations de profil.](images/formatsdk01.png)

Les données de profil prennent trois formes différentes : les données contenues dans un objet de profil dans une application, un fichier XML sur le disque et les données dans l’en-tête d’un fichier ASF. Chacune de ces formes de données est affichée sous la forme d’un rectangle ombré dans le diagramme.

## <a name="data-in-a-profile-object"></a>Données dans un objet de profil

Lorsque vous modifiez un profil, vous utilisez un objet de profil qui encapsule toutes les données de profil. Vous pouvez créer un objet de profil vide à l’aide de l’objet gestionnaire de profils. Vous pouvez également utiliser l’objet gestionnaire de profils pour charger des données de profil existantes dans un objet de profil.

La plupart des données de profil doivent être ajoutées et manipulées par le biais de l’utilisation d’objets représentant des parties individuelles du profil. Il s’agit notamment d’objets de configuration de flux, d’objets d’exclusion mutuelle, d’objets de partage de bande passante et d’objet de priorité de flux. Chacun de ces types d’objets peut être créé à l’aide de méthodes dans l’objet de profil. L’apport de modifications à ces objets n’affecte pas l’objet de profil tant que vous n’utilisez pas une méthode dans l’objet de profil pour inclure les données mises à jour de l’autre objet.

## <a name="data-in-an-xml-file"></a>Données dans un fichier XML

Les données de profil sont stockées sur disque sous la forme d’un fichier XML avec l’extension de nom de fichier. prx. le kit de développement logiciel (SDK) Windows Media Format est un ensemble de profils appelés profils système qui couvrent les types les plus courants de fichiers ASF. Les profils système sont stockés dans un fichier nommé WMSysPr9. prx. (notez que ce fichier ne contient en fait pas de profils système pour Windows série Media 9, car le concept de profils système n’est plus utilisé.) Lorsque vous enregistrez vos profils personnalisés, vous devez les enregistrer dans vos propres fichiers.

Vous pouvez utiliser l’objet gestionnaire de profils pour enregistrer les données d’un objet de profil dans une chaîne de texte XML. Vous pouvez ensuite utiliser les fonctions d’e/s de fichier de votre choix pour enregistrer la chaîne dans un fichier sur le disque.

## <a name="data-in-the-header-of-an-asf-file"></a>Données dans l’en-tête d’un fichier ASF

Le writer prend les informations du profil et les utilise pour créer les flux qui entrent dans la section de données du fichier ASF. La majeure partie des données de profil est stockée dans la section d’en-tête du fichier lors de l’écriture d’un fichier. Lors de la lecture, l’objet lecteur (ou l’objet lecteur synchrone) peut accéder aux informations contenues dans l’en-tête du fichier. Dans ce cas, l’objet de lecture crée un objet de profil et le remplit avec les données de l’en-tête.

Lorsque vous accédez aux données de profil à l’aide du lecteur (ou d’un lecteur synchrone), vous pouvez apporter des modifications aux informations de profil, mais il n’existe aucun moyen d’appliquer ces modifications au fichier dans le lecteur. Vous pouvez appliquer les informations de profil d’un fichier d’un lecteur à un profil dans un enregistreur pour créer un nouveau fichier avec les mêmes paramètres que le fichier du lecteur. Dans ce cas, toutes les modifications apportées aux informations de profil avant de définir le profil dans le writer seront reflétées dans les informations de profil enregistrées par le writer.

## <a name="using-profile-editor"></a>Utilisation de l’éditeur de profil

plutôt que de créer des profils à l’aide du kit de développement logiciel (SDK) de Format de média Windows, vous pouvez utiliser l’éditeur de profil, un utilitaire inclus avec Windows media encoder. Dans votre application d’encodage, utilisez la méthode **IWMProfileManager :: LoadProfileByData** pour charger le profil enregistré. Dans certains scénarios, par exemple, si vous utilisez un nombre limité de profils qui ne sont jamais modifiés de manière dynamique, il peut être plus pratique d’utiliser l’éditeur de profil pour créer vos profils.

Toutefois, si vous utilisez l’éditeur de profil, il est recommandé de ne pas utiliser le paramètre « Taille vidéo : identique à l’entrée vidéo ». Lorsque cette case à cocher est activée, l’éditeur de profil crée un profil dont la hauteur et la largeur de sortie vidéo sont égales à zéro. lorsque Windows encodeur multimédia rencontre ces profils, il définit les valeurs correctes pour qu’elles correspondent à l’entrée vidéo. toutefois, l’enregistreur dans le kit de développement logiciel (SDK) du Format de média Windows ne le fait pas automatiquement. vous devez donc vous assurer que votre application définit la taille de l’image vidéo dans les cas où le profil n’en a aucun.

**Remarque** Certains éléments de configuration de flux ne sont pas stockés dans le profil. Les données du profil décrivent le format du fichier ASF terminé. Les propriétés de média d’entrée et d’autres données de configuration utilisées par l’objet enregistreur pour configurer les codecs ne sont pas enregistrées dans le profil. Cela comprend toutes les propriétés définies à l’aide de la méthode [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objet de partage de bande passante**](bandwidth-sharing-object.md)
</dt> <dt>

[**Concepts**](concepts.md)
</dt> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Objet d’exclusion mutuelle**](mutual-exclusion-object.md)
</dt> <dt>

[**Gestionnaire de profils, objet**](profile-manager-object.md)
</dt> <dt>

[**Configuration de flux, objet**](stream-configuration-object.md)
</dt> <dt>

[**Objet de priorité de flux**](stream-prioritization-object.md)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> </dl>

 

 





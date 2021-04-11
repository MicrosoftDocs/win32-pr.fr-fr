---
description: Attributs Media Foundation pour les objets d’en-tête ASF
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Attributs Media Foundation pour les objets d’en-tête ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db74ccb03536c7766dd7e1564119edbd41d5dbe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321617"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Attributs Media Foundation pour les objets d’en-tête ASF

L’objet d’en-tête ASF de niveau supérieur d’un fichier contient plusieurs objets de sous-en-tête ASF. L’objet ContentInfo stocke les informations de tous ces objets d’en-tête et expose certaines valeurs à une application par le biais d’attributs.

## <a name="file-properties-object"></a>Objet de propriétés de fichier

Cet objet d’en-tête est présent dans tous les fichiers ASF. Ces champs décrivent les attributs de niveau fichier de l’ensemble de la présentation. Le tableau suivant répertorie les champs de l’objet de propriétés de fichier et les attributs de descripteur de présentation correspondants.



| Champ de l’objet de propriétés de fichier | Attribut de descripteur de présentation                                                                            | Description                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| ID de fichier                      | [**ID du fichier. MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Identificateur unique de ce fichier.                                                               |
| Taille du fichier                    | [**\_ \_ taille totale des \_ fichiers MF PD \_**](mf-pd-total-file-size-attribute.md)                                         | Taille du fichier en octets.                                                                    |
| Date de création                | [**heure de création de MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | Date et heure de création du fichier.                                                               |
| Nombre de paquets de données           | [**\_paquets MF PD \_ ASF FM \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Nombre de paquets de données dans l’objet de données ASF.                                                 |
| Durée de lecture                | [**\_durée de \_ \_ \_ lecture \_ MF PD ASF**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Temps nécessaire pour lire le fichier, en unités de 100 nanosecondes. Cette valeur comprend le temps de préroll. |
| Durée d’envoi                | [**durée d’envoi de la norme MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Temps nécessaire pour envoyer le fichier, en unités de 100 nanosecondes.                                       |
| Preroll                      | [**préroll MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Durée de la mise en mémoire tampon des données avant la diffusion du fichier, en unités de 100 nanosecondes.            |
| Indicateurs                        | [**\_indicateurs FM PD \_ ASF \_ FichierPropriétés \_**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Indicateurs indiquant si le fichier est de diffusion ou de recherche.                                    |
| Taille minimale des paquets de données     | [**\_taille de \_ paquet min PD ASF \_ FichierPropriétés \_ Min \_ \_ .**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Taille minimale des paquets de données dans le fichier, en octets.                                        |
| Taille maximale des paquets de données     | [**\_ \_ \_ \_ taille maximale des \_ paquets \_ MF PD ASF FichierPropriétés**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Taille maximale des paquets de données dans le fichier, en octets.                                        |
| Débit maximal              | [**\_vitesse de \_ \_ \_ \_ transmission maximale MF PD ASF FichierPropriétés**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Vitesse de transmission instantanée maximale, en bits par seconde.                                            |



 

## <a name="stream-properties-object"></a>Objet de propriétés de flux

Cet objet d’en-tête décrit les propriétés des flux dans le fichier ASF. Dans Media Foundation, il est géré par l’objet de profil et l’objet de configuration de flux. Pour plus d’informations, consultez [création et configuration de flux ASF](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Objet de liste de codecs

Si cet objet d’en-tête est présent, l’attribut [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md) fournit la liste des codecs utilisés pour encoder les flux dans le fichier ASF. Chaque flux doit avoir ses informations de codec dans cet objet.

## <a name="script-command-object"></a>Script, objet de commande

Si cet objet d’en-tête est présent, il spécifie une liste de commandes de script qui sont prises en charge dans le fichier ASF. Une commande de script se compose d’un type de commande, d’un nom de commande et d’une heure de présentation. Le type de commande et le nom de commande sont des chaînes à caractères larges. Ces commandes peuvent être utilisées pour informer le client d’effectuer une action à un certain point de la présentation. Par exemple, une application peut utiliser le type de commande « nom_fichier » pour lire une séquence continue de fichiers ASF.

Pour afficher la liste des commandes de script, récupérez l’attribut de [**\_ \_ \_ script MF PD ASF**](mf-pd-asf-script-attribute.md) à partir du descripteur de présentation. Une application doit récupérer toutes les commandes de script avant de commencer la lecture.

## <a name="marker-object"></a>Marker, objet

Un marqueur est un signet dans un fichier ASF. Une application peut utiliser des marqueurs pour rechercher divers points dans le contenu. Chaque marqueur se compose d’un nom de marqueur, de l’heure de présentation associée et du décalage par rapport au début du fichier. L’attribut de [**\_ \_ marqueur ASF de la \_ balise ASF**](mf-pd-asf-marker-attribute.md) fournit une liste des marqueurs disponibles pour le fichier.

## <a name="stream-bitrate-properties-object"></a>Objet de propriétés de débit binaire

Cet en-tête stocke la vitesse de transmission moyenne de chaque flux présent dans le fichier ASF. Cette valeur est stockée sur le descripteur de flux du flux dans l’attribut de [**\_ vitesse de \_ \_ \_ transmission ASF SD STREAMBITRATES**](mf-sd-asf-streambitrates-bitrate-attribute.md) .

## <a name="content-encryption-object"></a>Objet de chiffrement de contenu

Cet objet d’en-tête est présent si le fournisseur de contenu a protégé le contenu à l’aide de Microsoft Digital Rights Management. Le tableau suivant répertorie les champs de l’objet de chiffrement de contenu et les attributs de descripteur de présentation correspondants :



| Champ de l’objet de chiffrement du contenu | Attribut de descripteur de présentation                                                                         | Description                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Données secrètes                     | [**\_données de \_ \_ secret CONTENTENCRYPTION \_ \_ pour MF PD ASF**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Tableau d’octets contenant les données secrètes.                                                                 |
| Type de protection                 | [**\_type de CONTENTENCRYPTION MF PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-type-attribute.md)                | Chaîne terminée par le caractère null qui a la valeur « DRM ».                                                       |
| ID de clé                          | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Chaîne terminée par le caractère null qui décrit l’identificateur de clé.                                          |
| URL de la licence                     | [**\_URL de \_ la \_ \_ licence CONTENTENCRYPTION \_**](mf-pd-asf-contentencryption-license-url-attribute.md) | Chaîne terminée par le caractère null qui contient l’URL à partir de laquelle acquérir la licence pour utiliser le contenu. |



 

## <a name="extended-content-encryption-object"></a>Objet de chiffrement de contenu étendu

Cet objet d’en-tête est présent si le fournisseur de contenu a protégé le contenu à l’aide du kit de développement logiciel (SDK) Windows Media Rights Manager 7. L’attribut d' [**\_ \_ \_ \_ \_ URL de licence CONTENTENCRYPTION pour MF PD ASF**](mf-pd-asf-contentencryption-license-url-attribute.md) fournit un tableau d’octets qui correspond au champ de données de l’objet d’en-tête. Ce champ est obligatoire pour utiliser le contenu.

## <a name="extended-stream-properties-object"></a>Objet de propriétés de flux étendu

Cet en-tête fait partie de l’objet d’extension d’en-tête. L’objet de propriétés de flux étendu fournit les propriétés du flux qui ne sont pas définies dans l’objet de propriétés de flux. Ces propriétés sont principalement utilisées pour déterminer les paramètres de « compartiment perdu », qui sont utilisés par le décodeur. Ces propriétés sont également utilisées par l’encodeur lors de la compression des données. Cela est géré par l’objet de profil et l’objet de configuration de flux. Pour plus d’informations, consultez [création et configuration de flux ASF](creating-and-configuring-asf-streams.md).

Le tableau suivant répertorie les champs d’objets de propriétés de flux étendus et les attributs de descripteur de flux correspondants.



| Champ de propriétés de flux étendu | Attribut de descripteur de flux                                                                                | Description                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Débit de données                     | [**\_vitesse de \_ \_ \_ transmission moyenne des \_ données EXTSTRMPROP \_ MF SD ASF**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Débit moyen des données, en bits par seconde.                                                                                   |
| Taille de la mémoire tampon                      | [**\_bufferSize SD \_ ASF \_ EXTSTRMPROP \_ Moy \_ .**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Taille de compartiment perdue. La valeur est le nombre de millisecondes de données pouvant être contenues dans la mémoire tampon à la vitesse moyenne des données.      |
| Autre vitesse de transmission des données           | [**\_vitesse de \_ \_ transmission de \_ \_ données Max \_ . ASF EXTSTRMPROP ASF**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Débit de pointe de données, en e/s. Le taux de données maximal est utilisé pour les flux avec une vitesse de transmission variable.                    |
| Taille de la mémoire tampon de remplacement            | [**\_bufferSize SD \_ \_ EXTSTRMPROP ASF \_ Max \_ .**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Taille maximale de compartiment avec fuites. La valeur est le nombre de millisecondes de données pouvant être contenues dans la mémoire tampon au taux de données maximal. |
| ID de langue du flux               | [**\_ID de \_ \_ langue EXTSTRMPROP \_ \_ MF \_ SD ASF**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | Langue utilisée par le flux, spécifiée sous la forme d’un index dans la liste de langues de l’objet de liste de langage.         |



 

## <a name="language-list-object"></a>Objet de liste de langues

Cet objet d’en-tête fait partie de l’objet d’extension d’en-tête. S’il est présent, l’attribut [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) fournit une liste des identificateurs de langue pris en charge dans le fichier. Les identificateurs sont conformes à la norme RFC 1766 pour la spécification des langues.

## <a name="mutual-exclusion-object"></a>Objet d’exclusion mutuelle

Cet en-tête spécifie des groupes de flux et leurs propriétés, dont une seule sera remise à la fois. Pour plus d’informations, consultez [utilisation de l’exclusion mutuelle pour les flux ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objet ASF ContentInfo](asf-contentinfo-object.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




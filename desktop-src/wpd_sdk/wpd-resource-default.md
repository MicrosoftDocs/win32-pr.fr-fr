---
description: Spécifie l’ensemble du fichier situé derrière l’objet. il s’agit également d’un moyen de faire référence à n’importe quel type de ressource, y compris ceux non couverts par d’autres types de ressources de Windows appareils mobiles, tels qu’un type d’objet personnalisé.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d939cf58033baded231363b39410c2e527fe303075c94255a00ba96831a609b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805879"
---
# <a name="wpd_resource_default"></a>\_ressource wpd \_ par défaut

Spécifie l’ensemble du fichier situé derrière l’objet. il s’agit également d’un moyen de faire référence à n’importe quel type de ressource, y compris ceux non couverts par d’autres types de ressources de Windows appareils mobiles, tels qu’un type d’objet personnalisé.

Toutes les ressources incorporées dans la ressource spécifiée seront incluses. Par exemple, la ressource par défaut d’un dossier racine des contacts peut inclure tous les contacts imbriqués. Toutefois, les ressources enfants qui sont simplement *liées* par des métadonnées ou des références ne sont pas incluses. Il peut s’agir, par exemple, d’une sélection, qui peut uniquement être liée à des fichiers audio par le biais de références de métadonnées ou de chemins textuels dans le fichier.

La seule valeur *PID* autorisée pour cette **PROPERTYKEY** est zéro.

Ce type de ressource doit prendre en charge les attributs suivants.



| Nom de l'attribut                                                                                                            | Obligatoire ou facultatif                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_ \_ \_ taille totale de l’attribut de ressource wpd \_](resource-attribute-properties.md)              | Obligatoire.                                              |
| [l' \_ attribut de ressource wpd \_ \_ peut \_ lire](attributes.md)                                     | Obligatoire si les clients peuvent lire cette ressource.            |
| [l' \_ attribut de ressource wpd \_ \_ peut \_ écrire](attributes.md)                                   | Obligatoire si les clients peuvent écrire dans cette ressource.        |
| [l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé](attributes.md)                                 | Obligatoire si les clients peuvent supprimer cette ressource.          |
| [\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd](attributes.md)   | Obligatoire si les clients ont un accès en lecture à la ressource.  |
| [\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd](attributes.md) | Obligatoire si les clients ont un accès en écriture à la ressource. |
| [\_format d' \_ attribut de ressource wpd \_](resource-attribute-properties.md)                       | Obligatoire.                                              |
| [\_clé de \_ ressource d’attribut de ressource wpd \_ \_](resource-attribute-properties.md)                                              | Recommandé.                                           |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Conditions requises pour les ressources**](requirements-for-resources.md)
</dt> </dl>

 

 




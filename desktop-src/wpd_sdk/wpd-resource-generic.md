---
description: Spécifie un type de ressource qui n’est pas défini autrement par les appareils mobiles Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112831"
---
# <a name="wpd_resource_generic"></a>\_ressource wpd \_ générique

Spécifie un type de ressource qui n’est pas défini autrement par les appareils mobiles Windows. Vous pouvez définir vos propres ressources personnalisées qui prennent en charge tous les attributs définis par des appareils mobiles ou Windows. Toutefois, toutes les ressources que vous créez doivent prendre en charge les attributs suivants.



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

 

 




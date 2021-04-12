---
description: Objet appareil
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Objet appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef76dbe26b1fd2c8d2bfd6da708728c9eb2177b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525911"
---
# <a name="device-object"></a>Objet appareil

L’objet appareil prend en charge les propriétés suivantes. Une application peut demander ces propriétés en interrogeant l’objet racine (en spécifiant l’ID d’objet de constante d' **\_ ID d' \_ objet \_ de périphérique wpd** défini). Toutes les valeurs de l’objet Device sont en lecture seule.

Si un appareil donné implémente la catégorie d' [ \_ \_ \_ appareils de catégorie fonctionnelle wpd](wpd-functional-category-device.md) , il doit également prendre en charge les propriétés associées à cette catégorie.



| Nom de la propriété                                                                                                         | Obligatoire ou facultatif                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                | Obligatoire. La valeur est **l' \_ \_ \_ ID d’objet d’appareil wpd**.                                                         |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                 | Obligatoire. La valeur est une chaîne vide.                                                                     |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                            | Obligatoire si l’objet représente un fichier.                                                                   |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                          | Obligatoire.                                                                                                   |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                    | Obligatoire si l’objet de l’appareil ne doit pas être présenté à l’utilisateur.                                              |
| [\_références d’objets wpd \_](object-properties.md)                                                | Obligatoire si l’objet appareil a des références à d’autres objets.                                              |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                    | Optionnel.                                                                                                   |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                                                   |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md) | Optionnel.                                                                                                   |
| [\_partenaire de \_ synchronisation des appareils wpd \_](device-properties.md)                                           | Optionnel.                                                                                                   |
| [\_ \_ version du microprogramme de l’appareil wpd \_](device-properties.md)                                   | Obligatoire.                                                                                                   |
| [niveau de puissance de l' \_ appareil wpd \_ \_](device-properties.md)                                             | Recommandé si l’appareil dispose d’une batterie.                                                                    |
| [\_ \_ source d’alimentation de l’appareil wpd \_](device-properties.md)                                           | Recommandé.                                                                                                |
| [\_protocole d’appareil wpd \_](device-properties.md)                                                    | Recommandé.                                                                                                |
| [fabricant de l' \_ appareil wpd \_](device-properties.md)                                            | Obligatoire.                                                                                                   |
| [\_modèle d’appareil wpd \_](device-properties.md)                                                          | Obligatoire.                                                                                                   |
| [Numéro de série de l' \_ appareil wpd \_ \_](device-properties.md)                                         | Obligatoire.                                                                                                   |
| [l' \_ appareil wpd \_ prend en charge les appareils \_ non \_ consommables](device-properties.md)                    | Obligatoire si l’appareil prend en charge des objets non-consommables ; autrement dit, s’il peut être utilisé pour le stockage de données simple. |
| [\_ \_ date/heure de l’appareil wpd](device-properties.md)                                                    | Optionnel.                                                                                                   |
| [\_ \_ nom convivial de l’appareil wpd \_](device-properties.md)                                         | Recommandé.                                                                                                |
| [\_ \_ schéma DRM pris en charge par l’appareil wpd \_ \_](device-properties.md)                          | Recommandé si l’appareil prend en charge les Rights Management numériques (DRM).                                         |
| [\_ \_ les formats pris en charge pour les appareils wpd \_ \_ sont \_ classés](device-properties.md)       | Recommandé si l’appareil prend en charge la classification de format par défaut.                                               |
| [\_type d’appareil wpd \_](device-properties.md)                                                            | Recommandé.                                                                                                |
| [\_ \_ \_ ID unique fonctionnel de l’appareil wpd \_](device-properties.md)                          | Optionnel.                                                                                                   |
| [\_ \_ ID unique du modèle d’appareil wpd \_ \_](device-properties.md)                                    | Optionnel.                                                                                                   |
| [TRANSPORT de l' \_ appareil wpd \_](device-properties.md)                                                  | Recommandé.                                                                                                |
| [étape de l’appareil d’utilisation de l' \_ appareil wpd \_ \_ \_](device-properties.md)                                  | Optionnel.                                                                                                   |
| [\_catégorie d' \_ objet \_ fonctionnel wpd](device-properties.md)                             | Obligatoire.                                                                                                   |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets n’hébergent généralement pas de ressources.

## <a name="commands"></a>Commandes

En plus des propriétés, les appareils doivent prendre en charge un ensemble spécifique de commandes définies par les appareils mobiles Windows. Les commandes prises en charge par un objet ou un appareil dépendent de son type, de ses fonctionnalités et de ses fonctionnalités.

Le tableau suivant décrit les classes de commande qui s’appliquent aux appareils, par fonctionnalité. En règle générale, un appareil se trouve sous plusieurs catégories et doit prendre en charge les commandes pour toutes les catégories applicables. Par exemple, un téléphone mobile avec un appareil photo se présente sous trois catégories : tous les appareils, appareils SMS et périphériques de capture d’images fixes. Une application cliente et de pilote personnalisée peut prendre en charge des commandes ou des propriétés supplémentaires que vous définissez, mais elle doit prendre en charge les commandes suivantes. Pour obtenir une description des commandes spécifiques qui se trouvent sous chaque catégorie de commande, consultez [commandes](commands.md).



| Description                                                                                                                                                                                                                      | Catégories de commandes                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tous les appareils.                                                                                                                                                                                                                     | **catégorie d' \_ CAPABILITIESWPD de catégorie wpd \_ \_ \_ commune**<br/> **\_ \_ énumération d’objets de catégorie wpd \_**<br/> **\_gestion des \_ objets de catégorie wpd \_**<br/> **Propriétés de l' \_ objet de catégorie wpd \_ \_**<br/> **Propriétés de l' \_ objet de catégorie wpd \_ \_ \_**<br/> **ressources de l' \_ objet de catégorie wpd \_ \_**<br/> |
| Appareils qui peuvent capturer des images fixes, telles que des appareils photo numériques.                                                                                                                                                                  | **\_capture d' \_ \_ image continue de catégorie \_ wpd**                                                                                                                                                                                                                                                                                   |
| Appareils qui peuvent envoyer des messages SMS (Short Message Service), tels que les téléphones cellulaires. L’envoi de messages SMS est souvent appelé « messagerie texte ».                                                                                      | **\_SMS de catégorie wpd \_**                                                                                                                                                                                                                                                                                                     |
| Appareils qui fonctionnent comme des dispositifs de stockage. Celles-ci incluent des lecteurs externes. Si un appareil prend en charge la possibilité de formater un magasin ou de déplacer des objets d’un emplacement à un autre, votre pilote doit prendre en charge cette catégorie.<br/> | **\_stockage de catégorie wpd \_**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 





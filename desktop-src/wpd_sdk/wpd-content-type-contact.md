---
description: '\_contact de \_ type de contenu wpd \_'
ms.assetid: 3ff6191f-d3c0-4bd3-946e-c3fbf68f368c
title: WPD_CONTENT_TYPE_CONTACT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fed10e0abb36a482141e5c796f5494b00b99f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519472"
---
# <a name="wpd_content_type_contact"></a>\_contact de \_ type de contenu wpd \_

Objet qui décrit son type comme un \_ contact de type de contenu wpd représente des données de \_ \_ contact personnelles.

Ce type d’objet prend en charge les propriétés suivantes.



| Nom de la propriété                                                                                                                   | Obligatoire ou facultatif                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [\_ID d’objet wpd \_](object-properties.md)                                                                          | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création. |
| [\_ \_ ID parent de l’objet wpd \_](object-properties.md)                                                           | Obligatoire.                                                                      |
| [nom de l' \_ objet wpd \_](object-properties.md)                                                                      | Obligatoire si l’objet représente un fichier.                                      |
| [\_ \_ \_ ID unique persistant de l’objet wpd \_](object-properties.md)                                    | Obligatoire, en lecture seule. Un client ne peut pas définir cette propriété, même au moment de la création. |
| [\_format d’objet wpd \_](object-properties.md)                                                                  | Obligatoire.                                                                      |
| [TYPE de contenu de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Obligatoire.                                                                      |
| [WPD, \_ objet \_ ISHIDDEN](object-properties.md)                                                              | Obligatoire si l’objet est masqué.                                              |
| [WPD, \_ objet \_ ISSYSTEM](object-properties.md)                                                              | Obligatoire si l’objet est un objet système (représente un fichier système).          |
| [taille de l' \_ objet wpd \_](object-properties.md)                                                                      | Obligatoire si l’objet a au moins une ressource.                              |
| [\_nom du \_ fichier d’origine de l’objet wpd \_ \_](object-properties.md)                                        | Obligatoire si l’objet représente un fichier.                                      |
| [\_objet wpd \_ non \_ utilisable](object-properties.md)                                                 | Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.          |
| [\_références d’objets wpd \_](object-properties.md)                                                          | Obligatoire si l’objet a des références à d’autres objets.                        |
| [\_Mots clés d’objet wpd \_](object-properties.md)                                                              | Optionnel.                                                                      |
| [ID de synchronisation de l' \_ objet wpd \_ \_](object-properties.md)                                                               | Optionnel.                                                                      |
| [l' \_ objet \_ wpd \_ est \_ protégé par DRM](object-properties.md)                                            | Obligatoire si l’objet est protégé par la technologie DRM.                         |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                     | Optionnel.                                                                      |
| [Date de modification de l' \_ objet wpd \_ \_](object-properties.md)                                                   | Recommandé.                                                                   |
| [Date de création de l' \_ objet wpd \_ \_](object-properties.md)                                                   | Optionnel.                                                                      |
| [\_ \_ références arrière des objets wpd \_](object-properties.md)                                                                          | Recommandé si l’objet est référencé par un autre objet.                     |
| [\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_](object-properties.md)               | Optionnel.                                                                      |
| [\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource](object-properties.md)           | Optionnel.                                                                      |
| [\_ \_ nom complet du contact wpd \_](contact-properties.md)                                                  | Obligatoire.                                                                      |
| [l' \_ objet wpd \_ peut \_ Supprimer](object-properties.md)                                                                               | Obligatoire si l’objet ne peut pas être supprimé.                                      |
| [\_paramètres régionaux de la langue de l’objet wpd \_ \_](object-properties.md)                                                                          | Optionnel.                                                                      |
| [\_ \_ nom complet du contact wpd \_](contact-properties.md)                                                                           | Obligatoire.                                                                      |
| [\_prénom du contact wpd \_ \_](contact-properties.md)                                                      | Recommandé.                                                                   |
| [\_ \_ noms intermédiaires du contact wpd \_](contact-properties.md)                                                  | Recommandé.                                                                   |
| [\_nom de \_ famille du contact wpd \_](contact-properties.md)                                                        | Recommandé.                                                                   |
| [préfixe de \_ contact wpd \_](contact-properties.md)                                                               | Recommandé.                                                                   |
| [\_suffixe du contact wpd \_](contact-properties.md)                                                               | Recommandé.                                                                   |
| [\_ \_ prénom phonétique du contact wpd \_ \_](contact-properties.md)                                   | Optionnel.                                                                      |
| [\_ \_ nom phonétique du contact wpd \_ \_](contact-properties.md)                                     | Optionnel.                                                                      |
| [\_ \_ \_ \_ adresse postale complète personnelle du contact wpd \_](contact-properties.md)                | Recommandé.                                                                   |
| [\_ \_ Adresse postale personnelle du contact wpd \_ \_ \_ ligne1](contact-properties.md)              | Optionnel.                                                                      |
| [\_ \_ Adresse postale personnelle du contact wpd- \_ \_ \_ ligne2](contact-properties.md)              | Optionnel.                                                                      |
| [\_ \_ \_ adresse postale personnelle \_ du \_ contact wpd](contact-properties.md)                | Optionnel.                                                                      |
| [\_zone d' \_ \_ adresse postale personnelle \_ du contact \_ wpd](contact-properties.md)            | Optionnel.                                                                      |
| [\_Code postal de l' \_ \_ \_ adresse postale personnelle \_ du contact \_ wpd](contact-properties.md) | Optionnel.                                                                      |
| [\_ \_ \_ adresse postale personnelle \_ du \_ contact wpd](contact-properties.md)          | Optionnel.                                                                      |
| [\_ \_ \_ \_ adresse postale professionnelle du contact de l’wpd \_](contact-properties.md)                | Optionnel.                                                                      |
| [\_ \_ Adresse postale professionnelle du contact wpd \_ \_ \_ ligne1](contact-properties.md)              | Optionnel.                                                                      |
| [\_ \_ Adresse postale de l’entreprise contact wpd- \_ \_ \_ ligne2](contact-properties.md)              | Optionnel.                                                                      |
| [\_ \_ \_ adresse postale du contact wpd \_ \_ ville](contact-properties.md)                | Optionnel.                                                                      |
| [\_région de \_ l' \_ adresse postale du \_ contact wpd \_](contact-properties.md)            | Optionnel.                                                                      |
| [Code postal de l' \_ \_ \_ adresse postale \_ de \_ l’entreprise \_](contact-properties.md) | Optionnel.                                                                      |
| [\_ \_ \_ adresse postale du contact du Bureau wpd \_ \_](contact-properties.md)          | Optionnel.                                                                      |
| [\_ \_ autre \_ \_ adresse postale complète du contact \_ wpd](contact-properties.md)                      | Optionnel.                                                                      |
| [\_ \_ \_ Adresse postale du \_ contact avec wpd \_](contact-properties.md)                    | Optionnel.                                                                      |
| [\_ \_ Adresse postale du contact wpd- \_ \_ \_ ligne2](contact-properties.md)                    | Optionnel.                                                                      |
| [\_ \_ \_ adresse postale autre adresse postale du \_ contact \_ wpd](contact-properties.md)                      | Optionnel.                                                                      |
| [\_adresse du contact wpd \_ autre région d' \_ adresse postale \_ \_](contact-properties.md)                  | Optionnel.                                                                      |
| [\_ \_ \_ adresse postale du \_ contact \_ avec le \_ Code postal](contact-properties.md)       | Optionnel.                                                                      |
| [\_adresse postale du contact d’un \_ autre \_ \_ \_ \_ pays postal](contact-properties.md) | Optionnel.                                                                      |
| [\_ \_ \_ adresse E-mail principale du contact wpd \_](contact-properties.md)                               | Recommandé.                                                                   |
| [\_ \_ adresse e-mail personnelle du contact wpd \_](contact-properties.md)                                              | Optionnel.                                                                      |
| [\_ \_ EMAIL2 personnel de contact wpd \_](contact-properties.md)                                            | Optionnel.                                                                      |
| [\_messagerie d' \_ entreprise \_ contact wpd](contact-properties.md)                                              | Optionnel.                                                                      |
| [\_EMAIL2 de \_ travail de contact wpd \_](contact-properties.md)                                            | Optionnel.                                                                      |
| [WPD- \_ contacter d' \_ autres \_ e-mails](contact-properties.md)                                                  | Optionnel.                                                                      |
| [\_ \_ téléphone principal du contact wpd \_](contact-properties.md)                                                | Recommandé.                                                                   |
| [\_ \_ téléphone personnel du contact wpd \_](contact-properties.md)                                              | Optionnel.                                                                      |
| [\_ \_ Téléphone personnel de contact wpd \_](contact-properties.md)                                            | Optionnel.                                                                      |
| [\_ \_ téléphone professionnel du contact wpd \_](contact-properties.md)                                              | Optionnel.                                                                      |
| [\_Téléphone de \_ travail de contact wpd \_](contact-properties.md)                                            | Optionnel.                                                                      |
| [\_ \_ téléphone mobile du contact wpd \_](contact-properties.md)                                                  | Optionnel.                                                                      |
| [\_ \_ Téléphone mobile à l’adresse du contact wpd \_](contact-properties.md)                                                | Optionnel.                                                                      |
| [\_ \_ télécopie personnelle du contact wpd \_](contact-properties.md)                                                  | Optionnel.                                                                      |
| [\_télécopie pour \_ les \_ contacts wpd](contact-properties.md)                                                  | Optionnel.                                                                      |
| [\_radiomessagerie du contact wpd \_](contact-properties.md)                                                                 | Optionnel.                                                                      |
| [WPD- \_ contacter d' \_ autres \_ téléphones](contact-properties.md)                                                  | Optionnel.                                                                      |
| [\_ \_ \_ adresse Web principale du contact wpd \_](contact-properties.md)                                   | Recommandé.                                                                   |
| [\_ \_ \_ adresse Web personnelle du contact wpd \_](contact-properties.md)                                 | Optionnel.                                                                      |
| [\_ \_ \_ adresse Web de l’entreprise du contact wpd \_](contact-properties.md)                                 | Optionnel.                                                                      |
| [messageries \_ instantanées de contact pour wpd \_ \_](contact-properties.md)                                        | Recommandé                                                                    |
| [\_ \_ MESSENGER2 instant de contact wpd \_](contact-properties.md)                                      | Optionnel.                                                                      |
| [\_ \_ MESSENGER3 instant de contact wpd \_](contact-properties.md)                                      | Optionnel.                                                                      |
| [nom de la \_ société du contact wpd \_ \_](contact-properties.md)                                                  | Optionnel.                                                                      |
| [\_nom de \_ la \_ société \_ phonétique du contact wpd](contact-properties.md)                               | Facultatif                                                                       |
| [\_rôle de contact wpd \_](contact-properties.md)                                                                   | Optionnel.                                                                      |
| [\_DateNaissance contact de wpd \_](contact-properties.md)                                                         | Optionnel.                                                                      |
| [\_ \_ télécopie principale du contact wpd \_](contact-properties.md)                                                                            | Optionnel.                                                                      |
| [\_époux de contact wpd \_](contact-properties.md)                                                                                  | Optionnel.                                                                      |
| [\_enfants du contact wpd \_](contact-properties.md)                                                                                | Optionnel.                                                                      |
| [\_Assistant de contact wpd \_](contact-properties.md)                                                                               | Optionnel.                                                                      |
| [\_ \_ date anniversaire du contact wpd \_](contact-properties.md)                                                                       | Optionnel.                                                                      |
| [\_sonnerie de contact wpd \_](contact-properties.md)                                                                                | Optionnel.                                                                      |
| [\_Notes d' \_ informations \_ communes wpd](object-properties.md)                                                                        | Optionnel.                                                                      |



 

## <a name="typical-resources"></a>Ressources standard

Ces objets incluent généralement les ressources suivantes.



| Nom de la ressource                                                       | Obligatoire ou facultatif       | Description                        |
|---------------------------------------------------------------------|----------------------------|------------------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md)              | Optionnel.                  | Contient les données de contact.         |
| [**PHOTO du contact de la \_ ressource wpd \_ \_**](wpd-resource-contact-photo.md) | Recommandé, le cas échéant. | Contient une image du contact. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conditions requises pour les objets**](requirements-for-objects.md)
</dt> </dl>

 

 




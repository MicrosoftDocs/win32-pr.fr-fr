---
description: Représentation de l’appareil
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Représentation de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484737"
---
# <a name="device-representation"></a>Représentation de l’appareil

Les appareils ont deux comportements principaux qui sont traités par l’architecture WPD (Windows Portable Devices) :

-   Accès et stockage du contenu. Par exemple, les applications doivent être en mesure d’ajouter des fichiers musicaux à un lecteur de musique portable.
-   Programmation de l’appareil. Cela comprend des opérations simples telles que la modification des paramètres et la préparation de l’appareil pour la capture de données, ou des opérations plus complexes telles que le chargement du microprogramme. Il peut s’agir par exemple de l’émission d’une commande « prendre une photo » sur un appareil photo encore numérique.

Dans WPD, ces comportements sont décrits en représentant l’appareil sous la forme d’une hiérarchie d’objets. L’illustration suivante montre une représentation d’objet WPD pour un appareil à fonctions multiples, qui dans ce cas est un téléphone mobile.

![Illustration montrant la hiérarchie des objets d’un téléphone mobile](images/wpd-overview-figure3.gif)

Cette hiérarchie illustre les fonctionnalités et le contenu suivants.

Ses

-   Objet de stockage. Cet appareil a un stockage de données.
-   Service de contacts. Ce service est un objet fonctionnel qui peut être utilisé pour synchroniser et stocker des contacts sur le téléphone.
-   Service SMS. Ce service est un objet fonctionnel qui peut être utilisé pour envoyer, recevoir et stocker des messages SMS.

Contenu :

-   Objets multimédias. Ce périphérique stocke des images, de la musique et des fichiers vidéo dans des dossiers sur l’objet de stockage. Tandis que les fichiers affichés dans l’illustration sont stockés dans un dossier, un appareil peut subdiviser le contenu en dossiers organisés selon le type de support stocké. par exemple, dossiers d’images, dossiers musicaux et dossiers vidéo.
-   Objets contact. Cet appareil stocke les informations de contact (telles que le nom, le numéro de téléphone et l’adresse) en tant qu’enfants du service de contacts.
-   Objets de message. Cet appareil stocke les messages SMS en tant qu’enfants du service SMS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble de l’application**](application-overview.md)
</dt> </dl>

 

 




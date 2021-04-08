---
description: Décrit les fichiers d’entrée utilisés par WsdCodeGen et les fichiers de sortie générés par WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: À propos de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034306"
---
# <a name="about-wsdcodegen"></a>À propos de WsdCodeGen

WsdCodeGen utilise un fichier de configuration XML pour déterminer l’emplacement des métadonnées du service. Le fichier de configuration est également utilisé pour définir les noms d’interface, les GUID d’interface, les noms de classe, les noms de méthodes et d’autres identificateurs. Pour plus d’informations sur ce fichier, consultez [WsdCodeGen configuration file](wsdcodegen-configuration-file.md).

WsdCodeGen requiert deux types de fichiers d’entrée : un fichier de configuration XML et un ou plusieurs fichiers de description de service (fichiers WSDL et/ou XSD). WsdCodeGen traite ces fichiers d’entrée et génère deux types de fichiers de sortie : les fichiers d’interface et les fichiers d’en-tête/source.

## <a name="input-files"></a>Fichiers d’entrée



| Type                      | Description                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fichier de configuration        | Fichier XML qui indique l’emplacement des métadonnées du service et définit les noms d’interface, les GUID d’interface, les noms de classe, les noms de méthodes et d’autres identificateurs. |
| Fichiers de description de service | Un ou plusieurs fichiers WSDL ou XSD qui décrivent les services à implémenter sur l’appareil.                                                                           |



 

## <a name="output-files"></a>Fichiers de sortie



| Type                        | Description                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fichiers d’interface             | Fichier IDL (Interface Definition Language) qui peut être utilisé avec le compilateur MIDL pour produire un fichier d’en-tête d’interface. Les clients WSDAPI et les services WSDAPI peuvent utiliser ce fichier d’interface.                                                                                                                                                           |
| Fichiers source et en-tête C++ | Fichiers C++ qui décrivent le contrat de message, l’espace de noms et les informations de type. Ils peuvent contenir du code proxy et/ou du code stub. Le code proxy implémente l’interface d’un service et traduit les appels de méthode de service en opérations WSDAPI qui effectuent des demandes de service. Le code stub traduit les demandes du service WSDAPI en code qui appelle les méthodes de service. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Générateur de code des services Web sur les appareils](web-services-for-devices-code-generator.md)
</dt> <dt>

[Utilisation de WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 



